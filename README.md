# JavaScript-Algorithms


Simple Algorithm Repo


//Reversal of String
function reverseString(str) {
  return str.split('').reverse().join('');
}

reverseString("hello");
//


//Factorialize
function factorialize(num) {
  if (num === 0) {return 1;}
  return num * factorialize (num - 1)
}

factorialize(5);
//



//Palindrome Identifier
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
//


//String Identifier
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

findLongestWord("The quick brown fox jumped over the lazy dog");
//


//Case Modifier 
function titleCase(str) {
  return str.toLowerCase().replace(/(^|\s)\S/g, (L) => L.toUpperCase());
}

titleCase("I'm a little tea pot");
//
