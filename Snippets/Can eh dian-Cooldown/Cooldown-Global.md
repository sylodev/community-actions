```// replace 'testing' with the name of your command
{=commandName;testing}
// replace '5m' with the cooldown time you want for your action
{=cooldownTime;5m}

// do not touch anything in the {if}'s below unless you want to change the cooldown message which is on line 9
{if;{catch;{time;{$cooldownTime}};err};==;err;{return;{responder.text;The creator of the action has input an improper time as a cooldownTime. check out https://docs.atlas.bot/tags/global#time-formattime for valid time inputs}}}
{if;{store.get;{$commandName}_cd};>;{time};
  {return;{responder.text;This command is on cooldown, it can be used again {time format=relative_time;{store.get;{$commandName}_cd}}}}
}

// keep the {store} tag together with your output if you want the cooldown to only trigger when a user succesfully uses the command, otherwise leave it just under the `{if}` above
{store.set;{$commandName}_cd;{time;{$cooldownTime}}}
{responder.text;wow you ran the command correctly}```