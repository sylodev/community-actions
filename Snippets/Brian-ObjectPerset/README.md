# ObjectPerset
An easy way of storing object-structured persets into your persistent storage.

## Disclaimer
This isn't a good way of bypassing the 500 perset limit per guild. It's only intended if you're working with user-specific data for your server or, storing objects for a specific item or info for example.

## Notice
Please ensure you know how most of the tags and regular expressions work in this snippet because it's not a very simple piece of code you see from other snippets. It's quite complicated (if you're a beginner) and only a few people might understand how things work in this snippet. Please read the [docs related to tags](https://atlas.bot/documentation/tags) first before using this snippet.

## Structure
The snippet uses and/or outputs a given perset into a 1st-level list in `yaml` format so let's assume you already have a perset with the following format:
```yaml
NumberedKey: 420
AnotherKey: value
Hotel: Trivago
```

## Versions
Currently, ObjectPerset only has 2 versions and those are:
- [**Number**](./ObjectPerset-Number.md) - fetch, overwrite and do math operations with keys. 
- [**String**](./ObjectPerset-String.md) - fetch and overwrite keys only.
