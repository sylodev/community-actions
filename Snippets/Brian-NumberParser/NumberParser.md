**Instructions:**
* Replace `INPUT_HERE` with anything you want to parse.

**Code**
```js
/**
 * Normal Floats 
*/
{math;abs(INPUT_HERE)}

/**
 * Human Readable Numbers
 * * k - thousands
 * * m - million
 * * b - billion
*/
{math;abs({replace;{replace;{replace;INPUT_HERE;k$;e3};m$;e6};b$;e9})}
```
