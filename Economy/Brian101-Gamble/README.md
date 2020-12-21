<div align="center">

# Gamble
A very fun, easy-to-use gambling game made for Atlas.

</div>

## Features

* **Bank space** - Increases overtime whenever you use gambling commands.
* **Boss fights** - Interact with atlas to redeem your win!
* **Customizable** - you have the freedom to modify/control your gameplay.
* **Bug free** - Exploiting is nearly 100% impossible.
* **Shop Menu** - A cool, shop menu to spend your coins to.
* **Compatability** - The economy system works with 500 or less than members.

### Setup

1. Follow the instructions on how to import actions into your Atlas dashboard first.
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
currency | this will serve as your tool to control the currency system | `a!currency <...args>` | Manage Server | false
help | trigger the help menu by leaving any command arguments **empty**| `a!gamble`, `a!give` | Send Messages | true
balance | checks your or someone else's balance | `a!balance [@user]` | Send Messages | true
give | gives other user coins | `a!give <amount> <@user>` | Send Messages | true
withdraw | withdraw coins from your bank | `a!withdraw <amount>` | Send Messages | true
deposit | deposit coins to your bank | `a!deposit <amount>` | Send Messages | true
gamble | roll a dice and win | `a!gamble <amount>` | Send Messages | true
slots | use the slot machine to win a jackpot price | `a!slots <amount>` | Send Messages | true

### Credits
* [Number Formatter](https://github.com/sylo-digital/community-actions/tree/master/Snippets/Emrison-NumberFormatter) - JaM#8608
* <a href="https://regexr.com" target="_blank">regexr.com</a> - My lovely assistant for Regular Expressions.
