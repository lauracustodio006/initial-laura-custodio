---
title: "FizzBuzz, chapter 2 Eloquent JavaScripte"
description: ""
omit_header_text: true
summary: "Programming article 1."
type: page
weight: 2
tags: [javascrips, problem]
---
## Introduction to the Problem
 I'm showing a problem and a solution showened in Chapter 2 of *Eloquent JavaScript* by *Marijn Haverbeke*.  See Eloquent JavaScript, Chapter 2 [here](https://eloquentjavascript.net/02_program_structure.html#p-1PXG58nhBq)

In summary, the program prints the numbers from 1 to 100, with three exceptions:

- For numbers divisible by 3, print `"Fizz"` instead of the number.  
- For numbers divisible by 5 (but not 3), print `"Buzz"`.  
- For numbers divisible by both 3 and 5 prints `"FizzBuzz"`.  

Below its the question.
<blockquote>
Write a program that uses console.log to print all the numbers from 1 to 100, with two exceptions. For numbers divisible by 3, print "Fizz" instead of the number, and for numbers divisible by 5 (and not 3), print "Buzz" instead.

When you have that working, modify your program to print "FizzBuzz" for numbers that are divisible by both 3 and 5 (and still print "Fizz" or "Buzz" for numbers divisible by only one of those).

(This is actually an interview question that has been claimed to weed out a significant percentage of programmer candidates. So if you solved it, your labor market value just went up.)
</blockquote>

# my solution:
```js
let num = 1; 
while(num <= 100) {
  if (num % 3 === 0 && num % 5 === 0){
    console.log("FizzBuzz");
  } else if (num % 3 === 0 ) { 
    console.log("Fizz"); 
  } else if (num % 5 === 0 ) { 
    console.log("Buzz"); 
  } else{
    console.log(num);
  }
  num++;
}
```
## Bind the first value
*	**Binding** defines a value to a name that can be used in an expression.*(Eloquent JavaScript chapter 2)*.
* In this case we defined the variable num to the initial value 1, since the problem requires to print the numbers from 1 to 100.
* **let** is the keywor we are using. We use **let** instead of **const** because the value of **num** changes throught the loop.

## Creating the loop
* A **loop** is a form of flow control that runs a piece of code multiple times. This will allows us to go back to some point in the program where we were before and repeat it with our current program state. *(Eloquent JavaScript chapter 2)*.
* I used a *while* loop combined with a **if statement**. Its syntax is:
>While (expression) {
>
>If  (expression) {
>
>Statement to execute
>
>} else if  (expression) {
>
>Statement to execute
>
>}}

# Step by step explanation
1. We define **num** to not be more then 100 by using the expression **num<=100**. This means the loop will continue as long as num is less or eqaul to 100.
2. The first **if statement** is to "to print "FizzBuzz" for numbers that are divisible by both 3 and 5".
```js
if (num % 3 === 0 && num % 5 === 0)
```
-  **num % 3** will gives the remainder when num is divided by 3.
- **== 0** we will check if the remainder is equal to 0, meaning that the num is divided by 3.
- **&&** means *and* so in this expression we check if both the conditions are true.
3. After the **if statement** we define a statement to execute.
```js
console.log("FizzBuzz");
```
- **Console.log ()** is a function that writes out its arguments to some text output device (eloquent JavaScript chapter 2).
- In this case it will output FizzBuzz in the device.
4. Next we do a **else if statement** that will handle the other parts of the problem. 
5. The last **else** doesn't have a **if statement** because it handles the remaining numbers, the numbers not divisible by 3 or 5. It will print the numbers itself
7. Lastly we have 
```js
  num++
  ```
- This means num = num + 1, num is increased by 1.
- This will allow the loop to continue to the next number.
