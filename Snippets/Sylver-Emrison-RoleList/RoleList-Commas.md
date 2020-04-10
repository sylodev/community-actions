**Note:** Seperates role mentions with commas (@Role1,@Role2,@Role3,@Role4,@Role5).

**Code:** 
```
{replace;{replace;{user.roles};(\d+);<@&$1>};\s;,}
```