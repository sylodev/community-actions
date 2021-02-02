**Instructions:**
* Replace `INPUT_HERE` with anything you want to parse.

**Code**
```js
/* normal numbers */
{math;abs(INPUT_HERE)}

/* numbers ending with "k" or "thousand" */
{math;abs({replace;INPUT_HERE;k$;e3})}
/* numbers ending with "m" or "million" */
{math;abs({replace;INPUT_HERE;m$;e6})}
/* numbers ending with "b" or "trillion" */
{math;abs({replace;INPUT_HERE;b$;e9})}
```
