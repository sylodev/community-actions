**This version is reserved for validating the following:** 
* Role Names — `@Members`
* Role IDs — `123456`

**Instructions:**
* Replace `DO_THIS` with the code you want to run if validation is successful.
* Replace `ELSE_DO_THIS` with the code you want to run if validation is invalid.
* Optional — Replace `{args}` with anything like the `{get}` tag.

**Code**
```sh
{if;{utils.isSnowflake;{role.id;{args}}};
  DO_THIS
  ;
  ELSE_DO_THIS
}
```
