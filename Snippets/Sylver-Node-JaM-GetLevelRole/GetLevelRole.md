**Instructions:** Paste the code at the very top of your level-up message box then use `{get;LevelRole}` to retrieve the level-up reward role in context (if there is one).

**Code:** 
```
{set;LevelRole;{find;{settings;plugins.levels.options.rewards};"level":{user.level},[^{r}]+?"content": ?"([0-9]+)}}
```

**Note:** A simple `{if}` check can output the reward role message only if it exists. For example:
```
{set;LevelRole;{find;{settings;plugins.levels.options.rewards};"level":{user.level},[^{r}]+?"content": ?"([0-9]+)}}

{channel.send;Congratulations {user.mention}! You just advanced to **level {user.level}**{if;{get;LevelRole};and gained the {role.mention;{get;LevelRole}} role}!}
```