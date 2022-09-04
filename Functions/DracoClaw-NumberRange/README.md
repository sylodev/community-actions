**Description:** Returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and stops before a specified number.

**Instructions:** `{range;max;min?;steps?}`

**Code:**
```
[#function;range;{=max};{=min};{=steps}]
    {=array;{random length={$max} return_array=true;1}}
    {=index;{or;{$min};0}}
    {=output_range;{[]}}

    {for;{=num};{$array};
        {push;{$output_range};{$index}}
        {if;{math;{$index}+1};==;{$max};{break}}
        {=index;{math;{$index}+{or;{$steps};1}}}
    }

    {return;{$output_range}}
[/function]
```
