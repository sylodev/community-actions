<div align="center">

# Gamble
A very fun, easy-to-use gambling game made for Atlas.

</div>

## Features

* **Bank space** - Increases overtime whenever you use gambling commands.
* **Boss fights** - Interact with atlas to redeem your win!
* **Customizable** - you have the freedom to modify/control your gameplay.
* **Bug free** - Exploiting is nearly 100% impossible.
* **Compatability** - The economy system works with 500 or less than members.

### Setup

1. Follow the instructions on [how to import actions into your Atlas dashboard](../../README.md#import-actions-from-this-repository-into-your-server) first.
2. After importing, you first, should whitelist yourself for testing purposes:
	* `a!currency whitelist @user` - `@user` resolves the rest of the command arguments after `whitelist`
	* `a!currency whitelist` - leaving the `@user` argument will auto whitelist the invocation user
3. You're now done! You can now play the game.


### Command Information
> **Legend**\
**<>** - required arguments\
**[]** - optional arguments

Command | Description | Usage | Permissions | Requires Whitelist
:---: | :---: | :---: | :---: | :---:
currency | Has certain tools to configure the game, or even manage someone's data. | `a!currency <...args>` | Manage Server | false
help | Triggers whenever you leave command arguments **empty**. | `a!gamble`, `a!give` | Send Messages | true
balance | Checks someone elses balance or yours if you don't specify a user. | `a!balance [@user]` | Send Messages | true
give | Gives other users some coins; the higher the give, the higher the tax. | `a!give <amount> <@user>` | Send Messages | true
withdraw | Withdraws some coins from your vault into your pocket. | `a!withdraw <amount>` | Send Messages | true
deposit | Deposits your specified amount of coins into your vault for safe keeping purposes. | `a!deposit <amount>` | Send Messages | true
gamble | Gamble rolls a **d12** dice, whoever gets the higher roll, wins! | `a!gamble <amount>` | Send Messages | true
slots | Slot machine gives you **double** or even **triple** of your bet if you win a jackpot. | `a!slots <amount>` | Send Messages | true

### Credits
* [Number Formatter](https://github.com/sylo-digital/community-actions/tree/master/Snippets/JaM-NumberFormatter) - JaM#8608
* <a href="https://regexr.com" target="_blank">regexr.com</a> - My lovely assistant for Regular Expressions.
