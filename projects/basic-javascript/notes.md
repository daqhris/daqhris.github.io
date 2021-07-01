# Basic JavaScript : Notes 
These are notes taken during self-learning sessions on the [freeCodeCamp](https://www.freecodecamp.org) platform. 

This notebook contains an overview of the fundamentals of JavaScript including *variables*, *arrays*, *loops* and *functions*.

~~Notes: brief records written down to aid the memory.~~

**Last update: 2021/05/31** (_ongoing changes_) 

## Courses (_78/111_)

1. Declare JavaScript variables  
JavaScript has 8 data types: `undefined`, `null`, `boolean`, `string`, `symbol`, `bigint`, `number`, `object`.  
Variables allow computers to store and manipulate data.  Declare a variable by using the word **var**.  
End statements with *semicolons*.

2. Storing values with the assignment operator  
Store a value in a variable with the *assignment* operator `=`.  
Calculations are firstly performed on the right side of `=` before the value is assigned to the left side.  

3. Assigning the value of one variable to another  
The value of one variable can be assigned to another variable by using the assignment operator.

4. Initializing variables with the asssignment operator  
It's totally right to attribute value to a variable in the same line that it is declared. 

5. Understanding uninitialized variables  
New variables have an initial value of `undefined`.  
If you do a mathematical operation on an `undefined` variable your result will be **NaN** which means _"Not a Number"_.  
If you concatenate a string with an `undefined` variable, you will get a literal string of `undefined`.

6. Understanding case sensitivity in variables  
All variables and function names are **case sensitive**.  
Capitalization is important.  
Multi-word variable names have the first word in lowercase and the first letter of each subsequent word is capitalized, like *camelCase*.

7. Add two numbers with JavaScript  
*Number* is a data type that represents numeric data.  
Use `+` as a symbol for an addition operator when placed between two numbers.  

8. Substract one number from another  
Use `-` as symbol for substraction.  

9. Multiply two numbers  
Use `*` for multiplication of 2 numbers.

10. Divide one number by another  
Use `/` for division.

11. Increment a number  
Use `++` to *increment* or add 1 to a variable.  
`i++;` equals `i=i+1;`

12. Decrement a number  
Decrease a variable by 1 with `--`.  

13. Create decimal numbers  
Decimal numbers can also be called *floating point* or *floats* and be stored in variables as value.  

14. Multiply two decimals  
Decimal numebrs can be multiplied like the whole numbers.  

15. Divide one decimal by another  

16. Finding a remainder  
`%` is the remainder operator that gives the remainder of the division of two numbers.  
Remainder division by 2 will determine if a number is *Odd* or *Even*.  

17. Compound assignment with augmented addition  
The `+=` operator is used to add by addition and assign directly a value to a variable.

18. Compound assignment with augmented substraction  
The operator `-=` substracts a number from a variable.  

19. Compound assignment with augmented multiplication  
`*=` multiplies a variable by a number.  
 
20. Compound assignment with augmented division  
`/=` divides a variable by another number.  

21. Declaring string variables  
A string is a series of zero or more characters enclosed in single or double quotes.

22. Escaping literal quotes in strings  
Place a backslash `\` in front of the quote so that the quote `"` appears inside the string.

23. Quoting strings with single quotes  
Single and double quotes work the same.  
A string has the exact kind of quote at the beginning and the end.  
One special use case is when `<a>` is present. Use single quote `'` for outer quotes.

24. Escape sequences in strings  
Reasons to use escaping characters : usage of special characters such as carriage return `\r`(or new line `\n` or tab `\t`) and represent multiple quotes in a string without misrepresentation.

25. Concatenating strings with plus operator  
The *concatenating* operator is the `+` operator used with a `String` value.

26. Concatenating strings with the plus equals operator  
*concatenate*: linked together in a chain or series.  
Use `+=` to concatenate a string onto the end of an existing string variable.

27. Constructing strings with variables   
One or more variables can be inserted into a string by using the concatenation operator `+`. 

28. Appending variables to strings  
It is possible to append more than one variables to a string by using `+=`.

29. Find the length of a string  
To know the length of a string value, you write `.length` after the string variable or string literal.

30. Use bracket notation to find the first character in a string  
*zero-based* indexing: starting to count from zero.  
Finding a character at a specific zero-based index within a string is called *bracket notation*.  
```javascript
var firstName = "Charles";
var firstLetter = firstName[0];
```  

31. Understand string immutability  
*immutable*: can't be altered after creation.  
String values are immutable.  
You can not change an individual character of a string.  
The only way to change this string is to assign it with a whole new string.

32. Use bracket notation to find the Nth character in a string  
Bracket notation `[]` is necessary to get the character at any position inside a string. 

33. Use bracket notation to find the last character in a string  
Substract one from the string's length in order to get the last letter. `.length - 1`. 

34. Use bracket notation to find the Nth-to-last character in a string  
Use `.lenght - nth` to get the value of the nth-to-last caharacter in a string value.

35. Word blanks  
_Mad Libs_ is a game of filling words in the missing pieces of a sentence.

36. Store multiple values in one variable using JavaScript Arrays
Store many pieces of data in one place by using the variable `array`.
```javascript
var sandwich = ["peanut butter", "bread", 2021]
```

37. Nest one array within another array
Otherwise called *multi-dimensional array*.
```javascript
var myArray = [["jump", 100],["dance", 150], ["walk", 50]];
```

38. Access array data with indexes
Access to data inside arrays is done with *indexes*.
_array indexes_ have the same bracket notation as strings and are *zero-based*.  
`var myData = myArray[0];`

39. Modify array data with indexes  
Entries of arrays are *mutable*.
`myArray[0] = 45;`

40. Access mutli-dimensional arrays with indexes  
*Multi-dimensional arrays* are an array of arrays.

41. Manipulate arrays with push()
`.push()` function is used to append data at the end of an array.
`.push()` takes one or more parameters. 

42. Manipulate arrays with pop()  
`.pop()` function is used to pop a value off of the end of an array which will be store by assigning it to a variable.

43. Manipulate arrays with shift()  
`.shift()` function removes the first element from an array.

44. Manipulate arrays with unshift()  
`.unshift()` function is used to add elements in front of an array. 

45. Shopping List  
```javascript
var myList = [["peanuts", 10],["books", 9],["shirts", 8],["lamps", 7],["shoes", 7],["watches", 6]];
```

46. Write reusable JavaScript with functions  
*functions* are reusable parts of code.
Once they are defined, you can omit writing the full code and only *invoke* the function `functionName();`.  
```javascript
function functionName() {
  console.log("Hello World");
}
```

47. Passing values to function with arguments  
*Parameters* are variables that act as placeholders for the value that are to be input when it is called.   
*Arguments* are the actual values that are input into a function when it is called.  
```javascript
function testFun(param1, param2) {
  console.log(param1, param2);
}
```
```javascript
function functionWithArgs(param1, param2) {
  console.log(param1 + param2);
};
functionWithArgs(144, 256);
```

48. Global scope and functions
*Scope* means the visibility of variables.  
Variables which are defined outside of a function block have *global* scope, meaning that they can be seen everywhere in the code. 
Always declare variables with `var`. Without `var`, they are created in the *global* scope. 

49. Local scope and functions  
Variables that are only visible within a function or function parameters have *local* scope. 

50. Global vs. Local scope in functions  
*local* variable takes precedence over the *global* variable.

51. Return a value from a function with return  
`return` statement is used to send a value back out of a function.  
Pass values into a function with *arguments*.  
```javascript
function plusThree(num) {
  return num + 3;
}
var answer = plusThree(5);
```
`answer` has the value `8`. 

52. Understanding undefined value returned from a function   
```javascript
var sum = 0;
function addSum(num) {
  sum = sum + num;
}
addSum(3);
```
`addSum` is a function without a `return` statement. The function will change the global `sum` variable but the returned value of the function is `undefined`.

53. Assignment with a returned value  
Whatever that's on the right of the equal sign will be resolved before the value is assigned, even if it's a return value. 

54. Stand in line  
A *queue* is an abstract *data structure* where items are kept in order.  
```javascript
function nextInLine(arr, item) {
  arr.push(item);
    return item = arr.shift();
}
```
55. Understanding boolean values 
*boolean* is a data type that may only be: `true` or `false`.  
These two states are mutually exclusive, one is on and other is off.  

56. Use conditional logic with if statements  
_if_ statements lead to the execution of code in the curly braces under certain conditions defined in the parantheses.
```
if (condition is true) {
  statement is executed
}
```
```javascript
function trueOrFalse(wasThatTrue) {
if (wasThatTrue) {
  return "Yes, that was true"
}
return "No, that was false";
}
```

57. Comparison with the equality operator  
`==` is called the *equality operator*, one of many *comparison operators*. 
It compares two values and returns `true` if they're equivalent or `false` if they are not. It also operates a type conversion of the compared values(_number, string, ..._)

58. Comparison with the strict equality operator  
`===` is called the *strict equality* and does not perform a type conversion. 

59. Practice comparing different values  
Determine the type of a variable or a value with the `typeof` operator. 
`==` operator performs type conversion but `===` does not perform type conversion. 

60. Comparison with the inequality operator  
`!=` is the inequality operator, meaning *not equivalent* and that it returns `false` where equality would return `true` and *vice versa*.

61. Comparison with the strict inequality operator  
`!==` means **striclty not equal** and does not convert data types.

62. Comparisson with the greater than operator  
The _greater than_ operator `>` compares the values of two numbers.  
It returns `true` when the number on the left is greater than the number to the right. 

63. Comparison with the greater than or equal to operator  
`>=` is called the _greater than or equal to_ operator.

64. Comparison with the less than operator  
`<` is named the *less than* operator that compares the values of two numbers. 

65. Comparison with the less than or equal to operator  
The _less than or equal to_ operator is `<=`.

66. Comparison with the logical and operator  
`&&` is called the _logical and_ operator.
It will return `true` if and only if the _operands_ to the left and to the right of it are true.   
```javascript
if (num > 5 && num < 10) {
  return "Yes";
}
return "No";
```

67. Comparisons with the logical or operator  
The *logical or* operator `||` returns `true` if either of the _operands_ is `true`.  
```javascript
if (num > 10 || num < 5) {
  return "No";
}
return "Yes";
```

68. Introducing else statements  
With an `else` statement, an alternate block of code gets executed. `if/else`

69. Introducing else if statements   
In the case of many conditions, you can chain `if` statements together with `else if` statements. 
```javascript
if (num > 15) {
  return "Bigger than 15";
} else if (num < 5) {
  return "Smaller than 5";
} else {
  return "Between 5 and 15";
}
```

70. Logical order in if else statements  
Order is very important when working with `if` and `else if` statements. 

71. Chaining if else statements  
```javascript
if (condition1) {
  statement1
} else if (condition2) {
  statement2
} else if (condition3) {
  statement3
. . .
} else {
  statementN
}
```  

72. Golf Code  
```javascript
var names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"];
function golfScore(par, strokes) {
  // Only change code below this line
if (par, strokes == 1) {
  return "Hole-in-one!";
}
else if (par, strokes <= par - 2) {
  return "Eagle";
}
else if (par, strokes == par - 1) {
  return "Birdie";
}
else if (par, strokes == par) {
  return "Par";
}
else if (par, strokes == par + 1) {
  return "Bogey";
}
else if (par, strokes == par + 2) {
  return "Double Bogey";
}
else {
  return "Go Home!";
}
  // Only change code above this line
}
golfScore(5, 4);
```  

73. Selecting from many options with switch statements   
Use a `switch` statement when you have many options to choose from.  
`case` statements define various possible values.  
`switch` tests a value and can have many *case* statements.  
Statements are executed from the first matched `case` value until a `break` is encountered.  
```javascript
switch(lowercaseLetter) {
  case "a":
    console.log("A");
    break;
  case "b":
    console.log("B");
    break;
}
```  
`case` values are tested with strict equality `===`.  
The `break` stops executing statements.  
If `break` is omitted, next statement will be executed.  

```javascript
function caseInSwitch(val) {
  var answer = "";
  // Only change code below this line
switch(val) {
  case 1:
      return "alpha";
    break;
  case 2:
      return "beta";
    break;
  case 3:
      return "gamma";
    break;
  case 4:
      return "delta";
    break;
}
  return answer;
}
caseInSwitch(1);
```  

74. Adding a default option in switch statements  
Add the `default` statement which will be executed if no matching `case` statements are found.  
`default` statement should come in the last position.  

```javascript
default:
  defaultStatement;
  break;
```

75. Multiple identical options in switch statements  

```javascript
var result = "";
switch(val) {
  case 1:
  case 2:
  case 3:
    result = "1, 2, or 3";
    break;
  case 4:
    result = "4 alone";
}
```

76. Replacing if else chains with switch  
`switch` statements can be easier to write than many chained `if/else if` statements.  

77. Returning boolean values from functions  
Use *equality comparison* instead of *if/else* statements. 
```javascript
function isEqual(a,b) {
  return a === b;
}
```  

78. Return early pattern for functions  
As soon as `return` statement is reached, the execution of the current function stops and control returns to the calling location.  

```javascript
function abTest(a, b) {
if (a<0 || b<0) {
  return undefined;
}
  return Math.round(Math.pow(Math.sqrt(a) + Math.sqrt(b), 2));
}
abTest(2,2);
```

79. Counting cards  
