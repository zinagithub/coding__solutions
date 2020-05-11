# Coding Solutions

> My own coding solutions to different coding challenges.

### Table of Contents

- [Freecodecamp](#Freecodecamp)
  - [Intermediate Algorithm Scripting](#Intermediate-Algorithm-Scripting)
  - [ex2](#free_ex2)
  - [ex3](#free_ex3)
  - [ex4](#free_ex4)
  
- [hakerrank](#hakerrank)
  - [ex1](#haker_ex1)
  - [ex2](#haker_ex2)
  - [ex3](#haker_ex3)
  - [ex3](#hakr_ex4)
  
## Freecodecamp

### Intermediate Algorithm Scripting
* [Sum All Numbers in a RangePassed](#Sum-All-Numbers-in-a-RangePassed)
* [Diff Two ArraysPassed](#Diff-Two-ArraysPassed)
* [Seek and DestroyPassed]
* [Wherefore art thou]
* [Spinal Tap CasePassed]
* [Pig Latin]
* [Pig Latin]
* [Pig Latin]
* [Pig Latin]
* [Pig Latin]
* [Pig Latin]
* [Pig Latin]
* [Pig Latin]
* [Pig Latin]
* [Pig Latin]
* [Pig Latin]

  
### Sum All Numbers in a RangePassed

 We'll pass you an array of two numbers. Return the sum of those two numbers plus the sum of all the numbers between them. The lowest number will not always come first.

 ``` 
 Solution: 
 function sumAll(arr) {
  let sum = 0;
  let min = Math.min(arr[0],arr[1]);
  let max = Math.max(arr[0],arr[1]);
  for(let i= min;i <= max;i++){
     sum = sum + i
  }
  return sum;
}

sumAll([1, 4]);
``` 

### Diff Two ArraysPassed

Compare two arrays and return a new array with any items only found in one of the two given arrays, but not both. In other words, return the symmetric difference of the two arrays.
``` 
Solution1:
function diffArray(arr1, arr2) {
  var newArr = [];

    arr1.map(function(val){
      if (arr2.indexOf(val)==-1)
             newArr.push(val) 
      });
  
    arr2.map(function(val){
      if (arr1.indexOf(val)==-1)
             newArr.push(val); 
       });    
  
  return newArr;
}

diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]);

```
```
solution2:
function diffArray(arr1, arr2) {
    return arr1.
    concat(arr2).
    filter(val => !arr1.includes(val)||!arr2.includes(val)) 
}

diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]);

```


