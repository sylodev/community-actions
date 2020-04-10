**Note:** This snippet will *only* format whole numbers / integers (I.E. `718105` or `9482754`), not floats (I.E. `4291017.0417`).

**Instructions:** Paste code into the action and replace `NUMBER_HERE` with the number or tag containing the number to be formatted.

**Code:** 
```
{replace;NUMBER_HERE;(\d)(?=(\d\d\d)+$);$1,}
```