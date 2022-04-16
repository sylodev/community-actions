```// replace the {responder.text} at the bottom of the script (line 29) with your code and read the note (line 27)
// replace 'testing' with the name of your command
{=commandName;testing}
// replace '5m' with the cooldown time you want for your action
{=cooldownTime;5m}

// do not touch anything in the {if}'s below unless you want to change the cooldown message which is on line 23
{if;{catch;{time;{$cooldownTime}};err};==;err;{return;{responder.text;The creator of the action has input an improper time as a cooldownTime. check out https://docs.atlas.bot/tags/global#time-formattime for valid time inputs}}}
{=emptyArr;{[]}}
{if;{store.get;{$commandName}_cooldowns};
    {=arr;{store.get;{$commandName}_cooldowns}}
    {=user; }
    {for;{=info};{$arr};
        {=sInfo;{split;{$info};-}}
        {if;{$sInfo.1};>;{time};
            {push;{$emptyArr};{$sInfo.0}-{$sInfo.1}}
            {if;{$sInfo.0};==;{user.id};
                {=user;{$sInfo}}
            }
        }
    }
    {if;{$emptyArr};includes;{user.id};
        {return;{responder.text;You are on cooldown, you can use this command {time format=relative_time;{$user.1}}}}
    }
}

// keep the {store} tag together with your output if you want the cooldown to only trigger when a user succesfully uses the command, otherwise leave it just under the `{if}` above
{store.set;{$commandName}_cooldowns;{push return;{$emptyArr};{user.id}-{time;{$cooldownTime}}}}
{responder.text;wow look at you, you ran the command correctly}```
