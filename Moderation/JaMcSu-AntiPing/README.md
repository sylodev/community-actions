# AntiPing v2.1
AntiPing is a custom solution for discouraging tagging individual users from a predefined list. Previously this was a private action used exclusively on the Atlas support server, however I've decided to release it to the public. It's fairly simple to setup, so lets get right into it.

## Setup
* Follow the instructions for importing action files into your guild by following the steps found on the repository [README](https://github.com/doddsy/atlas-custom-actions/blob/master/README.md).
* Once imported to your guild, navigate to the **messageCreate** part of the action on your dashboard and populate the `NotifChannel` and `AP_List` variables at the top of the action according to the settings you want.
* On the **messageCreate** action, blacklist any roles you dont want to be affected by the AntiPing. On the **Command** action, whitelist the roles you want to be able to use the command.
* Optionally you can also enable `Delete invocation message` on the **messageCreate** action to delete the message whenever a user mentions someone on the AntiPing list.
* Woopdeedoo, if you didn't screw it up, AntiPing should be up and functioning in your guild. Try executing `a!ap help` in a text channel to see a complete list of AntiPing commands.

### Things to Note
* By default, AntiPing will hand out a verbal warning for the first AntiPing infraction and an official Atlas warning for every subsequent infraction. Currently the way actions use Discord permissions is a bit broken so muting, kicking, banning is not a possibility. In a future Atlas update, this should be fixed and AntiPing will be updated to reflect those changes.
* AntiPing keeps internal track of infractions dealt out to users who trigger the AntiPing, any time a user mentions someone on the AntiPing list, it will generate one perset *per user* to keep an accurate count. Persets are a limited resource, each guild is alotted 500 by default, so take this into consideration when importing AntiPing.
* If you wish to remove a user's AntiPing infractions, you must have Administrator permissions to execute the command: `a!eval {perset;<user id here>_PingCount;}`. This may be a built-in feature in a future AntiPing update but for now, this is how it's done. Note that this will *only* reset their AntiPing infractions count, it *will not* remove any warnings they recieved.
