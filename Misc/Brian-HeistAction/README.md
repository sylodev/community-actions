# HeistAction
This action allows you to manage heist events in your discord server.

## Features
- **Customizable** - Customize the heist message however you want. Either emnbed or a normal one, it's up to you really.
- **Checkers** - OPTIONAL - Check their balance first if all required arguments are correct.

## Instructions
The only things you should change are the `{set}` variables on top of the action code. These variables are only roles which should be pinged as you start an event.
1. Change what's in `role.heist` with the ID of your `Heist Ping` role
2. Change what's in `role.manager` with the ID of your `Heist Manager` role.
3. OPTIONAL - Change what's in `checks.bal` into a boolean ( `true` or `false` ) to check balance beforehand.
4. OPTIONAL - Change what's in `msg.reaction` into a unicode emoji or some animated emoji to react on the heist message.

## Modifying
These things below are variables you would need to change if you wanna replace the default heist message so make sure you do something to them like what I did in the code.
- `{get;role.heist}` — Your `Heist Ping` role.
- `{get;role.manager}` — Your `Heist Manager` role.
- `{get;user}` — The heist sponsor id.
- `{get;amount}` — The specified amount.

## Credits
- [NumberFormatter](../../Snippets/JaM-NumberFormatter) - used as-is.
- [ActionHelp](../../Snippets/Deano-ActionHelp) - with a 'lil touch.
