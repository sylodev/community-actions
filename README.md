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

## Requirements for contributing to this repository
* If your action is a command and has subcommands or any kind of {args} usage, you must include a help menu that shows how your action is used.
    * To add onto this, it **must** be callable through both `a!<command trigger>` (on its own) and `a!<command trigger> help`.
* If you make a pull request comprised of multiple `.action` files (hereby referred to as a superaction), you must put these into their own folder (following the file naming format below, just excluding the `.action` suffix) and include a `README.md` on what your superaction does and if it requires any special "setup". For an example, see [JaMcSu's "Advanced Auth"](https://github.com/doddsy/atlas-custom-actions/tree/master/Moderation/JaMcSu-AdvancedAuth).

### File Naming Format
All action files should follow the naming format: ```AuthorName-ActionName.action```
For example: ```JaMcSu-Math.action```

----------

#### Current Repository Moderators
* doddsy - node#2153 (Atlas Support Staff)
* JaMcSu - JaMcSu#8608 (Atlas Support Staff)
* Cykreet - Cykreet#5758 (Atlas Support Staff)
