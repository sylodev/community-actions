# Status

Command to send a status message pertaining a specified server with a status type.

## Usage

1) Edit the listed server name using the provided example. (More can be added if necessary)
2) Fill in the server list with your abbreviations in the invalid server name code block. I.E.:
```
[#if;{$server};!includes;{option;server_name}]
  {responder.embed;{{
  "title": "INVALID SERVER NAME!",
  "color": 460551,
  "description": "Use any of the following statuses, case-sensitive, for the command.",
  "fields": [
    {
      "name": "Types",
      "value": "• ark1\n• ark2\n• ark3\n• valheim\n• isle"
    }
  ]
  }}}
  {responder.ephemeral}
  {return}
[/if]
```
2) In your server, run the command and fill in the parameters as needed.