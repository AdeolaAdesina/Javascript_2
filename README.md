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

![Screenshot_149](https://user-images.githubusercontent.com/29931071/200634357-cacc0bdc-8ff3-423e-973f-16eb704eda29.png)


