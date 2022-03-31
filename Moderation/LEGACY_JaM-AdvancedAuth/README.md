# AdvancedAuth v2.1
AdvancedAuth is a powerful & fully-customizable guild authentication system. It has multiple levels of defense ranging from low to high security, which can be changed at a moment's notice. AdvancedAuth is extremely useful for helping to prevent raids or just to screen new users before allowing them access to your server.

### Available Security Levels
* **Level 0 - OFF**
AdvancedAuth is disabled in this state. New users require no authentication.

* **Level 1 - REACTION**
New members must react to a message to gain access to the entirety of your server.

* **Level 2 - KEYWORD**
New users are DMed a random keyword that they must type in the verification channel to gain access to the entirety of your server.

* **Level 3 - MATH**
New users are DMed a random math problem that they must type the solution in the verification channel to gain access to the entirety of your server.

* **Level 4 - QR CODE**
New users are DMed a QR code containing a random PIN code that they must type in the verification channel to gain access to the entirety of your server.

* **Level 5 - STAFF VERIFICATION**
New users are dropped into a ticket channel where they can chat one-on-one with a member of your staff team.

## Setup
Setting this superaction up in your guild is a bit harder than a normal superaction. If you're not familiar with importing or editing actions, you should consider not using this superaction. 
* First, let's create a role named `Unverified` (or a name you like better) that has it's **Read Messages & Send Messages** permissions denied. We will also create a channel named `verification` (or a name you like better), deny `@everyone`'s **Read Messages, Send Messages, & Add Reactions** permissions to that channel, and allow the `@Unverified` role **Read Messages & Send Messages** permissions. Enable channel slow-mode and set to `10 seconds`.
* We will need the IDs for both the `#verification` channel and the `@Unverified` role you just created. To do so, execute the `a!id <ROLE_NAME_HERE>` or `a!id <CHANNEL_NAME_HERE>` command and save the outputs for later.
* Next, let's head over to your [dashboard](https://atlas.bot/@me/guilds), select the guild you want to install AdvancedAuth in, and import all of the `.action` files found within this superaction. For a step-by-step on how to do this, see [here](https://github.com/sylo-digital/community-actions#import-actions-from-this-repository-into-your-server).
* Select the **Command** action, scroll down to **Script One**, and replace the value of the `UnverifiedRole` variable with the ID of the `Unverified` role.
* Navigate to the **Member Join** action, scroll down to **Script One**, and replace the value of the `VerifyChannel` variable with the ID of the `#verification` channel.
	* (OPTIONAL STEP) In the same **Member Join** action, edit the value of the `SVMessage` variable to something more personalized to your server. This message will only show up with **Level 5** authentication enabled.
* Now it's time to set whitelists to ensure only people who are supposed to use things are the ones who are actually using them. 
	* Select the **Command** action, select the **Role Whitelist** field and select a trusted staff role. (Our recommendation for roles whitelisted to this command should have **Manage Server** permissions or above.)
	* Select the **Message Create** action, select the **Trigger Content** field and select the `#verification` channel. Next select the **Role Whitelist** field and select the `@Unverified` role. Finally, select the **Channel Whitelist** field and select the `#verification` channel.
	* Select the **Reaction Add** action, select the **Channel Whitelist** field and select the `#verification` channel.
		* (OPTIONAL STEP) If you want to change the emoji that new members must react to gain access to your server, select the **Trigger Content** field and select your new emoji. This will only affect your server if you have **Level 1** authentication enabled.
* Now that everything is configured, you can enable AdvancedAuth. By default, AdvancedAuth is disabled (Level `0 | OFF`). To enable it, execute the `a!auth set <AUTH_LEVEL_HERE>` command. 

### Special Setup for Different Authentication Levels
If you have decided to use one of the following authentication levels in your server, you would do well to follow these special setup instructions.
* **Level 1 - REACTION**
In your `#verification` channel, you may want to write a short message to the effect of: **`Please react :EMOJI_HERE: to this message to gain access to the entirety of GUILD_NAME_HERE.`** Then to add the proper reaction to that message, execute the `a!tageval {message.react;EMOJI_NAME;MESSAGE_ID}` command.

* **Level 2-4 - KEYWORD, MATH, QR CODE**
For these authentication levels, you may want to write a short message in your `#verification` channel to the effect of: **`Please check your DMs for an authentication key to gain access to the entirety of GUILD_NAME_HERE.`**

* **Level 5 - STAFF VERIFICATION**
This authentication level requires the **Tickets** plugin to be enabled in your guild to function. You will also be alerted of this when you execute the command to set your authentication level to `5 | STAFF VERIFICATION`. You may also want to write a short message in your `#verification` channel to the effect of: **`We have opened a private channel for you to talk to one of our staff members. If accepted, you will gain access to the entirety of GUILD_NAME_HERE.`**

**Tip: If you want to make any of the above messages a bit fanicier, use our [Embed Builder](https://atlas.bot/embed-builder)**.

-----

**Last tested on Atlas version:** `8.4.9`
