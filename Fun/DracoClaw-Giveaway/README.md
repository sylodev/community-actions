An advanced giveaway system with many configurable options.

This ActionPack contains **6** actions.

All commands Required Permissions are set to `Manage Messages`.

__Commands__:
`/giveaway start` - Create a giveaway with customizable conditions.
    ```
    channel - The channel to run the giveaway.
    prize - What is being given away.
    duration - How long the giveaway should run for. `s/m/h/d/w/mo/y`
    winners - How many winners.
    host? - Who is hosting the giveaway.
    ping? - A role to ping when the giveaway starts.
    whitelist? - Roles the user must have to enter. `@Role_1 | @Role_2`
    blacklist? - Prevent users with these roles from entering. `@Role_1 | @Role_2`
    level_required? - Minimum chat level to enter.
    account_age? - How old the users account must be to enter. `s/m/h/d/w/mo/y`
    join_age? - How long the user must be in the server to enter. `s/m/h/d/w/mo/y`
    max_entries? - The maximum amount of users allowed to enter. Default=300
    multipliers? - Roles that grant additional entries. `@Role_1 x2 | @Role_2 x3`
    multi_highest? - How to count user multipliers. `true=Top Multiplier | false=Add Total`
    template? - Use a predefined conditions template.
    ```
`/giveaway end` - End a giveaway before its set endtime.
    ```
    message_id - ID of the giveaway to end.
    ```
`/giveaway reroll` - Re-roll a giveaway that has ended. Must be within 7 days since ending.
    ```
    message_id - ID of the giveaway to re-roll.
    winners? - How many winners to re-roll.
    ```
`/giveaway template` - Run by itself to set a template with the values specified via the dashboard.
    ```
    list? - Outputs the full template JSON when true.
    ```
__Interval__:
`*/2 * * * *` - Runs every two minutes. Ends pending giveaways, as well as clears old ones.