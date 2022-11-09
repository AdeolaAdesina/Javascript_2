# Javascript_2 Variables and Conditionals


# Variables

In programming, a variable is a container for a value. 

You can think of variables as little containers for information that live in a computer’s memory. Information stored in variables, such as a username, account number, or even personalized greeting can then be found in memory.

In short, variables label and store data in memory. There are only a few things you can do with variables:

- Create a variable with a descriptive name.
- Store or update information stored in a variable.
- Reference or “get” information stored in a variable.


In this lesson, we will cover how to use the ```var```, ```let```, and ```const``` keywords to create variables.

# Create a Variable: var

There were a lot of changes introduced in the ES6 version of JavaScript in 2015. One of the biggest changes was two new keywords, ```let``` and ```const```, to create, or declare, variables. 

Prior to the ES6, programmers could only use the ```var``` keyword to declare variables.

```
var myName = 'Arya';
console.log(myName);
// Output: Arya
```

Let’s consider the example above:

- 1. var, short for variable, is a JavaScript keyword that creates, or declares, a new variable.

- 2. myName is the variable’s name. Capitalizing in this way is a standard convention in JavaScript called camel casing

- 3. = is the assignment operator. It assigns the value ('Arya') to the variable (myName)

- 4. 'Arya' is the value assigned (=) to the variable myName. 

- 5. After the variable is declared, the string value 'Arya' is printed to the console by referencing the variable name: console.log(myName).


There are a few general rules for naming variables:

- Variable names cannot start with numbers.
- Variable names are case sensitive, so myName and myname would be different variables. It is bad practice to create two variables that have the same name using        different cases.
- Variable names cannot be the same as keywords. For a comprehensive list of keywords check out MDN’s keyword documentation.


## Class work

1. Declare a variable named favoriteFood using the var keyword and assign to it the string 'pizza'.

2. Declare a variable named numOfSlices using the var keyword and assign to it the number 8.

3. Under the numOfSlices variable, use console.log() to print the value saved to favoriteFood.

On the following line, use console.log() to print the value saved to numOfSlices.


Solution:

![Screenshot_150](https://user-images.githubusercontent.com/29931071/200634622-524bab26-6bd1-46bb-a356-ae483a28cf03.png)


# Create a Variable: let

As mentioned in the previous exercise, the let keyword was introduced in ES6. 

The let keyword signals that the variable can be reassigned a different value. Take a look at the example:

```
let meal = 'Enchiladas';
console.log(meal); // Output: Enchiladas
meal = 'Burrito';
console.log(meal); // Output: Burrito
```

Another concept that we should be aware of when using let (and even var) is that we can declare a variable without assigning the variable a value. 

In such a case, the variable will be automatically initialized with a value of undefined:

```
let price;
console.log(price); // Output: undefined
price = 350;
console.log(price); // Output: 350
```


Notice in the example above:

If we don’t assign a value to a variable declared using the let keyword, it automatically has a value of undefined.
We can reassign the value of the variable.


## Class work

1. Create a let variable called changeMe and set it equal to the boolean true.

2. On the line after changeMe is declared, set the value of changeMe to be the boolean false.

To check if changeMe was reassigned, log the value saved to changeMe to the console.

Solution:

![Screenshot_151](https://user-images.githubusercontent.com/29931071/200635696-cf6eab8e-8914-488f-87b4-aa96e1ee33be.png)



# Create a Variable: const

The const keyword was also introduced in ES6, and is short for the word constant. 

Just like with var and let you can store any value in a const variable. 

The way you declare a const variable and assign a value to it follows the same structure as let and var. Take a look at the following example

```
const myName = 'Gilberto';
console.log(myName); // Output: Gilberto
```

However, a const variable cannot be reassigned because it is constant. If you try to reassign a const variable, you’ll get a TypeError.

Constant variables must be assigned a value when declared. If you try to declare a const variable without a value, you’ll get a SyntaxError.


## Class work

1. Create a constant variable named entree and set it to equal to the string 'Enchiladas'.

2. Just to check that you’ve saved the value of 'Enchiladas' to entree, log the value of entree to the console.

3. Great, let’s see what happens if you try to reassign a constant variable.

Paste the following code to the bottom of your program.

```
entree = 'Tacos'
```

This code throws the typeerror error when you run your code.

Solution:

![Screenshot_152](https://user-images.githubusercontent.com/29931071/200636840-e7d80a39-672f-4df3-b7a3-e1ea683395bb.png)


# Mathematical Assignment Operators

Let’s consider how we can use variables and math operators to calculate new values and assign them to a variable. Check out the example below:

```
let w = 4;
w = w + 1;
console.log(w); // Output: 5
```


Another way we could have reassigned w after performing some mathematical operation on it is to use built-in mathematical assignment operators. We could re-write the code above to be:

```
let w = 4;
w += 1;
 
console.log(w); // Output: 5
```

We also have access to other mathematical assignment operators: ```-=```, ```*=```, and ```/=``` which work in a similar fashion.


```
let x = 20;
x -= 5; // Can be written as x = x - 5
console.log(x); // Output: 15
 
let y = 50;
y *= 2; // Can be written as y = y * 2
console.log(y); // Output: 100
 
let z = 8;
z /= 2; // Can be written as z = z / 2
console.log(z); // Output: 4
```

## Class work

1. Use the += mathematical assignment operator to increase the value stored in levelUp by 5.

```let levelUp = 10;```

2 Use the -= mathematical assignment operator to decrease the value stored in powerLevel by 100.

```let powerLevel = 9001;```

Solution:

![Screenshot_153](https://user-images.githubusercontent.com/29931071/200642224-03d49839-d475-43ff-bf58-fab13cdeb71c.png)



# The Increment and Decrement Operator

Other mathematical assignment operators include the increment operator ```(++)``` and decrement operator ```(--)```.

The increment operator will increase the value of the variable by 1. The decrement operator will decrease the value of the variable by 1. For example:

```
let a = 10;
a++;
console.log(a); // Output: 11

let b = 20;
b--;
console.log(b); // Output: 19
```


## Class work

```
let gainedDollar = 3;
let lostDollar = 50;
```

1. Using the increment operator, increase the value of gainedDollar.

2. Using the decrement operator, decrease the value of lostDollar.

Solution:

![Screenshot_154](https://user-images.githubusercontent.com/29931071/200639404-ce8a4149-4d4a-40f4-b920-3e5d21192872.png)



# String Concatenation with Variables

In previous exercises, we assigned strings to variables. Now, let’s go over how to connect, or concatenate, strings in variables.

The ```+``` operator can be used to combine two string values even if those values are being stored in variables:

```
let myPet = 'armadillo';
console.log('I own a pet ' + myPet + '.'); 
// Output: 'I own a pet armadillo.'
```

## Class work

1. Create a variable named favoriteAnimal and set it equal to your favorite animal.

2. Use console.log() to print 'My favorite animal: ANIMAL' to the console. Use string concatenation so that ANIMAL is replaced with the value in your favoriteAnimal variable.

Solution:

![Screenshot_155](https://user-images.githubusercontent.com/29931071/200640418-f1205ed6-16c6-4cea-b7c2-e9744c02bc7c.png)


# String Interpolation

In the ES6 version of JavaScript, we can insert, or interpolate, variables into strings using template literals. Check out the following example where a template literal is used to log strings together:

```
const myPet = 'armadillo';
console.log(`I own a pet ${myPet}.`);
// Output: I own a pet armadillo.
```

Notice that:

- a template literal is wrapped by backticks ` (this key is usually located on the top of your keyboard, left of the 1 key).
- Inside the template literal, you’ll see a placeholder, ${myPet}. The value of myPet is inserted into the template literal.
- When we interpolate `I own a pet ${myPet}.`, the output we print is the string: 'I own a pet armadillo.'

## Class work

1. Create a variable called myName and assign it your name.

2. Create a variable called myCity and assign it your favorite city’s name.

3. Use a single template literal to interpolate your variables into the sentence below. Use console.log() to print your sentence to the console in the following format:

```
My name is NAME. My favorite city is CITY.
```

Solution:

![Screenshot_156](https://user-images.githubusercontent.com/29931071/200641546-50be08a7-fe86-4761-a96b-ec35c7e851a3.png)


# typeof operator

While writing code, it can be useful to keep track of the data types of the variables in your program. If you need to check the data type of a variable’s value, you can use the typeof operator.

The typeof operator checks the value to its right and returns, or passes back, a string of the data type.

```
const unknown1 = 'foo';
console.log(typeof unknown1); // Output: string
 
const unknown2 = 10;
console.log(typeof unknown2); // Output: number
 
const unknown3 = true; 
console.log(typeof unknown3); // Output: boolean
```



# Conditional statements


In life, we make decisions based on circumstances. Think of an everyday decision as mundane as falling asleep — if we are tired, we go to bed, otherwise, we wake up and start our day.

These if-else decisions can be modeled in code by creating conditional statements. A conditional statement checks a specific condition(s) and performs a task based on the condition(s).

In this lesson, we will explore how programs make decisions by evaluating conditions and introduce logic into our code!

We’ll be covering the following concepts:

- if, else if, and else statements
- comparison operators
- logical operators
- truthy vs falsy values
- ternary operators
- switch statement


# If statement

If Statement
We often perform a task based on a condition. For example, if the weather is nice today, then we will go outside. If the alarm clock rings, then we’ll shut it off. If we’re tired, then we’ll go to sleep.

In programming, we can also perform a task based on a condition using an if statement:

```
if (true) {
  console.log('This message will print!'); 
}
// Prints: This message will print!
```

Notice in the example above, we have an if statement. The if statement is composed of:

- The if keyword followed by a set of parentheses ```()``` which is followed by a code block, or block statement, indicated by a set of curly braces ```{}```.
- Inside the parentheses (), a condition is provided that evaluates to true or false.
- If the condition evaluates to true, the code inside the curly braces {} runs, or executes.
- If the condition evaluates to false, the block won’t execute.

Let’s make an if statement.

## Class work

1. Using the let keyword, declare a variable named sale. Assign the value true to it.

2. Now create an if statement. Provide the if statement a condition of sale.

Inside the code block of the if statement, console.log() the string 'Time to buy!'.

Output:

![Screenshot_157](https://user-images.githubusercontent.com/29931071/200800450-ec657871-695f-49b8-bbd8-94101c6349f6.png)



# If...Else Statements

In the previous exercise, we used an if statement that checked a condition to decide whether or not to run a block of code. In many cases, we’ll have code we want to run if our condition evaluates to false.

If we wanted to add some default behavior to the if statement, we can add an else statement to run a block of code when the condition evaluates to false. Take a look at the inclusion of an else statement:

```
if (false) {
  console.log('The code in this block will not run.');
} else {
  console.log('But the code in this block will!');
}
 
// Prints: But the code in this block will!
```

An else statement must be paired with an if statement, and together they are referred to as an if...else statement.


## Class work

Add an else statement to the existing if statement. Inside the code block of the else statement, console.log() the string 'Time to wait for a sale.'

Output:

![Screenshot_158](https://user-images.githubusercontent.com/29931071/200801079-3301463a-030f-41c6-83c5-2c8a89ed1385.png)



# Comparison Operators

When writing conditional statements, sometimes we need to use different types of operators to compare values. These operators are called comparison operators.

Here is a list of some handy comparison operators and their syntax:

- Less than: <
- Greater than: >
- Less than or equal to: <=
- Greater than or equal to: >=
- Is equal to: ===
- Is not equal to: !==

We can also use comparison operators on different data types like strings:

```
'apples' === 'oranges' // false
```

In the example above, we’re using the identity operator ```(===)``` to check if the string 'apples' is the same as the string 'oranges'. Since the two strings are not the same, the comparison statement evaluates to false.

All comparison statements evaluate to either TRUE or FALSE and are made up of:

- Two values that will be compared.
- An operator that separates the values and compares them accordingly (>, <, <=,>=,===,!==).

Let’s practice using these comparison operators!

## Class work

1. Using let, create a variable named hungerLevel and set it equal to 7.

2. Write an if...else statement using a comparison operator. The condition should check if hungerLevel is greater than 7. If so, the conditional statement should log, 'Time to eat!'. Otherwise, it should log 'We can eat later!'.

Output:

![Screenshot_159](https://user-images.githubusercontent.com/29931071/200802124-0754d504-4a09-422a-bd38-e0fa369bd230.png)


# Logical Operators

Working with conditionals means that we will be using booleans, true or false values. 

In JavaScript, there are operators that work with boolean values known as logical operators. We can use logical operators to add more sophisticated logic to our conditionals. There are three logical operators:

- the and operator (&&)
- the or operator (||)
- the not operator, otherwise known as the bang operator (!)

When we use the && operator, we are checking that two things are true:

```
if (stopLight === 'green' && pedestrians === 0) {
  console.log('Go!');
} else {
  console.log('Stop');
}
```

If we only care about either condition being true, we can use the || operator:

```
if (day === 'Saturday' || day === 'Sunday') {
  console.log('Enjoy the weekend!');
} else {
  console.log('Do some work.');
}
```

The ! not operator reverses, or negates, the value of a boolean:

```
let excited = true;
console.log(!excited); // Prints false
 
let sleepy = false;
console.log(!sleepy); // Prints true
```

## Class work

In app.js there are two variables mood and tirednessLevel.

```
let mood = 'sleepy';
let tirednessLevel = 6;
```

Let’s create an if...else statement that checks if mood is 'sleepy' and tirednessLevel is greater than 8.

If both conditions evaluate to true, then console.log() the string 'time to sleep'. Otherwise, we should console.log() 'not bed time yet'.


Output:

![Screenshot_160](https://user-images.githubusercontent.com/29931071/200803016-4cb4011a-1679-48c9-8c9d-2f9323cceb4f.png)


After you press “Run”, play around with the || operator and the ! operator! What happens if you negate the value of the entire statement with ! and switch to || instead of &&?



# Truthy and Falsy

Let’s consider how non-boolean data types, like strings or numbers, are evaluated when checked inside a condition.

Sometimes, you’ll want to check if a variable exists and you won’t necessarily want it to equal a specific value — you’ll only check to see if the variable has been assigned a value.

Here’s an example:

```
let myVariable = 'I Exist!';
 
if (myVariable) {
   console.log(myVariable)
} else {
   console.log('The variable does not exist.')
}
```

The code block in the if statement will run because myVariable has a truthy value; even though the value of myVariable is not explicitly the value true, when used in a boolean or conditional context, it evaluates to true because it has been assigned a non-falsy value.

So which values are falsy— or evaluate to false when checked as a condition? The list of falsy values includes:

- 0
- Empty strings like "" or ''
- null which represent when there is no value at all
- undefined which represent when a declared variable lacks a value
- NaN, or Not a Number

Here’s an example with numbers:

```
let numberOfApples = 0;
 
if (numberOfApples){
   console.log('Let us eat apples!');
} else {
   console.log('No apples left!');
}
 
// Prints 'No apples left!'
```

## Class work

```
let wordCount;

if (wordCount) {
  console.log("Great! You've started your work!");
} else {
  console.log('Better get to work!');
}


let favoritePhrase;

if (favoritePhrase) {
  console.log("This string doesn't seem to be empty.");
} else {
  console.log('This string is definitely empty.');
}
```

1. Change the value of wordCount so that it is truthy. This value should still be a number.

After you make this change and run your code, 'Great! You've started your work!' should log to the console.

2. Change the value of favoritePhrase so that it is still a string but falsy.

After you make this change and run your code, 'This string is definitely empty.' should log to the console.

Output:

![Screenshot_161](https://user-images.githubusercontent.com/29931071/200804089-dd163927-587e-46be-b221-24338ab03d35.png)


# Truthy and Falsy Assignment

Truthy and falsy evaluations open a world of short-hand possibilities!

Say you have a website and want to take a user’s username to make a personalized greeting. Sometimes, the user does not have an account, making the username variable falsy. The code below checks if username is defined and assigns a default string if it is not:

```
let username = '';
let defaultName;
 
if (username) {
  defaultName = username;
} else {
  defaultName = 'Stranger';
}
 
console.log(defaultName); // Prints: Stranger
```

If you combine your knowledge of logical operators you can use a short-hand for the code above. In a boolean condition, JavaScript assigns the truthy value to a variable if you use the || operator in your assignment:

```
let username = '';
let defaultName = username || 'Stranger';
 
console.log(defaultName); // Prints: Stranger
```

Because || or statements check the left-hand condition first, the variable defaultName will be assigned the actual value of username if it is truthy, and it will be assigned the value of 'Stranger' if username is falsy. 

This concept is also referred to as short-circuit evaluation.


## Class work

```
let tool = 'marker';

// Use short circuit evaluation to assign  writingUtensil variable below:
let writingUtensil;
```

1. Let’s use short-circuit evaluation to assign a value to writingUtensil. Do not edit tool yet, we’ll return to tool in the next step.

Assign to writingUtensil the value of tool and if tool is falsy, assign a default value of 'pen'.

2. Notice that text 'The pen is mightier than the sword' logged to the console. Which means the value of writingUtensil is 'pen'.

What if we reassign the value of tool to 'marker'. Let’s see what happens to the value of writingUtensil.

3. Now make tool falsy and see the difference.


Output:

![Screenshot_162](https://user-images.githubusercontent.com/29931071/200806129-3c5a9538-06d5-4d3b-802e-28874a0ce835.png)

![Screenshot_163](https://user-images.githubusercontent.com/29931071/200806272-bce76c41-6de0-4e87-9364-f087b66ffdaa.png)


# Ternary Operator

In the spirit of using short-hand syntax, we can use a ternary operator to simplify an if...else statement.

Take a look at the if...else statement example:

```
let isNightTime = true;
 
if (isNightTime) {
  console.log('Turn on the lights!');
} else {
  console.log('Turn off the lights!');
}
```

We can use a ternary operator to perform the same functionality:

```
isNightTime ? console.log('Turn on the lights!') : console.log('Turn off the lights!');
```

In the example above:

- The condition, isNightTime, is provided before the ?.
- Two expressions follow the ? and are separated by a colon :.
- If the condition evaluates to true, the first expression executes.
- If the condition evaluates to false, the second expression executes.


## Class work

1. 

```
let isLocked = false;

if (isLocked) {
  console.log('You will need a key to open the door.');
} else {
  console.log('You will not need a key to open the door.');
}
```

Refactor, or edit, the first if...else block to use a ternary operator.

Output:

![Screenshot_164](https://user-images.githubusercontent.com/29931071/200807974-b56f57d2-9ff6-4cc6-acab-d0fa584cc299.png)


2.

```
let isCorrect = true;

if (isCorrect) {
  console.log('Correct!');
} else {
  console.log('Incorrect!');
}
```

Refactor the second if...else block to use a ternary operator.

Output:

![Screenshot_165](https://user-images.githubusercontent.com/29931071/200808483-6e0abcd0-8e56-4f63-8708-04cc1adae732.png)



# Else If Statements

We can add more conditions to our if...else with an else if statement. The else if statement allows for more than two possible outcomes. You can add as many else if statements as you’d like, to make more complex conditionals!

The else if statement always comes after the if statement and before the else statement. The else if statement also takes a condition. Let’s take a look at the syntax:

```
let stopLight = 'yellow';
 
if (stopLight === 'red') {
  console.log('Stop!');
} else if (stopLight === 'yellow') {
  console.log('Slow down.');
} else if (stopLight === 'green') {
  console.log('Go!');
} else {
  console.log('Caution, unknown!');
}
```

The ```else``` if statements allow you to have multiple possible outcomes. if/else if/else statements are read from top to bottom, so the first condition that evaluates to true from the top to bottom is the block that gets executed.


## Class work

```
let season = 'summer';

if (season === 'spring') {
  console.log('It\'s spring! The trees are budding!');
} else {
  console.log('Invalid season.');
}
```

1. In app.js there is already an if...else statement in place. Let’s add an else if statement that checks if season is equal to 'winter'.

Inside the code block of the else if statement, add a console.log() that prints the string 'It\'s winter! Everything is covered in snow.'.

Output:

![Screenshot_166](https://user-images.githubusercontent.com/29931071/200809985-9cb3ce8e-352c-4d1c-9b35-bde7d7061389.png)


2. Add another else if statement that checks if season is equal to 'fall'.

Inside the code block of the else if statement you just created, add a console.log() that prints the string 'It\'s fall! Leaves are falling!'.

Output:

![Screenshot_167](https://user-images.githubusercontent.com/29931071/200810648-8891510d-bb03-41d8-aa82-bcd5af97cdef.png)



# The switch keyword

else if statements are a great tool if we need to check multiple conditions. In programming, we often find ourselves needing to check multiple values and handling each of them differently. For example:

```
let groceryItem = 'papaya';
 
if (groceryItem === 'tomato') {
  console.log('Tomatoes are $0.49');
} else if (groceryItem === 'papaya'){
  console.log('Papayas are $1.29');
} else {
  console.log('Invalid item');
}
```

A switch statement provides an alternative syntax that is easier to read and write. A switch statement looks like this:

```
let groceryItem = 'papaya';
 
switch (groceryItem) {
  case 'tomato':
    console.log('Tomatoes are $0.49');
    break;
  case 'lime':
    console.log('Limes are $1.49');
    break;
  case 'papaya':
    console.log('Papayas are $1.29');
    break;
  default:
    console.log('Invalid item');
    break;
}
 
// Prints 'Papayas are $1.29'
```


## Class work

```
let athleteFinalPosition = 'first place';
```


1. Let’s write a switch statement to decide what medal to award an athlete.

athleteFinalPosition is already defined at the top of app.js. So start by writing a switch statement with athleteFinalPosition as its expression.

Output:

```
let athleteFinalPosition = 'first place';

switch (athleteFinalPosition) {
  
}
```

2. Inside the switch statement, add three cases:

The first case checks for the value 'first place'
If the expression’s value matches the value of the case then console.log() the string 'You get the gold medal!'
The second case checks for the value 'second place'
If the expression’s value matches the value of the case then console.log() the string 'You get the silver medal!'
The third case checks for the value 'third place'
If the expression’s value matches the value of the case then console.log() the string 'You get the bronze medal!'
Remember to add a break after each console.log().


Output:

![Screenshot_168](https://user-images.githubusercontent.com/29931071/200812350-88ad8a65-b242-4b85-bcd4-83ba1545d334.png)

3. Now, add a default statement at the end of the switch that uses console.log() to print 'No medal awarded.'.

If athleteFinalPosition does not equal any value of our cases, then the string 'No medal awarded.' is logged to the console.

Remember to add the break keyword at the end of the default case.

Output:

![Screenshot_169](https://user-images.githubusercontent.com/29931071/200812800-682dd6cf-5129-4a3d-88c3-7dbadfa44a12.png)

