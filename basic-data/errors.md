# Errors

Your program will have errors. In fact, errors are an intrinsic part of developing software for everyone, not just begginers.

Let's talk about a few kinds of errors you might have seen so far.

Errors in your program will appear in the dev tools console.

Access the dev tools console by going to the top level menu and selecting view -&gt; developer -&gt; javascript console.

You should never code anything in the browser without having this pane open, otherwise you might not catch some errors.

You should always make sure either your page loaded with the tools already, or you reload the page after opening the dev tools or some errors might not get displayed.

There are 2 broad categories of errors. We can use the dev tools to fix both kinds.

## 1. Syntax errors / runtime errors

These are errors where you will see red text in the console.

Syntax errors can be divided into 2 kinds:

a. compilation errors - javascript looks at your code file for the first time and sees some syntax error that it can't move past.

Let's introduce a syntax error into your program.

Replace your `kilometersToMiles` function with the one below.

```javascript
var kilometersToMiles = function distanceInKilometers){

  var distanceInMiles = distanceInKilometers * 0.62;

  return distanceInMiles;
};
```

You'll get the error: `Uncaught SyntaxError: Unexpected token ')'`. This may look cryptic, but once you see this error a few times \( and you definitely will \) you'll understand what it is trying to tell you.

FIrst of all, the console is helpfully telling you which line of your code the error is occuring on.

Specifically in this case the error was a missing parenthese. Javascript knew because of the `function` keyword that a function was about to be defined. It was waiting for an opening left parenthese. When it found a right parenthese it knew for sure that something was wrong.

There are some spcific rules about why javascript can't know that a left parenthese was missing \( rather than a right parenthese is incorrect \) which are outside the scope of this course, but in practice, unfortunately, you as the programmer will have to know that "I didn't expect a right parenthese" infers that it was looking for a left parenthese.

A significant amount of the feedback you will get from the computer will be these semi-cryptic messages about why your code is wrong.

b. runtime errors - errors that happen when you run your porogram.

Replace this line in the starter code:

```javascript
var myOutputValue = "hello world"()
```

You will see when you refresh the page that there is no red text.

Now click the submit button.

You'll get the error `Uncaught TypeError: "hello world" is not a function`. This is because there is a set of parentheses `()` instead of a semi-colon `;`.

Specifically javascript thinks the parentheses mean that you want to run some kind of function. This error isn't too common, but notice that for this type of error, javascript didn't let you know until it tried to run the code.

## 2. logical / control errors

Some of the errors your program will have will not produce any red output on the console.

Replace your main function with this code:

```javascript
var main = function(input) {

  var myOutputValue = kilometersToMiles(input);

  myOutputValue;
};
```

This `main` function is missing the `return` keyword. Without it we can see the value output by the `main` function is the value `undefined`.

This code does not have any javascript _syntax_ errors - it is considered by the computer to be valid javascript code, but it does not **behave** the way we want.

## debugging

Debugging is the process of diagnosing and fixing the errors you have in your program.

The debugging process can be relatively simple, in the case of type 1.a errors - syntax errors - javascript gives you red text in the console and you must start by going to the line that is mentioned in the console and then interpreting the true meaning of the error text given to you.

Debugging can become more complicated when you are trying to diagnose a logical error in your code- the computer is running the code without errors, but the behavior is not correct.

We'll talk about a few strategies you can use to diagnose and correct errors.

1. control flow checking - is our code even runnning?

Functions give us the ability to execute code in a certain order, from certain places in our code that we specify. If something in our code seems incomplete or wrong, one of the first things we can check is to see if it is running at all.

### console.log

`console.log()` is a function that we can run that will make text appear in the developer tools.

The thing we want to appear is passed an argument to `console.log` like so: `console.log("bananas!")`

Try writing some `console.log`s in all of the different structures of your code. Each `console.log` statement should be descriptive of where in the code you are. Also be careful not to make any errors here and describe something incorrectly!

We can use the fact that text is appearing in the dev tools console as an implicit signal that javascript it executing our code.

If our `console.log` statement appears in the dev tools console then we know that our code is reachable by opur program.

1. value checking - is the value correct?

Another way we can use `console.log` is to pass it the variable values our program deals with.

Are the values in our program the ones we expect?

As below we can pass variable values to `console.log`:

```javascript
var main = function(input) {
  var myOutputValue = "hello world";
  return myOutputValue;
};

var kilometersToMiles = function(distanceInKilometers){

  var distanceInMiles = distanceInKilometers * 0.62;

  console.log("this is distance in miles value");
  console.log(distanceInMiles);

  return distanceInMiles;
};
```
