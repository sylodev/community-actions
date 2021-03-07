# Color Roles
 Color Roles is a action with **4** sub commands and **one** reference to a native Atlas Command. This action lets you list roles, assign and remove them to/from yourself.

 ## Setup
 There are a few parts of this action command that you need to setup before you can use it.

 1) You need to create some color roles, if not already created.
    
2) Change NUMBER in {set;roles_amount;NUMBER} to the number of color roles you jut created.

3) Change COLOR_ROLE_ID in {set;1;COLOR_ROLE_ID} to the ID of your color role.
    *You can add additional color roles by copy pasting {set;1;COLOR_ROLE_ID} and changing the set;1 section to set;2 (etc for howver mnay color roles you have).*

4) If you have added (or removed) color roles then you would need to amend the first if statement and add in 2. {role.mention;{get;2}} (etc for howver mnay color roles you have). 

5) Congrats, you have your color role action all set up.🎉

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