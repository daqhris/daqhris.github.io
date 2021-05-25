# Basic JavaScript : Notes 
These are notes taken during self-training sessions on the freeCodeCamp platform.  

***Last changes: 2021/05/25***

## Main Lessons

1. Declare JavaScript Variables  
JavaScript has 8 data types: `undefined`, `null`, `boolean`, `string`, `symbol`, `bigint`, `number`, `object`.  
Variables allow computers to store and manipulate data.  Declare a variable by using the word **var**.  
End statements with *semicolons*.

2. Storing values with the assignment operator  
Store a value in a variable with the *assignment* operator `=`.  
Caculations are firstly performed on the right side of `=` before the value is assigned to the left side.  

3. Assigning the value of one variable to another  
The value of one variable can be assigned to another variable by using the assignment operator.

4. Initializing variables with the asssignment operator  
It's totally right to attribute value to a variable in the same line that it is declared. 

5. Understanding uninitialized variables  
New variables have an initial value of **undefined**.

6. Understanding case sensitivity in variables  
All variables and function names are case sensitive.  
Capitalization is important.  
Multi-word variable names have the first word in lowercase and the first letter of each subsequent word is capitalized. Same as in : *camelCase*.

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

25. Concatening strings with plus operator  
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
*immutable*: can't be altered after creation  
String values are immutable.  
You can not change an individual character of a string.  
The only way to change this string is to assign it with a whole new string.

32. Use bracket notation to find the Nth character in a string  
Bracket notation `[]` is necessary to get the character at any position inside a string. 

33. Use bracket notation to find the last character in a string  
Substract one from the string's length in order to get the last letter. `.length - 1` 

34. Use bracket notation to find the Nth-to-last character in a string  
Use `.lenght - nth` to get the value of the nth-to-last caharacter in a string value.

35. Word blanks
