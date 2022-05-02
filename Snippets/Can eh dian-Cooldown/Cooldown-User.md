```
// replace the {responder.text} at the bottom of the script (line 23) with your code and read the note (line 19+20)
// replace 'testing' with the name of your command
{=commandName;testing}
// replace '5m' with the cooldown time you want for your action
{=cooldownTime;5m}

// do not touch anything in the {if}'s below unless you want to change the cooldown message which is on line 14
{if;{catch;{time;{$cooldownTime}};err};==;err;{return;{responder.error;The creator of the action has input an improper time as a cooldownTime. \[Click Here\](https://docs.atlas.bot/tags/global#time-formattime) for valid time inputs}}}
{=cooldownArr;{or;{store.get;{$commandName}_cooldowns};{[]}}}
{if;{$cooldownArr};includes;{user.id};
    {=user;{split;{find;{$cooldownArr};/({user.id}\-\d+)/;1};-}}
    {=userCdTime;{$user.1}}
    {if;{$userCdTime};>;{time};
        {return;{responder.error;You are on cooldown, you can use this command {time format=relative_time;{$userCdTime}}}};
        {=cooldownArr;{catch;{split;{replace;{join;{$cooldownArr};\;};/{user.id}\-\d+\;?/g;};\;};err}}
        {if;{$cooldownArr};==;err;{=cooldownArr;{[]}}}
    }
}
// keep the 2 lines of code below (lines 21 + 22) together with your output if you want the cooldown to only trigger when a user succesfully uses the command
// otherwise leave it just under the `{if}` above
{=cdErr;{catch;{store.set;{$commandName}_cooldowns;{push return;{$cooldownArr};{user.id}-{time;{$cooldownTime}}}};err}}
{if;{$cdErr};==;err;{=firstItem;{shift;{$cooldownArr}}}{store.set;{$commandName}_cooldowns;{push;{$cooldownArr};{user.id}-{time;{$cooldownTime}}}}}
{responder.text;wow look at you, you ran the command correctly}
```
