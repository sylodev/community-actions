**Description:** Returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and stops before a specified number. Mimics [range()](https://www.w3schools.com/python/ref_func_range.asp)

**Instructions:** `{range;max;min?;steps?}`

**Code:**
```
[#function;range;{=range_max};{=range_min};{=range_steps}]
    {=range_array;{random length={math;{$range_max}-{or;{$range_min};0}} return_array=true;1}}
    {=range_index;{or;{$range_min};0}}
    {=range_output;{[]}}

    {for;{=range_num};{$range_array};
        {push;{$range_output};{$range_index}}
        {if;{math;{$range_index}+{or;{$range_steps};1}};>=;{$range_max};{break}}
        {=range_index;{math;{$range_index}+{or;{$range_steps};1}}}
    }

    {return;{$range_output}}
[/function]
```
