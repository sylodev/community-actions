```
// replace the {responder.text} at the bottom of the script (line 15) with your code and read the note (line 13)
// replace 'testing' with the name of your command
{=commandName;testing}
// replace '5m' with the cooldown time you want for your action
{=cooldownTime;5m}

// do not touch anything in the {if}'s below unless you want to change the cooldown message which is on line 11
{=globalCooldownTime;{store.get;{$commandName}_cd}}
{if;{catch;{time;{$cooldownTime}};err};==;err;{return;{responder.error;The creator of the action has input an improper time as a cooldownTime. \[Click Here\](https://docs.atlas.bot/tags/global#time-formattime) for valid time inputs}}}
{if;{$globalCooldownTime};>;{time};
  {return;{responder.error;This command is on cooldown, it can be used again {time format=relative_time;{$globalCooldownTime}}}}
}
// keep the {store} tag together with your output if you want the cooldown to only trigger when a user succesfully uses the command, otherwise leave it just under the `{if}` above
{store.set;{$commandName}_cd;{time;{$cooldownTime}}}
{responder.text;wow you ran the command correctly}
```
