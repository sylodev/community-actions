These actions will enable advanced verification on your server. When people join, they will be DM'ed a unique verification code that they have to paste in a special channel to gain access to the rest of your server. Here's how to set it up:

* To use this action library, you must first create a role named `Unverified` and give it no permissions.
* Next go to the **Roles** module on your guild's dashboard, and select the `Unverified` role as a Join Role.
* Create a channel named `#verify` and restrict `@everyone`'s permissions to it, except for the `Unverified` role.
* Copy and paste the action codes above into your dashboard and save them.
* Now when people join your server, they will be given the `Unverified` role and Atlas will DM them a verification code. If they paste the verification code into `#verify`, the `Unverified` role will be removed and they will gain access to the rest of your server!
