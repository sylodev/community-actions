# Atlas Custom Actions Repository
Welcome to the Atlas custom actions repository. This repository serves as a way to upload and download awesome Atlas actions made by the community. While this service *is* recognised by the [Atlas Bot](https://atlasbot.xyz/) staff team, it *does not* explicitly belong to them. Even though the moderators of this repository screen all actions submitted for malicious content, a few may slip through the cracks. Understand that you take full responsibility of any damages incurred by importing any action files from this source.

## Importing Actions From This Repository
If you're interested in importing one of the custom actions found within our repository into your guild, heres how to do it.
* Navigate the repository files and find the action file you want to import.
* Open the action file and right click **`Raw`**.
* Click `Save link as` and save the file somewhere you will remember!
* Navigate to the [dashboard](https://atlasbot.xyz/), find the actions page of your guild and click the `Import` button.
* In the window that appears, navigate to where you saved the file and upload it.

## Contributing Actions to This Repository
Have an awesome action you want to share? Heres how to get it on this repository for everyone to see.
* Fork this repository via the **`Fork`** button in the top-right of the screen.
* Select your action from the actions list on your [dashboard](https://atlasbot.xyz/).
* Click the `Export` button.
* Rename your action file in correspondence to the **File Naming Format** found at the bottom of this page.
* Navigate to the appropriate subcategory for your action (I.E. Fun folder for a dice-roll action.) and click **`Upload files`**.
* Select your action file and commit the changes to your fork.
* Create a pull request and wait for it to be approved by the repository moderators.

## Guidelines for Contributing
* All uploaded actions *must* be submitted in fluent, understandable English. Any pull requests that are made in a language other than Enlgish will be automatically denied.
* If your action is a command that contains *multiple* subcommands, you must include an embedded help menu that shows how your action is used which **must** be callable through both `a!<command trigger>` (on its own) and the `a!<command trigger> help` subcommand. Alternatively, if you wish for no help embed to be posted upon `a!<command trigger>`, posting a message directing you to the help embed is also acceptable.
   * If your action changes its output based *exclusively* on an `{args}` input and *does not* contain multiple subcommands, you are exempt from this guildline.
* If you make a pull request comprised of multiple `.action` files (hereby referred to as a superaction), you must put these into their own folder and include a `README.md` on what your superaction does and if it requires any special setup. See [AdvancedAuth](https://github.com/doddsy/atlas-custom-actions/tree/master/Moderation/JaMcSu-AdvancedAuth) for an example.
* If your action (or any action files comprising a superaction) requires end-user input to function such as a specific channel name or ID, message ID, username or ID, etc., to contribute to ease of use, you must declare variables at the beginning of your action code with a `{note}` tag explaining what the information will be used for so the end-user can populate it correctly. See [here](https://i.imgur.com/dVldQxo.png) for an example.

## File Naming Format
* **All superaction folders should follow the following naming format:** ```AuthorName-SuperActionName```
    * For example: ```JaMcSu-AdvancedAuth```
* **All action files within a superaction should follow the naming format:** ```AuthorName-SuperActionName-ActionName.action```
    * For example: ```JaMcSu-AntiPing-Command.action```
* **All standalone action files should follow the naming format:** ```AuthorName-ActionName.action```
    * For example: ```JaMcSu-Math.action```

* **If multiple people contributed to an action's development, the other author(s) name should be appended to the first author's name:** ```Author1Name-Author2Name-Author3Name.action```
    * For example: ```doddsy-JaMcSu-Cykreet-Example.action```

----------

#### Current Repository Moderators
* doddsy - node#2153 (Atlas Support Staff)
* JaMcSu - JaMcSu#8608 (Atlas Support Staff)
* Cykreet - Cykreet#5758 (Atlas Support Staff)
