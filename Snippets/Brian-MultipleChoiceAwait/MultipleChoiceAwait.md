**Instructions**
- Replace `TIME` with a number (in seconds) up to 60 for the `{channel.awaitMessage}` timeout.
- Replace `OPTION_#` with the options (in lowercase) you wish.
- Replace `DO_THIS` with tags you want to execute if they select that option.
- You can delete `...` and add as many similar `{if}` statements as you want if you want more options.
- Replace `OPTIONS_ARE_WRONG` with tags you want to run if none of the options were chosen.
- Whenever you add new options, add it option on our `{find}` tag located on our last
  `{if}` statement separated by a `|` pipeline.

**Code**
```
{set;awaited;{lower;{channel.awaitMessage;{user.id};TIME}}}

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
