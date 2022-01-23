**Code:**
```
{if;{and;
  {if;{args};!==;;true};
  {if;{args};!==;help;true}
};==;true;

	{note;Your custom action here}

;
	{a!ae;
		--title="**My Custom Action Help**";
		--description="This is what my action does";
		--field1name="Command Usage";
		--field1value="`{guild.prefix}myCustomCommand [help]` - Show the help dialog";
		--field2name="Example Usage";
		--field2value="`{guild.prefix}myCustomCommand <param>`";
	}
}
```
