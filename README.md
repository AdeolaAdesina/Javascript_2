# Javascript_2 Variables


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

