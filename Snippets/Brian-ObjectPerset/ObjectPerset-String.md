# Note
You're currently viewing the **Numbered** version of this snippet so this version obviously parses numbered keys for your perset.

## Instructions (Base Code)
- Replace every instance of `PERSET` with the name of your perset.
- Replace all `KEY` with the key in your perset.

## Example Perset
> **Perset Name:** `user`
```yaml
Name: Joe
Job: Clown
```

### Code (Fetching)
> **This code fetches the `Name` key from our `user` perset.**
```sh
{set;name;{find;{perget;fruits};Name: (\w+)}}}
{channel.send;User Name: {get;name}}
```
> **Base Code**
```sh
{set;key;{find;PERSET;KEY: (\w+)}}}
{channel.send;Key Value: {get;key}}
```



### Code (Overwriting)
> **This code overwrites the `Job` key from our `user` perset.**
```sh
{set;new_value;Star}
{set;job;{find;{perget;fruits};Job: (\d+)}}

{perset;user;{find;{perget;fruits};Job: (\w+);Job: {get;new_value}}}
{set;job;{find;{perget;fruits};Job: (\d+)}}

{channel.send;New Job: {get;job}}
```
> **Base Code — Replace `NEW_VALUE` with a numerical value.**
```sh
{set;new_value;NEW_VALUE}
{set;key;{find;{perget;PERSET};KEY: (\w+)}}

{perset;PERSET;{find;{perget;PERSET};KEY: (\w+);KEY: {get;new_value}}}
{set;key;{find;{perget;PERSET};KEY: (\w+)}}

{channel.send;New Key Value: {get;key}}
```
