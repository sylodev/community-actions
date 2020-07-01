Action that automatically transcripts tickets upon closing. Wraps the `ticket close` subcommand. It is important to note that this action **will not function properly** if you have the `Direct-message response` option enabled since it relies on a message sent in the ticket channel. You must have this option disabled!

It is also important to note that Discord requires bots to delete user information no longer than 30 days after receiving it. This means transcripts will be automatically deleted from Atlas' servers 30 days after being created. Keep this in mind when using this action.
