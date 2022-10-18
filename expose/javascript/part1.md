# Part 1. A Quick Introduction

### var declaration

1. Line 9 prints `values added: 20` since the variable names result is set to
   the sum of num1 and num2 on line 7. The function call in line 16 passes in
   the values of num1 as 10 and num2 as 10, thus result is set to 20. The
   statment in line 9 then prints the string "values added: " followed by the
   value of the result variable leading to the output: `values added: 20`

2. Line 13 prints `final result: 20` since the value of result is 20 for teh
   same reasons as question 1. Using var to declare result results in teh
   variable result having function scope, meaning that it can be accessed from
   anywhere within teh function. The keyword var does not provide a block scope
   which is why result is accessible outside the if block even though it is
   declared within it.


### let declaration

3. Line 9 still prints `values added: 20` musch like as with the var declaration
   in question 1 for that same reasons as in that question. The only difference
   between var and let declarations is the existence of a block scope. This
   doesn't change anything for the console.log statement on line 9 as it is in the same block in which the variable result was declared.

4. Line 13 results in a reference error being thrown since the variable result is not
   accessible outside of the code block of the if statement. This is different
   from question 2 since the var declaration does not have a block scope, so the
   result could be accessed within the entire function. Using the let
   declaration in this code limits result's scope to the if block and the
   console.log statement on line 13 falls outside this code block thus is not
   able to reference the variable to print its value.

### const declaration

5. Nothing is printed on line 9 since the code exits with a Type error on line 7
   before it reaches this line. result is a constant and the
   function attempts to change its value in ine 7 which results in teh Type
   Error.

6. This is a similar situation to question 5. Nothing is printed because the
   code exits with a Type error before reaching line 13 due to an attempt to change the value of the constant result in line 7.
