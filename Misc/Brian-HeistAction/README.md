# HeistAction
This action allows you to manage heist events in your discord server.

## Features
- **Validation** - Complex-ish checking of command arguments, no nested if's.
- **Checkers** - Check their balance first if all required parameters are present.
- **Customizable** - You can customize the message however you want.

## Instructions
The only things you should change are the `{set}` variables on top of the action code. These variables are only roles which should be pinged as you start an event.
1. Change `role.heist` with your `Heist Ping` role.
2. Change `role.manager` with your `Heist Manager` role.

## Modifying
These things below are the variables you would need to change if you wanna change the default heist message so make sure you do something to them like what I did in the code.
- `{get;role.heist}` — Our `Heist Ping` role.
- `{get;role.manager}` — Our `Heist Manager` role.
- `{get;user}` — The heist sponsor.
- `{get;amount}` — The given amount.

## Credits
- [NumberFormatter](https://github.com/sylo-digital/community-actions/tree/master/Snippets/JaM-NumberFormatter)