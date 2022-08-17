# What Are Functions?
[Functions](https://docs.atlas.bot/scripts/functions) are part of Atlas' Pella code that, by themselves, do not typically make up a functional action. They tend to be under 512 characters and can be pasted into an existing action seamlessly by a semi-competent person who knows what they are doing. See [Upload Requirements](https://github.com/sylo-digital/community-actions/tree/master/Functions#upload-requirements) for more detailed information on how to properly contribute functions.

## How To

### Integrate Functions From This Repository Into Your Action
* In this repository, navigate to the snippet you want to integrate into your action.
* Find and copy the **Code** to your clipboard.
* Navigate to the Atlas dashboard, find the Actions page, and select the action you want to integrate into.
* Follow any special **Instructions** on the snippet page if any.

### Contribute Functions to This Repository
* Fork this repository via the ![Fork](https://micro.sylo.digital/f/7Vdn7l.png) button located in the top-right corner of this repository.
* In your fork, navigate to the **Functions** folder.
* Create your files in correspondence to the **[Folder Format Requirements](https://github.com/sylo-digital/community-actions/tree/master/Functions#folder-format-requirements)** found at the bottom of this page.
* Commit the changes to your fork.
* Create a pull request and wait for it to be merged by the repository moderators.

## Upload Requirements
* All functions must be uploaded in Markdown (`.md`) using the template found [here](https://pastebin.com/raw/h72GqXN1). Any pull requests in text formats other than Markdown will result in said pull request being automatically closed.
* All functions must return a with a unique output variable.
* Functions belong in the [Functions](https://github.com/sylo-digital/community-actions/tree/master/Functions) folder and must follow the [Folder Format Requirements](https://github.com/sylo-digital/community-actions/tree/master/Functions#folder-format-requirements). Any functions outside of this folder are not allowed and will be [re]moved.
* As detailed in the [Folder Format Requirements](https://github.com/sylo-digital/community-actions/tree/master/Functions#folder-format-requirements), if your function file supports multiple "versions" or "variations" of modified code to achieve different outcomes, you must follow the **multiple-format** folder requirements which have the added step of including a `README.md` in the base folder that explains the difference between each "version" or "variant" of your function.

## Folder Format Requirements
* **All single-function files should adhere to the following naming format:**
>**Folder Name:**    
>`AuthorName-FunctionName`    
>**Folder Contents:**    
>`FunctionName.md`
* **All multiple-format files should adhere to the following naming format:**
>**Folder Name:**    
>`AuthorName-FunctionName`    
>**Folder Contents:**    
>`FunctionName-FormatName.md`      
>`...`    
>`README.md`
* **If multiple people contributed to a function's development, the other author(s) name should be appended to the original author's name:**
>`AuthorName-AuthorName-AuthorName-FunctionName`
