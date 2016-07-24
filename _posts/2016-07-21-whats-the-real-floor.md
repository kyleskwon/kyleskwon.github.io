---
layout: post
title: What's the Real Floor?
---

{:.center} 
## Breaking Down a Codewars Kata #2

{:.right} 
<strong>Difficulty level: easy</strong>

<br>
<hr>
<br>

{:.center} 
### Task

The objective of this challenge is to write a function that given a building floor (from an American's perspective) returns the "real" floor.

Specifically, the 1st floor is the ground floor and there is no 13th floor because of superstition (13 is unlucky). Actually, sometimes I see the 4th floor missing in an elevator, and I believe that's because "four" and "death" are similarly pronouced in Mandarin Chinese. For this kata, we'll still include the 4th floor, because it's fun to do bad things. 


~~~javascript
function getRealFloor(number) {
    // insert code here
}

getRealFloor(-1) == -1 # Basement floors
getRealFloor(0) == 0 # Special case to please Europeans
getRealFloor(1) == 0 # Ground floor
getRealFloor(2) == 1 # 2nd floor
...
getRealFloor(12) == 11 # 12th floor
getRealFloor(14) == 12 # 14th floor
getRealFloor(15) == 13 # 15th floor
~~~


{:.center} 
### Action

Instantly, I wanted to create an if, else if statement inside the function with the conditions (inside the parentheses) for the basement, ground, 1st, 2nd-12th, and 14th flor or higher. When a condition is true based on the number passed into getRealFloor, it would return the "real" floor as a number. I used the == to compare (n) to 0 and 1, and the > and < symbols to compare (n) to 0, 1, and 13


~~~javascript
function getRealFloor(n) {
  if (n == 0 || n == 1) {
    return 0;
  } else if (n < 0) {
    return n;
  } else if (n > 1 && n < 13) {
    return n - 1;
  } else if (n > 13) {
    return n - 2;
  }
}
~~~

{:.center} 
### Result

All the tests passed

~~~javascript
* the number passed into the function is an American floor
getRealFloor(-1); 
    returns -1 # Basement floors
getRealFloor(0); 
    returns 0 # Special case to please Europeans
getRealFloor(1); 
    returns 0 # Ground floor
getRealFloor(2); 
    returns 1 # 2nd floor
...
getRealFloor(12); 
    returns 11 # 12th floor
getRealFloor(14); 
    returns 12 # 14th floor
getRealFloor(15); 
    returns 13 # 15th floor
~~~

Can you think of another solution for [this kata](https://www.codewars.com/kata/574b3b1599d8f897470018f6)?