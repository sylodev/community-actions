# Note
You're currently viewing the **Numbered** version of this snippet so this version obviously parses numbered keys for your perset.

## Instructions
- Yes

## Example Perset
> **Perset Name:** `fruits`
```yaml
Avocado: 26
Ponkan: 15
Apple: 42
```

### Code (Fetching)
> **Base Code**
```sh
{set;volatile_key;{find;PERSET;KEY: (\d+)}}}
{channel.send;Volatile Key Count: {get;volatile_key}}
```
> **This code fetches the `Avocado` key from our `fruits` perset.**
```sh
{set;avocado;{find;{perget;fruits};Avocado: (\d+)}}}
{channel.send;Avocado Count: {get;avocado}}
```

### Code (Overwriting)
> **Base Code**
```sh
{set;new_value;NEW_VALUE}
{set;key;{find;{perget;PERSET};KEY: (\d+)}}

{perset;PERSET;{find;{perget;PERSET};KEY: (\d+);KEY: {get;new_value}}}
{set;key;{find;{perget;PERSET};KEY: (\d+)}}

{channel.send;New Key Count: {get;key}}
```
> **This code overwrites the `Ponkan` key from our `fruits` perset.**
```sh
{set;new_value;123}
{set;ponkan;{find;{perget;fruits};Ponkan: (\d+)}}

{perset;fruits;{find;{perget;fruits};Ponkan: (\d+);Ponkan: {get;new_value}}}
{set;ponkan;{find;{perget;fruits};Ponkan: (\d+)}}

{channel.send;New Ponkan Count: {get;ponkan}}
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
