**Instructions:** Use `{get;arg1}`, `{get;arg2}`, and `{get;arg3}` to obtain the set arguments. If you want to use this method across more than a single action, replace `set` and `get` with `perset` and `perget`.

**Code:** 
```
{set;arg1;{find;{args};(.*?)(?:\s?)(?:\|)(?:\s?)(.*?)(?:\s?)(?:\|)(?:\s?)(.*?$);1}}
{set;arg2;{find;{args};(.*?)(?:\s?)(?:\|)(?:\s?)(.*?)(?:\s?)(?:\|)(?:\s?)(.*?$);2}}
{set;arg3;{find;{args};(.*?)(?:\s?)(?:\|)(?:\s?)(.*?)(?:\s?)(?:\|)(?:\s?)(.*?$);3}}
```