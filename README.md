# uplab

____----
# Задание 1
Check to see if a string has the same amount of 'x's and 'o's. The method must return a boolean and be case insensitive. The string can contain any char.
# Код:
```html
function XO(str) {
    var a = str.replace(/x/gi, '');
    var b = str.replace(/o/gi, '');
    return a.length === b.length;
}
```
