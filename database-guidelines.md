# Database guidelines

↑ **Parent:** [Developing OurBigBook](developing-ourbigbook.md)

Every foreign key should have a manually created associated index, this is not done automatically by neither PostgreSQL nor Sequelize:
- [https://stackoverflow.com/questions/970562/postgres-and-indexes-on-foreign-keys-and-primary-keys](https://stackoverflow.com/questions/970562/postgres-and-indexes-on-foreign-keys-and-primary-keys)
- [https://github.com/sequelize/sequelize/issues/5042](https://github.com/sequelize/sequelize/issues/5042)

## ↑ Ancestors (2)

1. [Developing OurBigBook](developing-ourbigbook.md)
2. [OurBigBook Project](split.md)
