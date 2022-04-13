# Atlas Community Actions Repository
Welcome to the **Atlas Community Actions Repository**, a public resource for users of the [Atlas](https://atlas.bot) Discord bot to share custom-made actions and snippets of code with others in the Atlas community. Although every attempt is made to scan all actions submitted to this repository for malicious content, we assume no responsibility for any damages incurred from importing content from this source into your server.

| WARNING: Folders marked as LEGACY are from the before the vX update. Working behavior may vary. |
| --- |

## How To
The following information is for actions only. For information on how to utilize snippets, see [here](https://github.com/sylo-digital/community-actions/tree/master/Snippets#what-are-snippets).

### Import Actions From This Repository Into Your Server
If you're interested in importing one of the custom actions found within our repository into your server, here's how to do it:
* Ensure that Atlas is in your server and has the proper permissions to send and read messages, moderate, etc. If it is not currently in your server, [click here](https://atlas.bot/get) to invite it now. If you have never used Atlas before you may be asked to login with your Discord account.
* Navigate to the [My Servers](https://atlas.bot/guilds) page and select the server you want to import the action into.
* Back on GitHub, navigate the repository files and find the action file you want to import.
* Open the action file and right click [![](https://micro.sylo.digital/f/0wUEjK.png)](https://www.youtube.com/watch?v=q5Dj5G1kaqI "It's Raw!")
* Click **Save link as** and save the file somewhere you will remember!
* Back on the Atlas dashboard, click on the **Actions** tab and click ![Import Action](https://micro.sylo.digital/f/VvL4FU.png).  
  This will open a prompt for you to select the `.action` file you just downloaded. Find it and upload it.
* Congratulations! The imported action should now show up in the **Actions** sidebar.

### Contribute Actions to This Repository

Have an awesome action you want to share? Here's how to get it on this repository for everyone to see. Before uploading your action, you might want to take a look at our **[Guidelines for Contributing](https://github.com/sylo-digital/community-actions#guidelines-for-contributing)** to see if it meets our standards.
* Fork this repository via the ![Fork](https://micro.sylo.digital/f/7Vdn7l.png) button located in the top-right corner of this repository.
* On the Atlas dashboard, select your action from the actions list on your [dashboard](https://atlas.bot/).  
  For Actions with multiple files, Action Packs, you can select multiple actions to export as a group.
* Click the ![Export Action](https://micro.sylo.digital/f/VxTrhm.png) button to save the `.action` file to your device.
* Rename your action file in correspondence to the **[Folder Format Requirements](https://github.com/sylo-digital/community-actions#folder-format-requirements)** found at the bottom of this page.
* Navigate to the appropriate subcategory for your action (I.E. Fun folder for a dice-roll action.) and click ![Add file](https://micro.sylo.digital/f/kX8Krb.png)
* Select your action file and commit the changes to your fork.
* Create a pull request and wait for it to be approved by the repository moderators.

## Guidelines for Contributing
**1.** - All uploaded actions  _must_  be submitted in fluent, understandable English. Any pull requests that are made in a language other than English or that contain excessive typos will be automatically closed.

**2.** - All submitted actions must be placed in a folder per the **[Folder Format Requirements](https://github.com/sylo-digital/community-actions#folder-format-requirements)** along with a `README.md` file with a short (or long) description of what the action does. If you make a pull request comprised of an `.actionpack` file include any special setup required in the README.

**4.** - If your action(pack) requires static end-user input to function such as a specific channel name or ID, message ID, user ID, etc., to contribute to ease of use, you must declare variables at the beginning of your action code with a `// note` explaining what the information will be used for so the end-user can populate it correctly. See [here](https://micro.sylo.digital/f/8XW4l3) for an example. You must also declare that there is end-user input required in your action(pack) README.

**5.** - Wrappers or aliases for existing Atlas commands do not meet our requirements for contributing. Any action that is submitted in which its sole purpose is to execute a native Atlas command under a disguised name will be automatically denied. The only exception to this guideline is if the wrapper adds a specific functionality to the execution of the command that is not available when running the native command alone.

## Folder Format Requirements
We impose restrictions on how files are uploaded and organized to keep the repository neat and tidy. Please remember to follow these requirements when you upload your action(pack)'s or it may be denied.

>**Folder Name:**    
>`AuthorName-ActionName`    
>**Folder Contents:**    
>`ActionName-TriggerType.action`
or
>`ActionName.actionpack`  
>`README.md`

* **If multiple people contributed to a action(pack)'s development, the other author(s) name should be appended to the original author's name:**
>`AuthorName-AuthorName-AuthorName-ActionName`
* **If the action(pack) takes advantage of the increased tag limits of Atlas Prime, or uses Prime only features, append a label:**
>`AuthorName-ActionName-Prime`
-----
#### Repository Moderators
All current moderators of this repository are Atlas staff members.
* [JaM3141](https://github.com/JaM3141) - [JaM#8608](https://discord.com/users/204045630836834305)
* [cykreet](https://github.com/cykreet) - [Cykreet#1083](https://discord.com/users/723483880291827732)
* [DracoClaw](https://github.com/DracoClaw) - [DracoClaw#0065](https://discord.com/users/341680387979870219)
