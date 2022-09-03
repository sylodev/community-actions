# Instructions
* Simply follow the instructions written from the comments of the code then you'll get yourself done.

## Code (1/2)
This code contains the common function(s) we need to prevent repetition of the same code that does the same operation. Paste this first then move on to the next part.
```js
// Replace INPUT_HERE with your custom or fixed input.
{=input;INPUT_HERE}
// Cuts off the decimals from the parameter, if ever it has. Do not modify unless you know what you entirely know what you are doing.
[#function;truncate;{=parameter}]
  {=value;{split;parameter;.}
  {return;{$value.0}}
[/function]
```

## Code (2/2)
This second half of the code contains not just one, but multiple ways to parse numbers if it meets it's respective conditions.

### #1: Floats  
In any other words, floats are numbers that may contain decimals. 
```js
{truncate;{$input}}
```

### #2: Shorthand Readables
Shorthand readables aren't valid numbers but which a person may infer as one due to the following common suffixes:
- `k` - thousands
- `m` - millions
- `b` - billions
```js
{truncate;{replace;{replace;{replace;{$input};/k$/g;e3};/m$/g;e6};/b$/g;e9}}
```
