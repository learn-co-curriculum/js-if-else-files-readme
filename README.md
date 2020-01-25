# Conditional Statements and Control Flow

## Objectives
1. Define control flow for when a JS program is executed.
2. Implement control flow in different ways.
3. Use `if`, `else`, and `else if` statements.

## What is Control Flow?
> A control flow construct is a language feature which disrupts the normal progression to the next statement and conditionally or unconditionally branches to another location in source code.                                
> –– [Robert Klemme](http://blog.rubybestpractices.com/posts/rklemme/004-Control_Flow.html)

In other words, control flow lets you tell your program what code to execute conditionally. As humans, we actually enact flow control *every day*. For instance, if you are hungry, you will go and get a snack. Otherwise, you'll stay put and continue to read this awesome readme.

Control flow is an important part of JS programming. In the context of a web application, for example, you can easily think of content or functionality on a website you've visited that is only available to a user *if* that user is logged in.

## Implementing Control Flow

There are a number of ways to tell your program to conditionally execute certain code. Today we are going to discuss conditional statements using `if`.


### `if` Statements

One of the most common ways to enact control flow is the `if` statement. Whatever block of code that follows the `if` statement will get evaluated—i.e. read and enacted by the computer. If this evaluation of the `if` statement results in `true`, then the code through to the associated `}` will run.

Let's look at a few examples:

```javascript
if (5 > 2) {
  console.log("5 is greater than 2")
}
```
* The code above will print "5 is greater than 2" because the `if` statement evaluates as `true`.

Meanwhile:

```javascript
if (2 > 5) {
    console.log("2 is greater than 5")
}
```
* The code above will not print anything because the `if` statement evaluates as `false`.

So what if we want our program to print something *else* when the `if` condition evaluates as `false`?

### The `else` Keyword

To accomplish this, we can follow an `if` statement with an `else` statement. Take a look:

```ruby
if (false) {
   console.log("This will never get printed because the above statement evaluates to false.")
} else {
   console.log("This will get printed!")
}
```

An `else` statement sets a "default" condition for when your `if` statement's conditional evaluates as `false`. Every condition that doesn't evaluate as `true` will instead pass through the `else` statement.

##### Further Examples

So far, we've seen `if` statements that rely on the explicit use of the `true` and `false` booleans. Let's look at some examples that require a little more thought.

###### Example 1

```javascript
if (6 + 3 === 9) {
  console.log("Giraffes have no vocal cords.")
}
```

* The code above will print `Giraffes have no vocal cords.` Since `6 + 3` equals `9` (i.e. `9` is equal to `9`), the `if` statement's conditional evaluates as `true`.

**Top-tip:** *Remember that the comparative operator* `===` *("triple-equals") is used to check equality. This is distinct from the assignment operator* `=`*("single-equals"), which is used to set the value of a variable.*

###### Example 2

```javscript
if (6 + 3 < 5) {
  console.log("The hummingbird is the only animal that can fly backwards")
}
```
* The code above will not print anything because `6 + 3`, which is equivalent to `9`, is *not* less than `5`, making the `if` statement's conditional evaluate as `false`.

###### Example 3

```javascript
var dog = "satisfied"

if (dog === "hungry") {
  console.log("Refilling food bowl.")
} else {
  console.log("Reading newspaper.")
}
```

* This will print "Reading newspaper."

### `else if` Statements

Sometimes, we want to control the flow of our program based on more than one condition. For example, if I am hungry, then I will get a snack. If I am thirsty, then I will get a drink of water. Otherwise, I will stay here and continue learning more about control flow.

We can add additional layers of complexity to our `if` and `else` statements by using the `else if` keyword.

Let's add an `else if` statement to Example 3 from above:

```javascript
var dog = "thirsty"

if (dog === "hungry") {
  console.log("Refilling food bowl.")
} else if (dog === "thirsty") {
  console.log("Refilling water bowl.")
} else {
  console.log("Reading newspaper.")
}
```

* This will print "Refilling water bowl."

We can cascade as many `else if` statements as we wish, however `else if` statements can only be used following an `if` statement, and must precede the associated `else` statement (if used).

```javascript
var dog = "cuddly"

if (dog === "hungry") {
  console.log("Refilling food bowl.")

} else if (dog === "thirsty") {
  console.log("Refilling water bowl.")

} else if (dog === "playful") {
  console.log("Playing tug-of-war.")

} else if (dog === "cuddly") {
  console.log("Snuggling.")

} else {
  console.log("Reading newspaper.")
}

```

* This will print out "Snuggling."

<p class='util--hide'>View <a href='https://learn.co/lessons/js-if-else-files-readme'>Conditional Statements</a> on Learn.co and start learning to code for free.</p>
