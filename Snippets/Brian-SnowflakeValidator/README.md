# Snowflake Validator
This snippet parses user arguments into a valid Discord snowflake.

**Examples:**
> **Legend**\
`<Valid ...>` - means the statement is true\
`<Invalid ...>` - means the statement is invalid or false

* **Input:** `a!validate @user`\
	**Output:** `<Valid User>`

* **Input:** `a!validate #channel`\
	**Output:** `<Valid Channel>`

* **Input:** `a!validate @role`\
	**Output:** `<Valid Role>`

* **Input:** `a!validate asdnfhbn`\
	**Output:** `<Invalid User/Channel/Role>`
