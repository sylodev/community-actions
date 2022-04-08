# NumberFormatter
A slice of TagScript that turns normal numbers (`1234567`) into formatted numbers (`1,234,567`).

**Examples:**
* Input: `{replace;420420420;(\d)(?=(\d\d\d)+$);$1,}`  
Output: `420,420,420`

* Input: `{set;Num;51246948}{replace;{get;Num};(\d)(?=(\d\d\d)+$);$1,}`  
Output: `51,246,948`

* Input: `{replace;100000000000000000000;(\d)(?=(\d\d\d)+$);$1,}`  
Output: `100,000,000,000,000,000,000`
