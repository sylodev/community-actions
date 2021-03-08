**This version is reserved for validating the following:** 
* User Mentions — [`@JustBrian`](https://www.youtube.com/watch?v=dQw4w9WgXcQ)
* User Names — `JustBrian`
* User Tags — `JustBrian#9793`
* User IDs — `605419747361947649`

**Instructions:**
* Replace `DO_THIS` with the code you want to run if validation is successful.
* Replace `ELSE_DO_THIS` with the code you want to run if validation is invalid.
* Optional — Replace `{args}` with anything like the `{get}` tag.

**Code**
```sh
{if;{utils.isSnowflake;{user.id;{args}}};
  DO_THIS
  ;
  ELSE_DO_THIS
}
```
