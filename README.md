# JavaScript-Algorithms


**__Simple Algorithm Repo I've put together to show the work I have beginners knowledge of. I'll be using these algorithms in the future to build projects and further my ability to use these, and other more efficient ways of doing things. This was all done through freecodecamp in their browser engine.__** 
___

**//Reversal of String**
```
function reverseString(str) {
  return str.split('').reverse().join('');
}

reverseString("hello");
```
___





**//Factorialize**
```
function factorialize(num) {
  if (num === 0) {return 1;}
  return num * factorialize (num - 1)
}

factorialize(5);
```
___






**//Palindrome Identifier**
```
function palindrome(str) {
  let front = 0;
  let back = str.length - 1;
  while (back > front) {
    while ( str[front].match(/[\W_]/) ) {
      front++;
      continue;
    }
    while ( str[back].match(/[\W_]/) ) {
      back--;
      continue;
   }
     if ( str[front].toLowerCase() !== str[back].toLowerCase() ) return false
    front++;
    back--;
  }
  return true;
}


palindrome("eye");
```
___






**//String Identifier**
```
function findLongestWord(str) {
  var words = str.split(' ');
  var maxLength = 0;
  
  for (var i = 0; i < words.length; i++) {
    if (words[i].length > maxLength) {
      maxLength = words[i].length;
    } 
}
  return maxLength;
}

findLongestWord("I must not fear.
Fear is the mind-killer.
Fear is the little-death that brings total obliteration.
I will face my fear.
I will permit it to pass over me and through me.
And when it has gone past I will turn the inner eye to see its path.
Where the fear has gone there will be nothing. Only I will remain.");
```
___





**//Case Modifier** 
```
function titleCase(str) {
  return str.toLowerCase().replace(/(^|\s)\S/g, (L) => L.toUpperCase());
}

titleCase("Telperion and Laurelin");
```
___




**//Largest number in Array Selector**
```
function largestOfFour(arr) {
  var results = [];
  for (var n = 0; n < arr.length; n++) {
    var largestNumber = arr[n][0];
    for (var sb = 1; sb < arr[n].length; sb++) {
      if (arr[n][sb] > largestNumber) {
        largestNumber = arr[n][sb];
      }
    }
    
    results[n] = largestNumber;
  }
  
    return results;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```
___




**//Boolean String Verifier**
```
function confirmEnding(str, target) {
  return str.substr(-target.length) === target;
}

confirmEnding("Bastian", "n");
```
___




**//Recursive String Repeater**
```
function repeatStringNumTimes(str, num) {
  if (num < 0)
    return "";
  if (num === 1)
    return str;
   else
    return str + repeatStringNumTimes(str, num - 1); 
  }


repeatStringNumTimes("abc", 3);
```
___
