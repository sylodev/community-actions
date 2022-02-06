# NumberSorter
Sorts values from highest to lowest.

**Directions:**  
Fill out the `{set}` at the begining of the snippet with the values you want sorted.  
The snippet will sort the values and place them in keys.  
`{get;1}` - Highest  
`{get;2}` - Second Highest  
`{get;3}` - Second Lowest  
`{get;4}` - Lowest

**Expanding:**  
Expanding the snippte is as simple as adding another one of the modules to the end, incrementing the `{set}` value each time.  
```
{set;string;{replace;{get;string};/{get;4}/;}}
{set;5;{math;max({get;string})}}
```
Additionally add another `value` key to the top as well as to the `{set;string;...}`. 
