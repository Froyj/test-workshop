# Simple calculator

## Learn to code a simple calculator using Javascript

#### Introduction

The purpose of this workshop is to guide you through the following core fundamentals in JavaScript via building a Calculator.

#### Concepts

During this workshop, we will learn to manipulate :

* Variables
* Operators
* Types
* Control structures

#### Starting point

Complete the following steps to have the project starting point on your local machine using any terminal of your choice.

* Create a new folder "simple-calculator" and create an empty index.html file.
* Add a HTML 5 structure to this file and open it with you favorite IDE (aka. Visual Studio Code).
* In the `<body>`, add a `<script>` tag with the code `console.log('Hello world');`

Open the index.html file in a browser, open the Console and verify that you can read 'Hello world'. When it's the case, remove the "console.log('Hello world');" line

**You are ready to start !**

Here what it should look like :

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calculator</title>
</head>
<body>
  <script>
    
  </script>  
</body>
</html>
```

#### Variables

* They must start with a letter, recommended to start with a lowercase letter.
* When naming variables use the **camelCase naming convention**.
* Declare a variable with **var**, **let** or **const**.
* Assign a value to the variable using the ‘**=**’ operator.
* They can be of multiple **datatypes** (*string*, *array*, etc …)

**Example :**

```Javascript
// the user is authentified
let isUserAuthentufied = true;

// the total invoice
let totalInvoice =  450.45
```

Now let's back to our index.html, to make this calculator work we're going to need some variables.

* Create 3 variables called operand, firstValue and secondValue, assign them the values of "+" for operand, 1 for firstValue and 2 for secondValue.
* Add three console.log for firstValue, secondValue and operand 
* What are the prints of the three previous logs?
* Now, instead of assigning values to variables, you will use the prompt function to ask the value to the user, eg: `const value = prompt('Enter you value');`
* What are the prints of the three previous logs?



```Html
<script>
  let firstValue = prompt('First value:');
  let secondValue = prompt('Second value:');
  let operand = prompt('Operand:');

  console.log(firstValue);
  console.log(secondValue);
  console.log(operand);
</script>
```

#### Operators

* Arithmetic operators are used to calculate expressions.
* **Comparison** operators allow you to **compare** two expressions. They return the **boolean** corresponding to the result of the comparison.
* **Logic** operators are used to **validate or deny** Boolean expressions.
* Assignment operators are used to change the value of a variable.

**Example:**

```Javascript
let firstValue = 5;
let secondValue = 10;

let sum = firstValue + secondValue;
let substract = firstValue - secondValue;
let multiplication = firstValue * secondValue;
let division = firstValue / secondValue;
```

Back to our calculator :

* Remove the three console.log(...) from your code
* Add a console.log of firstValue + secondValue: what is the print?
* Why?
* Convert the values from string to number with the function parseInt, eg: `value = parseInt(value);`
* Now what is the print of the log?

```html
<script>
  let firstValue = prompt('First value:');
  firstValue = parseInt(firstValue);
  let secondValue = prompt('Second value:');
  secondValue = parseInt(secondValue);
  let operand = prompt('Operand:');

  console.log(firstValue + secondValue);
</script>
```


#### Control Structure

* They are used to **control the flow** of a part of a program.
* They can also be used to control a flow **inside** or **outside** of a function.
* The block of code **inside** the if or else section is only executed **if the condition is true**
* Some examples are the following: 
  * if … else, 
  * switch/case,
  * while loop,
  * do while loop,
  * for loop

**Example: **
```javascript
const balance = 50;

//50 is greater than 0 => The condition is truthy.
if (baleance >= 0) {
  //Executes this statement
  console.log("Your balance is positive.");
} else {
  // Do not execute this statement
  console.log("Your balance is negative");
}

// expected output:  Your balance is positive
```

Getting back to our index.html file, our goal is to create a function to make an operation which changes according to the operator that has been entered in the prompt.

* Remove the previous console.log(...) from your code
* Now you will add a condition on the value of the operator : 
  * First you will test if the operation is equals to "+". If so, do a console.log of firstValue + secondValue.
  * Then, in any other case, do a console.log of firstValue - secondValue.

```html
<script>
  let firstValue = prompt('First value:');
  firstValue = parseInt(firstValue);
  let secondValue = prompt('Second value:');
  secondValue = parseInt(secondValue);
  let operand = prompt('Operand:');

  if (operand === '+') {
    console.log(firstValue + secondValue);
  } else {
    console.log(firstValue - secondValue);
  }
</script>
```


* Now, modify your code in order to use the "switch/case" control structure, and add conditions on "+", "-", "*" and "/".
* In each case, log the corresponding mathematical operation.
* Add a default case which logs "Invalid operator".

```html
<script>
  let firstValue = prompt('First value:');
  firstValue = parseInt(firstValue);
  let secondValue = prompt('Second value:');
  secondValue = parseInt(secondValue);
  let operand = prompt('Operand:');


  switch (operand) {
    case '+':
      console.log(firstValue + secondValue);
      break;
    case '-':
      console.log(firstValue - secondValue);
      break;
    case '*':
      console.log(firstValue * secondValue);
      break;
    case '/':
      console.log(firstValue / secondValue);
      break;
    default:
      console.log('Invalid operator');
  }
  if (operand === '+') {
    console.log(firstValue + secondValue);
  } else {
    console.log(firstValue - secondValue);
  }
</script>
```

Good job, through this step-by-step workshop you coded a simple calculator !

Now let's reuse all we have seen here through another exercise...

#### Challenge : The Price is Right

You have to code a simple program covering the followings :
* **Ask the player's name**
* **Store a random number** between 1 and 100
* **Ask a number** to the player (between 1 and 100)
* If the player's number is **over** the stored value, log **"It's less"**
* If the player's number is **under** the stored value, log **"It's more"**
* If the player's number **equals** the stored value, log **"*$player* wins"** (where *$player* is replaced by the player's name)
* **Repeat** these instructions until the players win, or if it takes more than 5 rounds
*  If the player **didn't found** the right price, log **"Game Over"**
