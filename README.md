# uplab

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
