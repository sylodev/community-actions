```{note;replace "5m" with whatever time you want the action to be on cooldown for after a user uses the action.
utilizes {utils.parseTime} -> "Parses a 'human' time (e.g, "in 2h", "2h3m") to a timestamp compatible with {utils.time}"}
{set;cooldown;5m}
 
{note;replace testing with the name of the action}
{set;command_name;testing}
 
 
{note;if the cooldown get's changed, instead of waiting for the original cooldown time it reset's the cooldown's}
{if;{get;cooldown};!==;{perget;{get;command_name}_timer};
    {perset;{get;command_name}_timer;{get;cooldown}}
    {perset;{get;command_name}_cooldown}
}
{set;time_cd;{utils.timestamp}}
{note;checks if your id has a cooldown associated with your ID or not, and if you do it checks if your cooldown is over}
{if;{perget;{get;command_name}_cooldown};includes;{user.id};
    {set;cooldown_time;{find;{perget;{get;command_name}_cooldown};/{user.id}-(\d+)/;1}}
    {if;{get;time_cd};>;{get;cooldown_time};
        {set;cooldown_time;over}
        {perset;{get;command_name}_cooldown;{replace;{perget;{get;command_name}_cooldown};{user.id}-\d+}}
    };
    {set;cooldown_time;over}
}
{if;{get;cooldown_time};!==;over;
    {channel.send;this command is on cooldown. Time remaining: `{utils.prettyMs;{math;({find;{perget;{get;command_name}_cooldown};/{user.id}\-(\d+)/;1}-{get;time_cd})}}`};
    


    {note;REPLACE ME WITH YOUR ACTION CODE, DO NOT TOUCH ANYTHING ABOVE OR BELOW (excluding the 2 {set}'s at the top of the action) UNLESS YOU KNOW WHAT YOU'RE DOING (or want to change the cooldown message above this line)}



    {set;error_cd;{catch;{perset;{get;command_name}_cooldown;{perget;{get;command_name}_cooldown} {user.id}-{utils.timestamp;{utils.parseTime;{get;cooldown}}}};error}}
    {if;{get;error_cd};===;error;{perset;{get;command_name}_cooldown;{find;{perget;{get;command_name}_cooldown};/^(?:\d+\-\d+)(.+)/;1} {user.id}-{utils.timestamp;{utils.parseTime;{get;cooldown}}}}}
}```