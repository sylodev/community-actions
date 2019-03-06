# BasicallyBastion Documentation
BasicallyBastion is a recreation of the proprietary Bastion bot which does some menial tasks on the [Atlas support server](https://atlasbot.xyz/support), including handling suggestions. Currently this is Bastion's only job so this action-pack emulates that feature using custom actions within Atlas itself. If you don't know what that means, you probably shouldn't be using this...

## Initial Setup
* Follow the steps on the [repository README](https://github.com/doddsy/atlas-custom-actions/blob/master/README.md) for importing action files.
* Once both action files are imported into your guild, click on the **Message Create** action and edit the values for the `SuggestionApprovalChannel` & `SuggestionChannel` fields according to your servers preferences. (See **Recommended Permissions , Restrictions & Settings**)
* Thats it, it's pretty plug-and-play!

### Recommended Permissions, Restrictions & Settings
**Suggestion Channel**
* @everyone - Read Messages | Allow
* @everyone - Send Messages | Allow
* @everyone - Add Reactions | Deny
* Atlas - Add Reactions | Allow
* Slow-Mode | Enabled (Minimum of 10 seconds)

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
