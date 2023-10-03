This is basically like the Auto Roles provided by Atlas natively but the fact that it can be *conjured* up anywhere at any time without using the dashboard. 
It supports select menus and buttons as well.

How to set it up?
- After importing the action, in a discord text channel, run `/reactrole add group` with the related information. Running this will create a new reactrole "group" which which is going to be like a shell housing all the roles of that group
- This also supports inputting a default emoji for your roles. If a default emoji is provided, then atlas will use that emoji if a specific one isn't there for a role (More info below).
- This also supports custom messages with placeholders as well. The placeholders are displayed at the end of this page. You can use them to be replaced with the corresponding stuff in the output message when the reactrole is used. Kindly note that this will NOT be used in case multiple roles in select menus are added together.
- Then, we can start adding roles to this group we created. Run `/reactrole add role` along with the required information. This will add the said role in the group.
- You can specify an emoji for each role which overrides the default group emoji. It would be displayed along with the role name in the reactionrole.
- You can also put in a message for THIS specific role which overrides the default message. (Also supports placeholders) (Kindly note that this will NOT be used in case multiple roles in select menus are added together.)
- Now, you can add more roles using the same command multiple times
- You are all done. To make the reactionrole message, simply run `/reactrole make` and specify the name of a group with an optional channel where the message will be sent!

How to remove a role/group
- To remove a group or role, use the `/reactrole remove` command
- When using the command, specifying just the group name will delete the group PERMANENTLY. This is irreversible.
- If you specify the role as well, it will simply remove that specific role from that group. This is also permanent.

**Placeholders for messages**
- role_mention: Mentions the role added/removed
- user_mention: Mentions the user who clicked on the reactrole
- role_id: Role ID of the role
- role_color: Color of the role
- function_todo: Outputs `added to` if the role is added and `removed from` if the role is removed!
