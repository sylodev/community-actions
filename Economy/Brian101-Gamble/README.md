<div align=center>

# Gamble
A simple gamble game made for [Atlas](https://atlasbot.xyz)!

</div>

### Setup

* Save those actions on your computer
* Import Them using your dashboard
	* In order for users to use those commands, make sure you whitelist them (and yourself of course) using the following command:
		* `a!whitelist <me | userID>`
		* This will create a key on your persistent storage with the following format: 
		Key: `{user.id}_currencyData`
		Data: 
		```
		Pocket: 0
		Vault: 0
		Whitelisted: true
		```
		* Whitelisting users will set their pocket and vault to a random number between 1 and 100,000 coins.
* Voila! You can now use these commands.


### Command Usage
Name | Definition | Usage
--- | --- | ---
whitelist | allow certain users to use these commands | `a!whitelist <me \| userID>`
balance | checks your or someone else's balance. | `a!balance <optionalUser>`
give | gives other user some coins | `a!give <amount> <user>`
withdraw | withdraw some coins from your bank | `a!withdraw <all \| max \| amount>`
deposit | deposit some coins to your bank | `a!deposit <all \| max \| amount>`
gamble | gamble your coins | `a!gamble <amount \| all \| max \| half>`


### Credits
* JaM#8608 - [Number Formatter](https://github.com/atlasbot/community-actions/tree/master/Snippets/JaM3141-NumberFormatter)
