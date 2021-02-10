# Ticket System
Ticket System is a (super)action with a total of 3 actions. This (super)action let you manage users, such as blacklisting them and only letting them open one ticket. You can also add a reaction "panel" where your users react to Atlas' message and are able to create a ticket.

## Setup
We are going to start the setup process, I have tried to make it simple, so this is going to be fast and easy.

* Setting up Discord permissions.

We will create a ticket channel or information channel, whatever you want to call it, where main Atlas' message will get posted within the reaction.
To this channel, you must set the `@everyone` role `Send Messages` permissions to X, to prevent users from talking there. (Make sure to also keep any other role on Neutral), second, you will create a role called `Ticket Reason` or `Reason`, anything you want it to be called, this is a temporal role Atlas will add to talk inside the channel, for this, make sure you set this role `Send Memssages` permissions to ✔️.

As a second channel, you will create a "redirect" channel, where some Atlas' natives responses will get sent, make it a private channel that your staff or only the server owner can see. Make sure Atlas can view it and send messages there. ;)

Also, make sure Atlas has proper permissions to send messages and add reactions in that channel. Sometimes the ticket plugin is a bit buggy when Atlas does not have Administrator, so a good option would be giving Administrator to Atlas to prevent future errors.

* Setting up whitelists.

Awesome, we have all our needed permissions and channels, now we will go to our dashboard and find the Ticket reaction add action. Once you navigated to it, we will set a `Channel Whitelist` for it, this whitelist will be our "ticket channel". This is to make it so if users react with a Ticket in any other channel, it gets ignored and only triggers in our ticket channel.

* Final Setup.

Alright, if you followed everything correctly, now we can setup the last things, instead of going to your action and searching the persets, I have made a setup process included in the `ts` command. Just run `a!ts setup` and a series of prompts will trigger, provide the channel ID of the ticket channnel your created, the redirect channel ID and finally the reason role ID. If you need time searching the ID's, each prompt will trigger after 300 seconds of no response or if you say `cancel`. 
This should be everything, feel free to give it a test, you can use `a!ts help` to see all the subcommands and information.

* Support Server

If you're stuck, or need help, feel free to join Atlas [support server](https://discord.gg/4HWswAxfcP) and ask for the (super)action creator, [dark#8901](https://discord.com/users/449245847767482379).