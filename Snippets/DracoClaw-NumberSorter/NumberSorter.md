**Code:** 
```
{set;A;valueA}
{set;B;valueB}
{set;C;valueC}
{set;D;valueD}

{set;string;{get;A} {get;B} {get;C} {get;D}}

{set;1;{math;max({get;string})}}
{set;string;{replace;{get;string};{get;1};}}
{set;2;{math;max({get;string})}}
{set;string;{replace;{get;string};{get;2};}}
{set;3;{math;max({get;string})}}
{set;string;{replace;{get;string};{get;3};}}
{set;4;{math;max({get;string})}}

{get;1} {get;2} {get;3} {get;4}
```
