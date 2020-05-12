# Coding Solutions

> My own coding solutions to different coding challenges.

### Table of Contents

- [Freecodecamp](#Freecodecamp)
  - [Intermediate Algorithm Scripting](#Intermediate-Algorithm-Scripting)
  - [ex2](#free_ex2)
  - [ex3](#free_ex3)
  - [ex4](#free_ex4)
  
- [Hackerrank](#Hackerrank)
  - [Making Anagrams](#Making-Anagrams)
  - [ex2](#haker_ex2)
  - [ex3](#haker_ex3)
  - [ex3](#hakr_ex4)
  
## Freecodecamp

### Intermediate Algorithm Scripting
* [Sum All Numbers in a Range](#Sum-All-Numbers-in-a-Range)
* [Diff Two Arrays](#Diff-Two-Arrays)
* [Seek and Destroy](#Seek-and-Destroy)
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

  
### Sum All Numbers in a Range

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

### Diff Two Arrays

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
### Seek and Destroy

## Hackerrank

### Making Anagrams(https://www.hackerrank.com/challenges/ctci-making-anagrams/problem?h_l=interview&playlist_slugs%5B%5D=interview-preparation-kit&playlist_slugs%5B%5D=strings)
```
solution:
function makeAnagram(a, b) {
    var arrA = a.split('');
    var arrB = b.split('');
    var diff = [];
    var same = [];
    arrA.concat(arrB).map(function(val){
        if (!arrA.includes(val) || !arrB.includes(val))
           diff.push(val);
        else
           if (!same.includes(val))
              same.push(val);  
    });

    var freq= same.reduce(function(acc,val){
            var freq1 = 0;
            var freq2 = 0;
            for (var i = 0;i < arrA.length;i++){
                if (arrA[i] == val)
                   freq1++;
            }
            for (var j = 0;j < arrB.length;j++){
                if (arrB[j] == val)
                   freq2++;
            }
            acc = acc + (Math.max(freq1,freq2) - Math.min(freq1,freq2)); 
            return acc;
    },0);                                           
                                               
    return freq+diff.length
}


```
