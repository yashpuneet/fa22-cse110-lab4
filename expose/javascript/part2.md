# Part 2. A Little More of a Challenge...

### Declarations

1. Line 12 prints out the number of elements in the passed array `prices`. This
   is done by printing the final value of the for loop iteration variable `i`
   which caused the for loop to exit. Since the iteration variable `i` is
   declares using `var` which cannot have a block scope, it has a function scope
   instead and is thus accessible outside the loop. The console.log statement is
   within the function `i` was declared in, so its value is printed out. Line 12
   therefore prints `3` to the console.

2. Line 13 prints out the value calculated and stored in the variable
   `discountedPrice` in the last iteration of the for loop. Much like the
   iteration variable, `discountedPrice` is defined usring `var` meaning that it
   has a function scope (block scope does not exist for `var`). The last
   iteration sets `discountedPrice` to `300*(1-0.5) = 300*0.5 = 150`. Line 13
   therefore prints the value `150` to the console.

3. Line 14 prints the value of `finalPrice` set in the last iteration of the for
   loop. As seen in question 3, the value of `discountedPrice` in this iteration
   is 150. The `Math.round()` function rounds a number to the nearest integer
   however, since `discountedPrice * 100` is already an integer, it has no effect.
   Moreover, dividing `discountedPrice * 100` by 100 results in `finalPrice`
   being assigned the value of `discountedPrice`. Line 14 therefore prints the
   value `150` to the console.

4. The functon will return an array of discounted prices, with the value at each
   index being the discounted price corresponding to the price at the same index
   in the passed in `prices` array. The for loop iterates through all these
   prices, calculates the 'discountedPrice`, rounds it to 2 decimal places and
   stores it in the `discounted` array to be returned. The funtion therfore
   returns the array `[50, 100, 150]`.

5. Line 12 causes a Reference error to occur since the iteration variable `i` is
   not accessible at line 12. Being declared using `let`, the iteration
   variable can have block scope and since it is declared in teh for loop, its
   block is the for loop. Since the `console.log()` function lies outside the
   for loop, the iteraton variable `i` canot be accessed by it.

6. Line 13 causes a Reference error for the same reason as question 5. The
   variable `discountedPrice` is declared using `let` in the for loop and thus
   has a block scope limited to the for loop. The `console.log()` statement
   falls outside the for loop and thus `discountedPrice` cannot be referenced by
   it causinga Reference error.

7. Line 14 prints the value assigned to `finalPrice` in the last iteration of
   the for loop. Though being declared with `let`, 'finalPrice' is declared
   outside of any code blocks within the function giving it function scope. As
   the `console.log()` statement falls within the function, `finalPrice` can be
   accessed by it and its value is printed to the console. This value was
   calculated in question 3 and is `150`. Line 14 therefore prints `150` to the
   console.

8. The function still returns an array of diuscounted prices much like question
   4 . Even though teh variable declarations changed from `var` to `let`, this 
   did not cause any scope reference errors for calculations as these exist
   within the for loop code block. Therefore, for the same reasons as question
   4, the function returns the array `[50, 100, 150]`.

9. Line 11 returns a reference error much like question question 5 . The `let`
   variable declaration gives i block scope limited to teh for loop thus teh
   `console.log()` statement on line 12 is not able to access `i` to print its
   value resulting in a Reference error. 

10.  Line 12 prints out the number of elements in the input array `prices`. This is beacouse length is declared as a constant and set to the legth of teh array. This value has function scope and since, the `console.log()` statement is within the function it is able to print teh value of `length` to teh concole. Therefore, teh value printed in `3`.

11. The  funtion will return an array of discounted prices. Even though
	discountedPrice is declared as a constant, it has block scope and is thus
	redeclared every iteration. Due to this, it is never actually changed across
	iteratiosn since it is essentially out-of-scope and inaccessible after each
	iteration and then redeclared at the beginning of the next iterations. The
	output is therefore the array `[50, 100, 150]`.

### Datatypes

12. 
	A. student.name
	B. student["Grad Year"]
	C. student.greeting()
	D. student["Favorite Teacher"].name
	E. student.courseLoad[0]

### Arithmetic

13.
	A. '3' + 2 = '32' 
		- To allow string concatenation, the integer 2 is converetd to a string

	B. '3' - 2 = 1
		- Since - does not define any string operation, the string is converted
		  to an integer instead to allow the numerical subtraction operation

	C. 3 + null = 3
		- The + here is respresenting teh numerical addition opertaion since
		  there is no string present. This results in null being converted to 0

	D. '3' + null = '3null'
		- The + here resresets string concatenation, thus null is converted to
		  teh string "null"

	E. true + 3 = 4
		- The + here represents numerical addition. The boolean value true us thus
		  converetd to its numerical representation of 1

	F. false + null = 0
		- The + here represents the addition operation. To allow this, the boolean
		  false is converted to its numerical representation, 0, and null is also
		  converted to its numerical representation, 0.

	G. '3' + undefined = '3undefined'
		- The + here represents the string concatenation operation. undefined is
		  converted to a string, "undefined" to allow this operation.

	H. '3' - undefined = NaN
		- This results NaN or Not-a-Number because the - operation is not
		  defined for string types and undefined does not have a numerical
		  representation (it is represented as NaN if required to be a numeral)
		  this resulting in an undefiend operation.

### Comparison

14. 
	A. '2' > 1 = true
		- The string, '2' is convereted to a number and is compared to the
		  number 1. Since 2 is greater than 1, this returns true.

	B. '2' < '12' = false
		- This returns false since strings comparions are done character by
		  character. This, therfore, comapres the characters '2' and '1' first
		  and since '2' is not less than '1', it returns false.

	C. 2 == '2' = true
		- The string '2' is converted to a number and when compared with the
		  integer, 2, it is equal thus returning true.

	D. 2 === '2' = false
		- The strict equality operator does not allow type conversions and since
		  2 and '2' are different datatypes, they are not equal and thus the
		  comparison returns false.

	E. true == 2 = false
		- true in numeral representation is 1. Since 1 is not equal to 2, this
		  returns false.

	F. true === Boolean(2) = true
		- The `Boolean()` function converts all non-empty values to true. Since
		  2 is not an empty value, it is converted to true and thus the
		  comparison returns false.

15. The difference between teh two types of equality comparisons is that `==`
	allows for type conversions whereas `===` is a strict equality and does not
	allow type conversions. Therefore, two values which are of different
	datatypes but could convert to the same value would be shown as equal by
	`==` but not by `===`.

### Functions

17.  Calling the function as mentioned modifies the input array by multiplying
	 each entry by 2 and returns a new array with these modified values. The for
	 loop iterates through the input array, calls teh function `doSomething` for
	 each element which returns the input element multiples by 2, and
	 pushes it into the new Array.The returned value is `[2, 4, 6]`.

### setInterval(), setTimeout(), clearTimeout()

19. The output of the code is:
	`1
	3
	4
	2'

	This is because as we enter the function, line 2 prints 1. Line 2 then sets
	a 1 second timer to print 2 after the timer ends. The next two lines are run
	before this timer ends so 2 is printed at the end. Line 4 uses the same
	timeout function but sets this timeout to 0, effectively printing the value
	immediately. Line 5 also prints 4 immediately thus resulting in the above
	mentioned output.


