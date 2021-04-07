# Color Roles
This action lets you list roles, assign and remove them to/from yourself. This action includes four subcommands and three references from native Atlas commands.

## Setup
There are a few parts of this action command that you need to setup before you can use it.

1. You need to create some color roles, if not already created.  
2. Replace `NUMBER` in `{set;roles_amount;NUMBER}` to the number of color roles you just created.
3. Change `COLOR_ROLE_ID` in `{set;1;COLOR_ROLE_ID}` to the ID of your color role.
   You can add more roles by copy pasting the `{set;1}` tag and replacing them with numbers `2`, `3`, `etc...`
4. If you added (or removed) a color role(s), you would need to add in a `{role.mention;{get;2}}` tag in the `list` if statement, replacing the `2` in `get;2`with the next highest number from the `set` section.
5. Congrats! you have your color role action all set up 🎉.

