A set of moderation wrappers that customizes the DM sent to the target, as well as adds features.

The goal of the custom DM is to provide the target with aditional information about the punishment, while also anonymizing the action to protect the acting moderator from any targeting they may recive. 

The default message is `You have been [action] in {guild.name} for <reason>.`

These wrappers maintian the function of the `--nodm` flag, so if you would still like to not have the target notified of the action you can add the flag.

The commands `a!ban`, `a!kick`, and `a!purgeban` retain all original functions with only the new user DM.

The following command have been given additional features:

`a!tempban`
The target DM will include the length of the punishment that was specified (s/m/h/d/w/y).

`a!warn`
The target DM will include the number of warnings.

`a!mute`
An aditional punishment duration has been added. `na` mutes the user indefinetly.  
The target DM will include the length of the punishment that was specified (s/m/h/d/w/y/na).
