**Action Name:**
`a!verify`

**Action Type:**
Command

**Action Content:**
`{if;{args;1};===;{perget;{user.id}_Key};{user.removerole;Unverified};{user.send;Incorrect key entered. Please try again. If you believe this is a mistake, please contact a staff member.}}`

**Usage:**
`a!verify <code>`

**Recommended Settings:**
* Reply (Direct Message)
* Fall back to invocation channel - OFF
* Delete invocation message - ON
* Role Whitelist - Unverified
* Channel Whitelist - #verify
