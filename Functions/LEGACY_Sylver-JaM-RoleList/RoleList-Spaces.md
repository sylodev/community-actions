**Note:** Seperates role mentions with spaces (@Role1 @Role2 @Role3 @Role4 @Role5)

**Code:** 
```
{replace;{user.roles};(\d+);<@&$1>}
```