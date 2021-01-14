**Instructions:** Use `{get;arg1}`, `{get;arg2}`, `{get;arg3}`, `{get;arg4}`, and `{get;arg5}` to obtain the set arguments. If you want to use this method across more than a single action, replace `set` and `get` with `perset` and `perget`.

**Code:** 
```
{set;arg1;{find;{args};(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)$;1}}
{set;arg2;{find;{args};(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)$;2}}
{set;arg3;{find;{args};(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)$;3}}
{set;arg4;{find;{args};(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)$;4}}
{set;arg4;{find;{args};(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)(?:\s?(?:\||,|\/)\s?)(.*)$;5}}
```