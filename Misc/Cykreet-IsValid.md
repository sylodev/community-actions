**Command Name:**
`a!isvalid`

**Bot Response:** `{if;{args};!==;{user.username;{args}};{a!advancedembed;--color="#fc5858";--title="{args} is not a member in the server.";--timestamp}}
{if;{args};===;{user.username;{args}};{a!advancedembed;--color="#58fc78";--title="{user.tag;{args}} is a member in the server.";--timestamp}}`

**Command Description:**
Checks if the user specified is in the server
**(NOTE: Do not try and mention a person and this does not work with nicknames)**

**Usage:**
`a!isvalid <User's Name>`

**Recommended Settings:** None
