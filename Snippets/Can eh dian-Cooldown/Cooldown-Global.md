```{note;replace "5m" with whatever time you want the action to be on cooldown for after a user uses the action.
utilizes {utils.parseTime} -> "Parses a 'human' time (e.g, "in 2h", "2h3m") to a timestamp compatible with {utils.time}"}
{set;cooldown;5m}
 
{note;replace testing with the name of the action}
{set;command_name;testing}


{if;{get;cooldown};!==;{perget;{get;command_name}_timer};
    {perset;{get;command_name}_timer;{get;cooldown}}
    {perset;{get;command_name}_cooldown}
}
{if;{utils.timestamp};<;{perget;{get;command_name}_cooldown};
    {channel.send;this command is on cooldown. Time remaining: `{utils.prettyms;{math;({perget;{get;command_name}_cooldown}-{utils.timestamp})}}`};
    {perset;{get;command_name}_cooldown;{utils.timestamp;{utils.parseTime;{get;cooldown}}}}
 
 
    {note;REPLACE ME WITH YOUR ACTION CODE, DO NOT TOUCH ANYTHING ABOVE (excluding the 2 {set}'s at the top of the action) UNLESS YOU KNOW WHAT YOU'RE DOING (or want to change the cooldown message above this line)}


}```