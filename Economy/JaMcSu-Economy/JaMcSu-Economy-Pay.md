**WARNING** Users can pay themselves with this command, doubling their balance. This command is not recommended to be used at all!

**Command Name:**
`a!pay`

**Bot Response:**
```{set;NewPBal;{math;{perget;{user.mention}_Balance}-{args;2}}}{set;NewRBal;{math;{perget;{args;1}_Balance}+{args;2}}}{perset;{user.mention}_Balance;{get;NewPBal}}{perset;{args;1}_Balance;{get;NewRBal}}{a!advancedembed;--title="Transaction Receipt";--description="Sent :economy_gem: `{args;2}` Gems from {user.mention} to {args;1}";--timestamp}```

**Command Description:**
Send money to other users.

**Usage:**
`a!pay <user> <amount>`

**Example:**
`a!pay @JaMcSu 10`

**Recommended Settings:**
* Exempt Roles - `🏦 Account Holder`
