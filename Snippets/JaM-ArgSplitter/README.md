# ArgSplitter
Small snippet of code that enables multi-word arguments delimited by pipes (`|`) and parses them into single arguments. Keep in mind there are different versions for different numbers of arguments. The 2-argument version will *only* accept 2 arguments. No more, no less. The same goes for 3-arg, 4-arg, etc. versions.

**Example:** `a!command argument one here|argument two here|argument three here`
* `{get;arg1}` - Output: `argument one here`
* `{get;arg2}` - Output: `argument two here`
* `{get;arg3}` - Output: `argument three here`