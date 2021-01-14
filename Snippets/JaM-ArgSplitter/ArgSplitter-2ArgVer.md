**Instructions:** Use `{get;arg1}` and `{get;arg2}` to obtain the set arguments. If you want to use this method across more than a single action, replace `set` and `get` with `perset` and `perget`.

**Code:** 
```
{set;arg1;{find;{args};(.*)(?:\s?(?:\||,|\/)\s?)(.*)$;1}}
{set;arg2;{find;{args};(.*)(?:\s?(?:\||,|\/)\s?)(.*)$;2}}
```