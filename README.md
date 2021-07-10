# uplab
Михайлов Константин
____
# Задание 1
Check to see if a string has the same amount of 'x's and 'o's. The method must return a boolean and be case insensitive. The string can contain any char.
# Код
```html
function XO(str) {
    var a = str.replace(/x/gi, '');
    var b = str.replace(/o/gi, '');
    return a.length === b.length;
}
```
____
# Задание 2
An isogram is a word that has no repeating letters, consecutive or non-consecutive. Implement a function that determines whether a string that contains only letters is an isogram. Assume the empty string is an isogram. Ignore letter case.
```html
function isIsogram(str){
  var i, j;
  str = str.toLowerCase();
  for(i = 0; i < str.length; ++i)
    for(j = i + 1; j < str.length; ++j)
      if(str[i] === str[j])
        return false;
  return true;
}
```
____
# Задание 3
Make a program that filters a list of strings and returns a list with only your friends name in it.

If a name has exactly 4 letters in it, you can be sure that it has to be a friend of yours! Otherwise, you can be sure he's not...
```html
function friend(friends){
  return friends.filter(name => name.length === 4)
}
```
____
# Задание 4
In DNA strings, symbols "A" and "T" are complements of each other, as "C" and "G". You have function with one side of the DNA (string, except for Haskell); you need to get the other complementary side. DNA strand is never empty or there is no DNA at all (again, except for Haskell).
```html
function DNAStrand(dna){
    var res= "";
      for(var i =0; i<dna.length; i++) 
      {
        if (dna[i]==="A") 
       {
        res +="T";
       }
        else if (dna[i]==="T") 
       {
        res += "A";
        }
        else if (dna[i]==="C")
        {
        res +="G";
        }
        else if (dna[i]==="G")
        {
        res += "C";
        }
        else {
        res+=dna[i];
        }
     }
     return result;
}
```
____
# Задание 5
Trolls are attacking your comment section!

A common way to deal with this situation is to remove all of the vowels from the trolls' comments, neutralizing the threat.

Your task is to write a function that takes a string and return a new string with all vowels removed.

For example, the string "This website is for losers LOL!" would become "Ths wbst s fr lsrs LL!".

Note: for this kata y isn't considered a vowel.
```html
function disemvowel(str) {
  return str.replace(/[aeiou]/gi, '');
}
```
____
# Задание 6
Your task is to make a function that can take any non-negative integer as an argument and return it with its digits in descending order. Essentially, rearrange the digits to create the highest possible number.
```html
function descendingOrder(n){
  return parseInt(String(n).split('').sort().reverse().join(''))
}
```
____
# Задание 7
Given the triangle of consecutive odd numbers:
```html
             1
          3     5
       7     9    11
   13    15    17    19
21    23    25    27    29
...
```
Calculate the sum of the numbers in the nth row of this triangle (starting at index 1)
```html
function rowSumOddNumbers(n) {
	return Math.pow(n, 3);
}
```
____
# Задание 8
In this kata you will create a function that takes a list of non-negative integers and strings and returns a new list with the strings filtered out.
```html
function filter_list(l) {
  return l.filter(Number.isInteger);
}
```
____
# Задание 9
Given two integers a and b, which can be positive or negative, find the sum of all the integers between and including them and return it. If the two numbers are equal return a or b.
```html
function getSum( a,b )
{
  var min = Math.min(a, b),
  max = Math.max(a, b),
  result = 0;
  while (min <= max) {
    result += min;
    min++;
  }
  return result;
}
```
____
# Задание 10
You are given an odd-length array of integers, in which all of them are the same, except for one single number.

Complete the method which accepts such an array, and returns that single different number.
```html
function stray(numbers) {
    var a = numbers.sort();
  
  if(a[0] != a[1]) {
    return a[0]
  } 
  return a[a.length-1]
}
```
