Action that utilizes a TagScript algorithm to calculate what day of the week a provided date fell/will fall on. Features include automagically adjusting to varying lengths of months (28 days - 31 days), automagically adjusting to leap years (you can't find out what day Feb. 29 2019 was because that date doesn't exist), and automagically adjusting to the Gregorian calendar (Dates before the year 1582, the start of the Gregorian calendar, won't be parsed).

**Usage:** `a!dayweek <YYYY-MM-DD>`  
**Example:** `a!dayweek 1776-07-04`  
**Output:** `July 4, 1776 is a Thursday`
