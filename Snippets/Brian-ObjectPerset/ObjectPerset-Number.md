# Note
You're currently viewing the **Numbered** version of this snippet so this version obviously parses numbered keys for your perset.

## Instructions (Base Code)
- Replace every instance of `PERSET` with the name of your perset.
- Replace all `KEY` with the key in your perset.
- 

## Example Perset
> **Perset Name:** `fruits`
```yaml
Avocado: 26
Ponkan: 15
Apple: 42
```

### Code (Fetching)
> **This code fetches the `Avocado` key from our `fruits` perset.**
```sh
{set;avocado;{find;{perget;fruits};Avocado: (\d+)}}}
{channel.send;Avocado Count: {get;avocado}}
```
> **Base Code**
```sh
{set;key;{find;PERSET;KEY: (\d+)}}}
{channel.send;Key Count: {get;key}}
```



### Code (Overwriting)
> **This code overwrites the `Ponkan` key from our `fruits` perset.**
```sh
{set;new_value;123}
{set;ponkan;{find;{perget;fruits};Ponkan: (\d+)}}

{perset;fruits;{find;{perget;fruits};Ponkan: (\d+);Ponkan: {get;new_value}}}
{set;ponkan;{find;{perget;fruits};Ponkan: (\d+)}}

{channel.send;New Ponkan Count: {get;ponkan}}
```
> **Base Code — Replace `NEW_VALUE` with a numerical value.**
```sh
{set;new_value;NEW_VALUE}
{set;key;{find;{perget;PERSET};KEY: (\d+)}}

{perset;PERSET;{find;{perget;PERSET};KEY: (\d+);KEY: {get;new_value}}}
{set;key;{find;{perget;PERSET};KEY: (\d+)}}

{channel.send;New Key Count: {get;key}}
```



### Code (Math Operations)
> **This code does `{math}`s on our `Apple` key from our `fruits` perset.**
```sh
{set;add_value;123}
{set;apple;{find;{perget;fruits};Apple: (\d+)}}

{perset;fruits;{find;{perget;fruits};Apple: (\d+);Apple: {math;{get;apple}+{get;add_value}}}}
{set;apple;{find;{perget;fruits};Apple: (\d+)}}

{channel.send;New Apple Count: {get;apple}}
```
> **Base Code — Replace `ADD_VALUE` with a numerical value.**
```sh
{set;add_value;ADD_VALUE}
{set;key;{find;{perget;PERSET};KEY: (\d+)}}

{perset;fruits;{find;{perget;PERSET};KEY: (\d+);KEY: {math;{get;key}+{get;add_value}}}}
{set;key;{find;{perget;PERSET};KEY: (\d+)}}

{channel.send;New Key Count: {get;key}}
```
