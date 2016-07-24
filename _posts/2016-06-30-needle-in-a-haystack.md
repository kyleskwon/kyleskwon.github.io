---
layout: post
title: Needle in a Haystack
---

{:.center} 
## Breaking Down a Codewars Kata #1

{:.right} 
<strong>Difficulty level: easy</strong>

<br>
<hr>
<br>

{:.center} 
### Task

The objective of this challenge is to write a function called findNeedle() that takes an array full of junk, but contains one "needle". Once it finds the needle, it should return the phrase "found the needle at position " plus the index of the needle.

The function is given with an empty body like so...

~~~javascript
function findNeedle(haystack) {
    // insert code here
}
~~~

{:.center} 
### Action

Immediately, I thought to find the index of the string "needle" in the haystack (the array that is passed into the function) using the .indexOf() method (which returns a number). After storing the index in a variable, I returned the phrase plus that variable using string concatination

~~~javascript
function findNeedle(haystack) {
    var index = haystack.indexOf("needle");
    return "found the needle at position " + index;
}
~~~

{:.center} 
### Result

Thus, for this function

~~~javascript
findNeedle(['hay', 'junk', 'moreJunk', 'needle', 'randomJunk'])
~~~

the result is 

~~~javascript
"found the needle at position 3"
~~~

because the first index of an array is 0, so even though the needle is in the fourth position, it's index is 3.

Notice the space after the word "position" in the function so the 5 doesn't latch onto it in the phrase that is returned. 

Can you think of another solution for [this kata](https://www.codewars.com/kata/a-needle-in-the-haystack/train/javascript)?