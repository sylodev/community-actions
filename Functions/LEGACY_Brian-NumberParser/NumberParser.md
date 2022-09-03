# Instructions
* Those are written within the code comments written directly above them. 

## Code (1/2)
This code contains the common function(s) we need to prevent repetition of the same code that does the same operation. Paste this first anywhere within your action's code then move on to the next part.
```js
// Replace INPUT_HERE with your custom or fixed input.
{=input;INPUT_HERE}

// This cuts off the decimals from the input if it ever has. Do not modify unless you entirely know what you are doing.
[#function;truncate;{=parameter}]
  {=parameter;{split;{$parameter};.}}
  {return;{$parameter.0}}
[/function]
```

## Code (2/2)
This second half of the code contains not just one, but multiple ways to parse numbers if it meets it's respective conditions.

### #1: Floats  
In any other words, floats are numbers that contain decimals. 
```js
{truncate;{$input}}
```

### #2: Shorthand Readables
Shorthand readables aren't valid numbers but which a person may infer as one due to their common suffixes; `k` (thousands), `m` (millions) or `b` (billions).
```js
{truncate;{replace;{replace;{replace;{$input};/k$/g;e3};/m$/g;e6};/b$/g;e9}}
```
