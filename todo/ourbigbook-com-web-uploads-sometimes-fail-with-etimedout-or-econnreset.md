<h1 id="ourbigbook-com-web-uploads-sometimes-fail-with-etimedout-or-econnreset">ourbigbook.com --web uploads sometimes fail with ETIMEDOUT or ECONNRESET</h1>

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Bug](bug.md), [Web upload](web-upload.md)

<a id="_188"></a>
ourbigbook --web sometimes randomly times out on ourbigbook.com. First an ID extraction or render hangs, and then after a few seconds things blow up Usually happens around the thousands of articles uploaded.

<a id="_189"></a>
I've seen it happen once or twice locally as well.

<a id="_190"></a>
There are no server exceptions on `heroku logs`. I simply can't understand why it happens.

<a id="_191"></a>
Once the error was `ETIMEDOUT`, but most times it was `ECONNRESET`.

<a id="_192"></a>
<a id="_193"></a>
- [https://stackoverflow.com/questions/17245881/how-do-i-debug-error-econnreset-in-node-js](https://stackoverflow.com/questions/17245881/how-do-i-debug-error-econnreset-in-node-js)

<a id="_194"></a>
Next time it happens I'm just going to add a timeout plus retry mechanism as it is rare enough that it shouldn't matter, and the problem does seem to go away if I try to continue the upload immediately afterwards: given the SHA2-based skips, restarting from the CLI we just start exactly where we had left off, so hopefully will also work from Js.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
