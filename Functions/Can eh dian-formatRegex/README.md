**Description:** takes a regular expression and formats it to work with atlas
**Usage:** `{formatRegex;RegExp}`

**Code:**
```[#function;formatRegex;{=fregex_input}]
  {return;{replace;{replace;{$fregex_input};/\\\\([$\}\{\;\\\]\\\[#\\\/\\\\])/g;\\\\\\$1};/([^\\\\])(\{[^\}]+)(\})/g;$1\\$2\\$3}}
[/function]```