# ArgSplitter
Small snippet of code that enables multi-word arguments delimited by pipes, commas, or forward-slashes (`|`, `,`, `/`) and parses them into single arguments. Keep in mind there are different versions for different numbers of arguments. The 2-argument version will *only* accept 2 arguments. No more, no less. The 3-argument version will *only* accept 3 arguments. No more, no less. The same goes for 4-arg, 5-arg, etc. versions.

It is also important to note that using URLs with this snippet can screw with the accurate detection of where the arguments are split because URLs contains forward-slashes (`/`) which *also* count as a valid separator. There ***is*** a fix to this; however if you're not familiar with regex, it may not be immediately obvious to you. Feel free to ask in our support server for this fix if you plan to use this snippet in conjuction with URLs. Do note that using this fix will only allow pipes and commas (`|`, `,`) as valid separators, forward-slashes (`/`) cannot be used.

**Example:** `a!command argument one here|argument two here|argument three here`
* `{get;arg1}` - Output: `argument one here`
* `{get;arg2}` - Output: `argument two here`
* `{get;arg3}` - Output: `argument three here`
