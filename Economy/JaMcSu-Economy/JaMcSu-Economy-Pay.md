**NOTE:** The reason this command is restricted to Administrators/Moderators is because users can pay themselves, effectively doubling their balance. It is highly recommended that you keep these restrictions.

**Command Name:**
`a!pay`

**Bot Response:**
```{set;NewPBal;{math;{perget;{user.mention}_Balance}-{args;2}}}{set;NewRBal;{math;{perget;{args;1}_Balance}+{args;2}}}{perset;{user.mention}_Balance;{get;NewPBal}}{perset;{args;1}_Balance;{get;NewRBal}}{a!advancedembed;--title="Transaction Receipt";--description="Sent :economy_gem: `{args;2}` Gems from {user.mention} to {args;1}";--footer="Transaction completed by: {user.tag}";--timestamp}```

**Command Description:**
Send money to other users.

**Usage:**
`a!pay <user> <amount>`

**Example:**
`a!pay @JaMcSu 10`

**Recommended Settings:**
* Exempt Roles - Equivalent of: (Administrator or Moderator)
