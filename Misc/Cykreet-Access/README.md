<h1 align="center">
  <br>
  DENY ACCESS COMMANDS
  <br>
</h1>
<p align="center">
        <a href="https://github.com/itsdoddsy/atlas-custom-commands/tree/master/Misc/Deny%20Access/Cykreet-Deny-Access/">
	<img src="https://img.shields.io/badge/Command-Deny-red.svg?maxAge=300" alt="Deny Command">
    </a>
        <a href="https://github.com/itsdoddsy/atlas-custom-commands/tree/master/Misc/Deny%20Access/Cykreet-Allow-Access/">
	<img src="https://img.shields.io/badge/Command-Allow-green.svg?maxAge=300" alt="Allow Command">
    </a>
</p>
<h4 align="center">
  <br>
  The following commands will ban the user from your server without removing them from your server.
  <br>
</h4>

* For these commands to work, you'll need to add both commands, the user should have no roles (unless you can configure it yourself) and you'll need to create a new channel exactly called `denied` and a new role called `Denied` with only the following permissions:
  * `Read Text Channels & See Voice Channels`
  * `Read Message History`

* Make sure the `Denied` role is at the bottom of the role hierarchy.

* In the `denied` channel send the following message:
  * `You have been denied access to this server by server staff.`
  * You could also use Atlas' `a!advancedembed` command to make a fancy embedded message.
  
* The `denied` channel should also have the following permissions setup:
  * Moderator Role:
    * ✅`Read Messages`
    * ❌`Send Messages`
    * ✅`Read Message History`
    * ❌`Add Reactions`
  * Denied Role:
    * ✅`Read Messages`
    * ❌`Send Messages`
    * ✅`Read Message History`
    * ❌`Add Reactions`
  * @everyone:
    * ❌`Read Messages`
    
 <h4 align="center">
  <br>
  Disclaimer: The "Denied" role should not have not have the "Read Messages" permission in any other public channels.
  <br>
</h4>
