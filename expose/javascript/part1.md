# Part 1. A Quick Introduction

### var declaration

1. Line 9 prints _values added: 20_ since the variable names result is set to
   the sum of num1 and num2 on line 7. The function call in line 16 passes in
   the values of num1 as 10 and num2 as 10, thus result is set to 20. The
   statment in line 9 then prints the string "values added: " followed by the
   value of the result variable leading to the output: _values added: 20_

2. Line 13 prints _final result: 20_ since the value of result is 20 for teh
   same reasons as question 1. Using var to declare result results in teh
   variable result having function scope, meaning that it can be accessed from
   anywhere within teh function. The keyword var does not provide a block scope
   which is why result is accessible outside the if block even though it is
   declared within it.
