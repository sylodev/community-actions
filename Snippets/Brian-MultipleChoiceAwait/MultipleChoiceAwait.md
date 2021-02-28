**Instructions**
- Replace `TIME` with a number (in seconds) up to 60 for the timeout.
- Replace `OPTION_#` with the options you wish.
- Replace `DO_THIS` with tags you want to execute.
- The `...` is the part you wanna extend so you can add another `{if}` statement in it.
- Replace `OPTIONS_ARE_WRONG` with tags you want to run if none of the options were met.\
- Whenever you add new options, add the option on our `{find}` tag located to our last
  `{if}` statement separated by a `|` pipeline.

**Code**
```
{set;awaited;{channel.awaitMessage;{user.id};TIME}}

{if;{get;awaited};===;OPTION_1;
  DO_THIS
}
{if;{get;awaited};===;OPTION_2;
  DO_THIS
}
...

{if;{find;{get;awaited};^(OPTION_1|OPTION_2)$};===;;
  OPTIONS_ARE_WRONG
}
```
