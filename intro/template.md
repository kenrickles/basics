# Basic Template / Basic Data

## Template - Our First Basic Program

Let's get started with running some code outside of the javascript console.

We'll be creating a super basic program.

**instructions**

Copy the starter code from github:

`cd` into your code directory.

```bash
cd ~/code
```

git clone the starter code:

```bash
git clone https://github.com/rocketacademy/basic-js-starter.git basic-data
```

This will create a `basic-data` directory inside your `code` directory.

`cd` into the `basic-data` directory.

```bash
cd basic-data
```

Open the `index.html` file in chrome.

**default template behavior**

The default starter code has one basic behavior.

After you open the `index.html` file in your browser, click the submit button.

This causes "hello world" to appear in the grey box.

**our own values being output**

Open the `script.js` file in your editor.

You should see the following:

```javascript
console.log("bananas");

var main = function(input){

  var myOutputValue = "hello world";

  return myOutputValue;
};
```

On line 3 we define the `main` function. The `{}` curly brance characters define the contents of this function.

Without a further formal definition we'll begin using this code to make stuff appear on the screen. \(We'll come back to the formal definitions later.\)

We are going to start with _line 5_: `myOutputValue` is a variable that holds the value that we see in the grey box after we click the button.

Change the value of the variable to something else. We'll start with numbers only:

```javascript
var myOutputValue = 2;
```

Remember to save the file and refresh the browser screen. Then you can try your changes out.

What happens when you click the button?

Try assigning a bunch of different values. See them output in the grey square.

```javascript
var myOutputValue = 12;
```

```javascript
var myOutputValue = 9999999999;
```

```javascript
var myOutputValue = 1.234234;
```

**operations as output**

Let's assign the output of our previous code to the variable:

Previously all the lines we had together look like this:

```javascript
var pi = 3.14;
var radius = 4;
var area = pi * radius * radius;
```

Let's assign our final value to the `myOutputValue` variable:

```javascript
var myOutputValue = area;
```

When we click the submit button our program is now succesfully calculating the area of a circle!

Try some other calculations. Remember to assign the final value to `myOutputValue` in order for them to appear in the grey square.

```javascript
var myOutputValue = 34534 * 2334;
```

```javascript
var myOutputValue = 12 * 12;
```

```javascript
var myOutputValue = 100 / 10;
```

## interactivity

A program needs to _take input_ and give output. So far our programs have only had input that we type in our code file, not directly from the user of `index.html`.

In the starter code we take some input by default.

What happens when you type something in the input box before you click the submit button?

We'll begin to add inputs to our program using the input box.

### `main` function parameters

We'll continue working with `functions` without formally defining them.

Our eventual goal is to create a program that takes defined inputs and gives outputs.

In our starter code, `input` is a _function parameter_ - in this case it contains the thing that was typed in the input box.

We can prove this is true simply by assigning the value of `input` to `myOutputValue` like so:

```javascript
var myOutputValue = input;
```

Now you should see that whatever you type in the input box gets put into the grey box.

### string data

`input` is always a _type_ of data called a _string_.

We'll now talk about this different kind of data inside of the javascript language and what makes it distinct from the number data we dealt with before.

\[Wikipedia\]\([https://en.wikipedia.org/wiki/String\_\(computer\_science](https://en.wikipedia.org/wiki/String_%28computer_science)\)\) defines a `string` as a _sequence of characters_.

This basically means that we are dealing with letters and words. These are defined with either single or double quotes:

```javascript
var name = "Susan";
var name2 = 'Kai';
```

Change the value of `myOutputValue` to a string value \(any set of words you want\) and see them appear in the grey box.

#### interactive messages

Let's use this string operation to make our program a little more interactive.

Change the code back again to assign the value of `input` to `myOutputValue`:

```javascript
var myOutputValue = input;
```

#### greeting program

We are going to explicitly state the purpose of our program now:

The user will type in their name, and we will use the name to greet them.

To do this we'll take `input` and combine it with some other strings to make the full output:

```javascript
var myOutputValue = "Hello " + input + " you look great today!";
```

**Further**

Change your program output to a different message. Make it longer, you can use input more than once in the output, for instance:

`Hello, Susan! Wow, Susan is a great name. Reminds me of this movie star....`

#### metric conversion program

Let's incorporate the math operations we were doing before into our program.

We'll explicitly change the purpose of our program to:

The user will enter a distance in kilometers and the program will output the distance in miles.

The formula for conversion is:

mi = km \* 0.62

So in javascript we can write it like this:

```javascript
var distanceInKilometers = 1;

var distanceInMiles = distanceInKilometers * 0.62;
```

Let's change the output so we can see the calculation on screen:

```javascript
var myOutputValue = distanceInMiles;
```

Try changing the values of `distanceInKilometers` to see the new conversion being output.

Now we can make out program interactive by letting the user enter a temperature amount.

Simply assign the value of `input` to `distanceInKilometers`.

#### Further

Other kinds of calculation operations?

#### output and format the result

Our conversion program should try to be as user friendly as possible.

This means we should try to output more than just a cryptic number in the grey square.

For example, if the user types in `5`, the progrma will output a message like:

```text
Hi! 5 kilometers is equal to 3.1 miles.
```

Simply use the result of the calculation together with some string values like we did in the greeting program:

```javascript
var myOutputValue = "Hi! "+input+" is equal to "+distanceInMiles"+ " miles.";
```

#### Further

Other kinds of formats?
