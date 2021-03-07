# Color Roles
This action lets you list roles, assign and remove them to/from yourself. This action includes four subcommands and one reference from a native Atlas command.

## Setup
There are a few parts of this action command that you need to setup before you can use it.

1. You need to create some color roles, if not already created.  
2. Replace `NUMBER` in `{set;roles_amount;NUMBER}` to the number of color roles you just created.
3. Change `COLOR_ROLE_ID` in `{set;1;COLOR_ROLE_ID}` to the ID of your color role.\
   You can add more roles by copy pasting the `{set;1}` tag and replacing them with numbers `2`, `3`, `etc...`
4. If you already added (or removed) a color role, you would need to ament the first `{if}` statement and add in `2` and do the same for our `{role.mention;{get;2}}` tag.
5. Congrats! you have your color role action all set up 🎉.

## Optional
You can remove Use `{guild.prefix}color help` to get help with this action if you do not wnat to be told how to bring up the help menu evey time you use ?color (which would be everytime you use one of the subcommands).

## Planned Addons
- A command to make a color role with specified hex.
- A command to make a color role with specified rgb codes?🤔
- A command to add color roles by tagging them.
- A command to delete color roles.
- A auto-color-role which gives either a chosen color or a random one when someone joins.
- A command to give users a random color role from the list.
- A togelable command to let users be dmed, or not, when they receive a role.
