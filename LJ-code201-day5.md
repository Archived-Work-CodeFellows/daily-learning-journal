# Learning Journal Entry 3 - class 201 - Day 5

Notes to write about:
CSS Layout
Functions
Scope

This week we talked more about CSS layout, functions and the idea of variable scope. The CSS talk was really useful as it started to clear up more about how the box model works and how the different elements flow with one another. CSS is kinda still a bit hazy but now knowing that order is from top to bottom, I am starting to grasp more about the concepts. Now the next step for me is to think more about how I want to design a site and experiment with the different boxes.

I am pretty comfortable with functions as I do have previous experience with them but it is always nice to have a refresher as it solidifies the basic concepts. Same with scope but I didn't consider the idea of how it affects the memory as the user is on the page. It'll be fun to implement functions.

##Functions and Scope
***

Functions allow for reuseable code that can be called on when needed rather than creating repetitive and clunky code. These functions can also make the debugging easier for bigger projects.

```javascript
function name() {
    //magic code
}

name();
```

Above is the basic construction of a function. You declare a function by typing the reserved word function and then writing a name for it. Make sure the name is relatable otherwise it could backfire and make debugging harder in the future. After you declare the function, inside of the curly brackets you start writing your statements that will be executed when you call the function.

Another example:

```javascript
function hello() {
    var greeting = console.log('Hello!');
    return greeting;
}

hello();
```

That function is called hello. Inside of this function called hello, there is a code statement. This statement is a console.log and that is going to print out the string hello. After that function we need to actually initialize the function and we do so by typing hello(). 

Inside of these functions can be complex statements that we can reuse but don't have to retype. We can even pass in arguments to have affects in the function

```javascript
var message = 'hello';

function greeting(hello){
    console.log(hello);
}

greeting(message);
```

Now, instead of the function being hard coded to only say hello, we have now designed a function that we can pass in a string to change what gets printed in the console.

Now that we've built a simple function, lets talk about scope. In the first hello function, we have a variable called greeting. This variable has a local scope. What that means is that the variable greeting only exists inside of the function. The interpreter cannot use that variable unless the code inside of the statement changes. 

The next example, there is a variable called message outside of the function greeting. This message is on a Global Scope. This variable can be manipulated and is stored outside and other functions and statements can be use this variable how ever they choose. 