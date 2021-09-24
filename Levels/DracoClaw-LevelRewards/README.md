A wrapper for the `a!level` command that adds a new sub-command.  

Auto generates an embed with information about the Role Rewards of the Levels plugin.  

Includes: 
- Total Rewards
- Reward Roles and the Levels asociated with them
- States of: 
	- DM Notifications
	- Stack Rewards
	- Role Sync.

Valid args are `role(s)` or `reward(s)`.  If neither are provided, the command defaults to native `a!level` functionality.

⚠ If you experience issues with the command, please run `a!tageval {settings;plugins.levels.options.rewards}` and ensure that all entries follow this format.  
`{"_id":"60de1cc74b8f911f86baf803","level":1,"type":"role","content":"627151734258794496"}`  
If an entry does not follow that format, simply delete the reward and remake it. Here is an example of an incorrectly formated reward.  
`{"_id":"5d46e8b7e9f17e0011ffa77d","content":"534877373963829248","level":20,"type":"role"}`
