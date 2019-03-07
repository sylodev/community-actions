# BasicallyBastion Documentation
BasicallyBastion is a recreation of the proprietary Bastion bot which does some menial tasks on the [Atlas support server](https://atlasbot.xyz/support), including handling suggestions. Currently this is Bastion's only job, so this action-pack emulates that feature using custom actions within Atlas itself (a lot easier than trying to host a local instance of Bastion). This action-pack is **meant to be edited by the user**, right now it *exactly* emulates Bastion so the messages are *very* server specific. If you don't know what that means, you probably shouldn't be using this...

## Initial Setup
* Follow the steps on the [repository README](https://github.com/doddsy/atlas-custom-actions/blob/master/README.md) for importing action files.
* Once both action files are imported into your guild, click on the **Message Create** action and edit the values for the `SuggestionApprovalChannel` & `SuggestionChannel` fields according to your server's preferences. (See **Recommended Permissions , Restrictions & Settings**)
* Next, edit the values for the `UpvoteEmoji` & `DownvoteEmoji` fields according to your server's preference.
* Thats it, it's pretty plug-and-play!

### Recommended Permissions, Restrictions & Settings
**Suggestion Channel**
* @everyone - Read Messages | Allow
* @everyone - Send Messages | Allow
* @everyone - Add Reactions | Deny
* Atlas - Add Reactions | Allow
* Slow-Mode - Enabled | Minimum of 15 seconds.
(This step is actually required for it to not break because of how Discord handles **messageCreate**)

**Suggestion Approval Channel**
* @everyone - Read Messages | Deny
* Staff Members - Read Messages | Allow
* Staff Members - Send Messages | Allow
* Atlas - Send Messages | Allow
* Atlas - Read Messages | Allow

**Message Create Action**
* Trigger Content - Same channel as `SuggestionChannel`
* Channel Whitelist - Same channel as `SuggestionChannel`

**Command Action**
* Channel Whitelist - Same channel as `SuggestionApprovalChannel`
* Role Whitelist - Same roles that have access to `SuggestionApprovalChannel` **(OPTIONAL)**

**Alright! BasicallyBastion should now be properly setup on your server. Once someone inputs a suggestion, use the** `a!suggestion approve <ID>` **or the** `a!suggestion deny <ID>` **command in the** `SuggestionApprovalChannel` **to approve or deny suggestions.**

**Note:** Dont like all the deletion messages in your action logs? Paste `actionlog-ignore` in the channel topic to bypass it.
