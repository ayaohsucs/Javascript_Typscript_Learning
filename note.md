**Template literals**
- string literals allowing embedded expressions.
```
 `string text ${expression} string text`
```
- enclosed by the back-tick instead of double or single quotes.
- [FYI] expression can be a literal value (a string or a number), a variable, a built-in value

**Javascript Loop**
- for loop
for (statement 1; statement 2; statement 3) {
    code block to be executed
}

- forEach Array prototype
array.forEach(function(currentValue, index, arr))

- for of 
for (variable of iterable) {
  statement
}

**Three dots**
- rest parameters: if the last parameter is prefixed with ..., it becomes an array whose elements are supplied by the actual arguments passed to the function 
```
function multiply(multiplier, ...theArgs) {
  return theArgs.map(function(element) {
    return multiplier * element;
  })
}
```
- theArgs is an array instance

- spread syntax: to expand an array (or any iterable) to places where zero or more arguments are expected
```
let dateFields = [1989, 6, 7];
let date = new Date(...dateFields);
```
