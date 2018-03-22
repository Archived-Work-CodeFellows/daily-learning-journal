# Learning Journal Entry 2 - Class 201 - Day 3-4

So far we have been going over the basics of primitive data types within Javascript. We have started out programming with developing a interactive guessing game script that takes user input. We talked about discussing problems in code speak or pseudo-code to work out how something should work or relate.

We then continued to learn about loops, arrays and the box model to further build upon out previous lab work. I still need work on my css and box model. The web languague is taking a little longer to grasp, not in terms of being difficult just knowing how things are affected and making more informative decisions to allow for faster developing.

Below I am gonna re-iterate brief things we discussed.

### pseudo-code:
***

We have gone over how to outline your problems and start thinking like developers. We need to use pseudo-code to get generalized ideas to inform the directions we want to take as we design the program.

```javascript
for(starting val; condition; increment) {
    do something for a finite number of times
}

while(true) {
    do something until condition is false;
}

do{ 
    do this at least once until the condition is false
} while (condition)
```
Those are just some examples. You can replace the filler as long as it still fits the statement and makes sense. Sometimes you know the problem but need to just write it out in a pseudo fashion to make more sense of it and then proceed to flesh it out

### loops, loops, loops
***

To build off of the pseudo-code, we started exploring three different loops:

* For
* While
* Do While

These loops are the first step that allow us to do iterative tasks without needing to repeat and create clunky code for us as well as other developers trying to read the code for debugging.

A for loop is great for specific iteration. A common use is to use it to index through an array to see all of the different indicies that live within that array.

```javascript
var foo = [1,2,3];

for(var i = 0; i < foo.length; i++) {
    console.log(foo[i]);
}
```

variable foo is an array with three elements in it. The quickest way to iterate through the array is to use a for loop. To start the for loop, you declare a variable, this time i and then create a condition. While i is less than the total length of the foo array, increment i by 1.

Inside of the loop, there is the console.log method which has the array foo[i] inside of it. This will print out each foo index until i is no longer less than foo's length. 

Instead of calling each index of foo manually (foo[0], foo[1], foo[2]) the for loop does the work for you.


While loops do the same thing, but will loop indefinitely until the conditional is false.

```javascript
var foo = [1,2,3];
var i = 0;

while (i < foo.length) {
    console.log(foo[i]);
    i++;
}
```

This while loop is doing the same thing as the previous for loop. First we declare a variable foo array with three elements. After that we declare a variable i and initialize it to zero. We start our while loop conditional which is saying while i is less than the foo array's length, print out foo[i] in the console.log method and then increment i by one. 

The while loop will continue to do this until i is no longer less than foo's length. The biggest difference between a for loop and a while loop is that for loops are for great for a finite set of iterations, the while loop is great for more flexible and uncertain amount of iterations as it will loop until it's condition is false.


Do While loops are like while loops except they will execute the block of code at least once whether the conditional is true or false.

```javascript
var foo = [1,2,3];
var i = 4;

do {
    console.log('I still get called even though var i is greater than foo.length');
    //console.log(foo[i]);
    i++;
} while (i < foo.length);
```
This Do While loop is set up to do the same as the previous two loops, but this time the variable i is initialized to 4 to show that the code within the Do block will still run even though i is already greater than the foo array length. If you change var i = 4 to var i = 0 and uncomment the console.log(foo[i]), you will see that it will count through the array just like the previous loops.

Do While loops are useful for situations where you want a block of code to run but based on what you need will determine if it needs to be iterative or not.

### Box Model
***

The box model is what is used when creating layouts for websites. It is how browsers render elements to the viewer. Each box has the four areas: content, padding, border and margin. These create your canvas that you can then manipulate with the css file.


HTML & CSS Jon Duckett:
>CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.
>If one block-level element sits inside another block-level element then the outer box is known as the containing or parent
>element

The main takeaway from this is to think about the layout as a stack of blocks. Manipulating these blocks is how we can achieve our desired layout.