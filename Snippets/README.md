# What Are Snippets?
Snippets are small pieces of Atlas' TagScript code that, by themselves, do not make up a functional action. They are usually under 512 characters and can be copy/pasted into an existing action seamlessly by a semi-competent person who knows what they are doing. There is no special file format for uploading code snippets, see [Upload Requirements](https://github.com/atlasbot/community-actions/Snippets#upload-requirements) for more detailed information on how to properly contribute snippets.

## How To

### Integrate Snippets From This Repository Into Your Action
* In this repository, navigate to the snippet you want to integrate into your own action.
* Find and copy the **Code** to your clipboard.
* Navigate to the Atlas dashboard, find the Actions plugin, and select the action you want to integrate into.
* Scroll down to the bottom of the page until you find the field titled ![Script One](https://i.imgur.com/RONF7h2.png).
* Follow any special **Instructions** on the snippet page if any.

### Contribute Snippets to This Repository
* Fork this repository via the ![Fork](https://i.imgur.com/oazJQxh.png) button located in the top-right corner of this repository.
* In your fork, navigate to the **Snippets** folder.
* Create your snippet files in correspondence to the **[Folder Format Requirements](https://github.com/atlasbot/community-actions/Snippets#folder-format-requirements)** found at the bottom of this page.
* Commit the changes to your fork.
* Create a pull request and wait for it to be merged by the repository moderators.

## Upload Requirements
* All snippets must be uploaded in Markdown (`.md`) using the template found [here](https://pastebin.com/raw/upQpJk0q). Any pull requests in text formats other than Markdown will result in said pull request being automatically closed.
* Snippets belong in the [Snippets](https://github.com/atlasbot/community-actions/Snippets) folder only using the following [Folder Format Requirements](https://github.com/atlasbot/community-actions/Snippets#folder-format-requirements). Any snippets outside of this folder are not allowed and will be [re]moved.
* As detailed in the [Folder Format Requirements](https://github.com/atlasbot/community-actions/Snippets#folder-format-requirements), if your snippet file supports multiple "versions" or "variations" of modified code to achieve different outcomes, you must follow the **multiple-snippet** folder format requirement which has the added step of including a `README.md` in the base folder that explains the difference between each "version" or "variant" of your snippet.

## Folder Format Requirements
* **All single-snippet files should adhere to the following naming format:**
>**Folder Name:**    
>`AuthorName-SnippetName`    
>**Folder Contents:**    
>`SnippetName.md`
* **All multiple-snippet files should adhere to the following naming format:**
>**Folder Name:**    
>`AuthorName-SnippetName`    
>**Folder Contents:**    
>`SnippetName-SnippetSubName.md`      
>`...`    
>`README.md`
* **If multiple people contributed to a snippet's development, the other author(s) name should be appended to the original author's name:**
>`AuthorName-AuthorName-AuthorName-SnippetName`
