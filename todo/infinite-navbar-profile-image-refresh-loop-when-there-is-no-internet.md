# Infinite navbar profile image refresh loop when there is no Internet

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Offline development](offline-development.md)

<a id="_650"></a>
This might be something to do with us trying to have a dummy fallbak image when the image URL does not exist.

<a id="_651"></a>
The request is:<a id="_652"></a>

```
GET https://static.productionready.io/images/smiley-cyrus.jpg net::ERR_INTERNET_DISCONNECTED
```
so it appears to be trying to infinitely fetch the default image.

<a id="_653"></a>
For now we seem to have managed to stop it from going infinite by selecting an image that is stored locally in the website.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
