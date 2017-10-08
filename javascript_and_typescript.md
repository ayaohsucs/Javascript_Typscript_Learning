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

  let multiplication = multiply(5, 3, 2, 7);
```
- theArgs is treated as an array

- spread syntax: to expand an array (or any iterable) to places where zero or more arguments are expected
```
let dateFields = [1989, 6, 7];
let date = new Date(...dateFields);
```
**Regular Experssions**
- Patterns used to match charater combinations in strings
```
let re0 = /abc/;
let re1 = new RegExp('abc');
```
- `\`: Non-special <-> Special
- `^`: Matches beginning of input; `$`: End of input
- `*`: Matches the preceding expression 0 or more times. Equivalent to {0,}
- `+`: Matches the preceding expression 1 or more times. Equivalent to {1,}
- `\w`: Any alphanumeric character, including the underscore. Equivalent to `[A-Za-z0-9\]`

- When finding out whether a pattern is found in a string, use `test` or `search`
```
let found = re0.test('abbbc');  // this should return false
```

References: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions#special-word-boundary
