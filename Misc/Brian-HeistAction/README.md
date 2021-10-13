# HeistAction
A standalone action that allows you to manage heist events in your discord server.

## Features
- **Customizable** - Customize the heist message however you want. Either using embeds or a normal one, it's up to you actually.
- **Prompting** - Check their balance first if all required arguments are present and correct. This is optional.

## Notes
This action however, depends on another bot, Dank Memer. This allows us on prompting for the sponsor's balance.

## Modifying
You can find these tags within the code, especially down the code which is the heist message. 
- `{get;heist_ping}` — Your `Heist Ping` role.
- `{get;user}` — The heist sponsor id.
- `{get;amount}` — The specified amount.

## Credits
- [NumberFormatter](../../Snippets/JaM-NumberFormatter) - used as-is.
- [ActionHelp](../../Snippets/Deano-ActionHelp) - with a 'lil touch.