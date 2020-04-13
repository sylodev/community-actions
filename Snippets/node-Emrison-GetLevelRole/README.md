**Description:** This snippet will display the ID of the Level Role that a user just earned, which can then be used in a `{role.mention}` or other role-related tags.

**Instructions:** Before incorporating this snippet into your guild, it's important that **Stack Rewards** is **disabled**. If you're fine with that, head over to the Levels plugin on your server's dashboard, and copy+paste the code below to the top of your Level Up message box. Then, you can use `{get;LevelRole}` to display the ID of the role that the user just earned. This is to be used like so:
- `{role.mention;{get;LevelRole}}`
- `{role.name;{get;LevelRole}}`

Please note that if you plan to use this snippet in an embedded level up message, `{role.mention}` does **not** work in Titles, Field Names, or Author Names. If you'd like to refer to the role in one of these embed elements, use `{role.name}` instead.

**Code:** ```{set;LevelRole;{find;{user.roles};({replace;{find;{settings;plugins.levels.options.rewards};([\d+]{17,18});-1;g};\s;|})}}```