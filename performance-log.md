# Performance log

↑ **Parent:** [Performance](performance.md)

On P51:

- `time ./ourbigbook --no-render . && time ./ourbigbook -S --log=perf index.bigb`:


  - ourbigbook 39e633f08b2abce10331b884c04d70dbe6d4565a before moving OurBigBook to Sequelize: 14s
    ```
    convert index.bigb
    perf start 248.0712810009718
    perf tokenize_pre 248.36641899868846
    perf tokenize_post 2027.6697090007365
    perf parse_start 2028.678952999413
    perf post_process_start 2684.3162699975073
    perf post_process_end 5017.946601998061
    perf split_render_pre 6572.925067000091
    perf render_pre 5018.202895000577
    perf render_2_pre undefined
    perf render_post 13093.658641997725
    perf end 13126.138450000435
    perf convert_input_end 14281.568749997765
    perf convert_path_pre_sqlite 14281.64151499793
    perf convert_path_pre_sqlite_transaction 14281.835940998048
    perf convert_path_post_sqlite_transaction 14551.673818998039
    perf convert_path_end 14551.860617998987
    convert index.bigb finished in 14309.703324001282 ms
    perf convert_path_to_file_end 14552.230636000633

    real    0m14.602s
    user    0m16.500s
    sys     0m1.832
    ```

    `sqlite3 _out/db.sqlite3 .schema`
    ```
    CREATE TABLE IF NOT EXISTS 'ids' (
            id TEXT PRIMARY KEY,
            path TEXT,
            ast_json TEXT
          );
    CREATE TABLE IF NOT EXISTS 'includes' (
            from_id TEXT,
            from_path TEXT,
            to_id TEXT,
            type TINYINT
          );
    CREATE INDEX includes_from_path
          ON includes(from_path);
    CREATE INDEX includes_from_id_type
          ON includes(from_id, type);
    CREATE TABLE IF NOT EXISTS 'files' (
            path TEXT PRIMARY KEY,
            toplevel_id TEXT UNIQUE
          );
    ```


  - ourbigbook 8e6a4311f7debd079721412e1ea5d647cc1c2941 after, OMG gotta debug perf now:
    ```
    real    0m29.595s
    user    0m34.095s
    sys     0m4.427s

    convert index.bigb
    perf start_convert undefined
    perf tokenize_pre 411.71094800531864
    perf tokenize_post 2265.3646410033107
    perf parse_start 2266.436312004924
    perf post_process_start 2905.8304330036044
    perf post_process_end 12113.761793002486
    perf split_render_pre 16534.5258340016
    perf render_pre 12114.092462003231
    perf render_post 40937.611143000424
    perf end_convert undefined
    perf convert_input_end 42042.85608199984
    perf convert_path_pre_sqlite 42042.92515899986
    perf convert_path_pre_sqlite_transaction 42147.847070001066
    perf convert_path_post_sqlite_transaction 42732.242132000625
    perf convert_path_end 42732.35991900414
    convert index.bigb finished in 42327.62727500498 ms
    perf convert_path_to_file_end 42732.534088000655

    real    0m42.779s
    user    0m46.530s
    sys     0m6.945s
    ```

    `sqlite3 _out/db.sqlite3 .schema`
    ```
    CREATE TABLE `Files` (`id` INTEGER PRIMARY KEY AUTOINCREMENT, `path` TEXT NOT NULL UNIQUE, `toplevel_id` TEXT UNIQUE);
    CREATE TABLE sqlite_sequence(name,seq);
    CREATE INDEX `files_path` ON `Files` (`path`);
    CREATE INDEX `files_toplevel_id` ON `Files` (`toplevel_id`);
    CREATE TABLE `Ids` (`id` INTEGER PRIMARY KEY AUTOINCREMENT, `idid` TEXT NOT NULL UNIQUE, `path` TEXT NOT NULL, `ast_json` TEXT NOT NULL);
    CREATE INDEX `ids_path` ON `Ids` (`path`);
    CREATE TABLE `Refs` (`id` INTEGER PRIMARY KEY AUTOINCREMENT, `from_id` TEXT NOT NULL, `from_path` TEXT NOT NULL, `to_id` TEXT NOT NULL, `type` TINYINT NOT NULL);
    CREATE INDEX `refs_from_path` ON `Refs` (`from_path`);
    CREATE INDEX `refs_from_id_type` ON `Refs` (`from_id`, `type`);
    CREATE INDEX `refs_to_id_type` ON `Refs` (`to_id`, `type`);
    ```

    The question is: is it because we added `async` Everywhere, or is it because of changes in the database queries?

    Answering the question: added old DB at: [https://github.com/ourbigbook/ourbigbook/tree/async-slow-old-db](https://github.com/ourbigbook/ourbigbook/tree/async-slow-old-db) and it is fast again. So DB debugging it is, hurray.

## ↑ Ancestors (3)

1. [Performance](performance.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Performance](performance.md)
