# Intro to Programming With Python

## Getting Started

### Pep Talk

### Setup

```python
print("Hello World!")
```

## Expressions

With that boring setup out of the way, we can finally write some code!

This section is about expressions. You should be pretty familiar with mathematical expressions like "5 + 5". The key point about expressions is they evaluate to something. For example, `5 + 5` evaluates to `10`. Not exactly rocket science. 

Wikipedia, the source of all knowledge and wisdom, defines expressions more formally:

> An expression in a programming language is a syntactic entity that may be evaluated to determine its value.

So what the heck does that mean? 

In this section you will learn about:
 - Python's various data types and what they are used for
 - The various types of expressions
 - How expressions can be combined indefinitely
 - How to call Python's built in functions

### Data types and Literals

Your computer can store all kinds of data, from text documents to cat pictures. And you should know that computers represent that data with ones and zeros. Well technically they store data with electrical signals that are either high or low. Somebody said: 

> A computer is a rock we taught how to think.

For our purposes though, a computer stores all its data as ones and zeros, which represent true and false. Each one of these numbers is called a bit and every other type of data is made out of these bits. Python has four basic data types.

- Boolean (bool)
- integers (int)
- floating point numbers (float)
- strings (str)

We will explore each in turn and show how to write them and print them out in Python. When we explicitly write out a value (as opposed to get it from a variable or a file, more on them later) we call that a literal. So `5` is the literal value for five.

#### Boolean Values

Bools are the only type I capitalized up there and that's because they are actually named after a dude, George Bool. He discovered what we call Boolean Algebra. Basically a Boolean value is either true or false. If we run the code

```python
print(True)
```

Then sure enough the output is
```python
True
```

Mindblowing. You can imagine what happens if we use `False` instead. Note that Python is case-sensitive. If you try this code

```python
print(true)
```

It should throw an error because Python does not know what `true` is. It does know what `True` with a capital T is. As we go on to name things like variables and functions we'll have to be mindful of our capitalization.

#### Integers

If you've taken some math classes you'll have heard of integers but a refresher might be in order. Integers are whole numbers like `0`, `100`, `-27`, and so on. They can't be fractions or have a decimal place. They can be negative though.

```python
print(0)
print(100)
print(-27)
```

#### Floats

Missing decimal places? Well here you go. Floating point numbers can store just about any real number albeit with limited precision.

```python
print(0.5)
print(3.14159)
print(-52.1)
```

What's the floating point? Well it refers to the decimal point and how it can "float" from position to position, changing the number by ten each time. For example
```python
print(31.4159)
print(3.14159)
print(31415.9)
```
All of these numbers are different multiples of pi. They are only differentiated by where the decimal point is.

#### Strings

Strings are ordered collections of characters. When we printed out "Hello World!" in the setup section? That text between the quotes is a string. Here are some examples

```python
print("Hello World!")
print("I am the very model of a modern Major General.")
print("This is my cat's favorite data type.")
```

We use quotation marks to tell Python the characters between the quotes are a string literal. It's easy to forget them so keep an eye out!

#### Exercises

Use the print function to print out the following information in the appropriate data type. If you don't want to use your info use the president or Lady Gaga or some.

Your name.

Your age.

Your gpa.

Your address.

### Comments

Comments are a way of writing little notes to yourself in the code. 

```python
print(40 + 2) # This is a very important number!
```

Everything after the `#` is ignored by Python. The above is a trivial example but learning how to write good comments is a very important skill. When you're writing out more complicated programs it can often be a good idea to spell out how that program should work with comments before you write any of the code.

There is a school of thought that suggests you should not use comments, that the code you write should be so well formatted and your choice of variable and function names should be so descriptive that no comments are necessary. Ignore these people. Certainly variables and functions should be named descriptive things but comments are incredibly important for helping others understand your code. They will even help you when you go back to your code after six months and have forgotten how everything works.

### Errors

### Operators

Technically literals like `5` and `"Hello World!"` are expressions but they aren't very interesting ones. An operator accepts one or more data and returns a single value. For example

```python
print(5 + 5)
```

Will print out `10`. The `+` sign is the addition operator. It accepts two values (whatever is to the left and right of it) and returns their sum. Think of operators as black boxes. They take one or more inputs, do some magic with them, and return a new value. Let's look at some examples.

### Boolean Operators

For the following examples you should know two facts: as I write this:

* It is overcast, and 
* I have a cat. 

Both of those facts are true.

Because I have a cat, we can represent it with `True`. Because it is overcast, that is `True` as well.

So if I say the sentence "I do not have a cat" is that sentence true or false? How would we represent that in Python?

```python
print(not True)
```

This code prints out `False`. The `not` keyword flips whatever comes after it to true if it is false and false if it is true. You can probably guess what this prints out:

```python
print(not False)
```

If I say the sentence "I have a cat and it is overcast" is that sentence true or false?

It seems true to me. Let's see how we would phrase that in Python:

```python
print(True and True)
```

When we print out that expression, it prints `True`! Try it. That keyword `and` is the operator.

Ok, next sentence: "I have a cat and it is sunny out." Well, part of that sentence is true and part of it is false. So if we have to evaluate whether the whole sentence is true or not what do we decide?

```python
print(True and False)
```

This expression evaluates to `False`. Why? Because `and` only evaluates to `True` if both expressions next to it are true. 

We have one more Boolean operator to look at: `or`.

Let's change our example to what will be the first of many of my patented ***Terrible Car Analogies***. Let's say I have a red car. If I say "My car is red or it is black." Is that a true statement or not? And of course, how would we represent that in Python? Behold:

```python
print(True or False)
```

This prints `True`! And that makes sense right? Well what if I said "My car is silver or it is black."? Let's try it:

```python
print(False or False)
```

That prints `False`. My car is neither silver nor black. The operator we are using is `or` and if one of `or`'s inputs is true it evaluates to true. But if both of them are false? It evaluates to false.

So we've introduced three Boolean operators: `not`, `and`, and `or`. How is `not` different? Notice it only accepts one Boolean value, the others accept two. We call operators like `not` "unary operators" and operators like `and` and `or` "binary operators". Don't be confused by the use of "binary" there! That just means the operator accepts two values, it's not about the data type of those values.

#### Exercises
Write down what you expect the following to print out. Then check your answers!

```python
print(False or True)
print(not True and True)
print(False and True or False)
```

### Arithmetic Operators

So that `and` and `or` stuff might have been unfamiliar, we're on surer ground now. When we introduced operators we used the following example:

```python
print(5 + 5) # prints 10
```

There are a few more arithmetic operators you need to know.

```python
print(5 - 5)  # prints 0
print(5 * 5)  # prints 25
print(5 ** 3) # prints 125
```

What do you think that last one does? If you guessed "exponentiation" you're right! If you're wondering `^` was already reserved for something else.

I'm sorry to report I fibbed earlier, `-5` is not a literal. You can see the minus sign is used for subtraction above but here it is the negation operator. It is a unary operator that flips negative numbers to positive and positive numbers to negative. It effectively multiplies the number by `-1`.

```python
print(-5)
```

Let's look at another example:

```python
print(5 / 5)  # prints 1.0
```

Wait, wait, hold up. `1.0`? Where did the `.0` come from? With the operators we have seen the data types of the inputs always match the type of the output. So our Boolean operators returned Boolean values. We have given all of these arithmetic operators integers as input and gotten integers as our output. So why are we getting a float out of this division?

Well, let's look at another example.

```python
print(5 / 2) # prints 2.5
```

Clearly `2.5` is not an integer. We could round it to an integer but we would lose some information. In Python 3 division always returns a floating point number. What if we wanted an integer though? We're going to talk about how to use functions in just a moment but let's get a sneak peek.

```python
print( int(2.5) )
```

The `int` function takes a value and returns an integer based on that value. What do you think the above prints? Try it out!

It prints `2`. You might expect it to print `3`, that's what `2.5` rounds to right? Well, just to drive this point home:

```python
print( int(2.999999) ) # still prints 2
```

The `int` function does not round, it truncates. Basically when you call `int` you are telling Python "Throw away everything after the decimal point." Now, integer division is sometimes what you want. For that, Python provides an "integer divide" operator.

```python
print(5 // 2) # yep, still prints 2
```

#### Type Coercion
Python will automatically convert integers into floats if it needs to. For example

```python
print(5 + 5.0)
```

This snippet prints `10.0`. We are adding an integer to a float. Python allows this, but automatically converts the integer into a float before the addition. Adding a float to a float returns a float so that's why our answer has a trailing `.0`.

This is pretty much the only instance of type coercion in Python. Letting this get out of hand *cough JavaScript cough* can cause all kinds of annoying and hard to track down bugs. For example adding a string to an integer will always result in a runtime error. 

#### The Modulo Operator

For this operator I ask you to travel back in time... many moons ago... to about fourth grade. This was longer ago for some of you than others. Remember when your math teacher was first introducing you to division. They would ask something like "How many times does 5 go into 14?" and "What is the remainder?". The answers are of course `2` and `4` respectively. Consider the following

```python
print(14 // 5) # prints 2
print(14 % 5)  # prints 4
```

That percent sign isn't a percent sign. I mean, it is, obviously. But it represents the modulo operator! This finds the remainder of a division. You would be forgiven for questioning the usefulness of such an operator but trust me, it's handy. Tuck it away for now, it'll be useful later.

#### Exercises

Write down what you expect the following to print out. You can use a calculator, that's not cheating. Then check your answers!

```python
print(10 + 15)
print(30 - 40)
print(66 / 12)
print(66 // 12)
print(10 ** 2)
print(100 ** 0.5) # this one is a little tricky
print(47 % 3)
print(2 % 5)      # this one is also a little tricky
```

#### Bonus

What will the following print out?

```python
print(234578263457 % 2)
```

You don't need to use a calculator. In fact, you can tell at a glance. What is the answer? And why is it easy to figure out? Why is it easier than `234578263457 % 3`?

### String Operators

You didn't forget about strings did you? One of my favorite things about Python is how painlessly it handles strings. We're not quite ready for all of the string manipulation shenanigans Python allows but we can get a taste. 

You can concatenate strings with the `+` operator. Consider the following:

```python
print("Hello" + "World!")
```

This prints `"HelloWorld!"` which isn't exactly what we wanted. Still, we can see that the concatenation operator mashed those strings together. How do we fix it?

```python
print("Hello" + " " + "World!") # prints "Hello World!"
```

We can also multiply a string by an integer.

```python
print("Repetitive" * 5) # prints RepetitiveRepetitiveRepetitiveRepetitiveRepetitive
```

Don't try to multiply a string by a string, or a float. What would that even do?

We can convert almost anything in Python to a string with the `str` function. For example

```python
print("One plus two plus three equals " + str(1+2+3)) # prints "One plus two plus three equals 6"
```

### Comparison Operators

A lot of the time we want to compare things. Is your age at least 21? Is your name equal to `"John Doe"`? To answer these kind of questions we use conditional operators. If I ask you "Is your age at least 21?" how do you answer? Well I can guess the answer is either "yes" or "no", true or false. Consider the following:

```python
print(5 == 5)
```

This expression is asking the question "Does 5 equal 5?" and you can probably guess the output is `True`. So far almost every operator has returned the same type that it was given. With `5 + 5` the addition operator accepts two integers and returns an integer. `True and True` accepts two Boolean values and returns a Boolean as well. The comparison operators are different. In the above snippet we give the equality operator (`==`) two integers and get out a Boolean. You might wonder why the equality operator uses two equals signs rather than one. In the next section we'll see why.

Let's look at some more examples.

```python
print(4 < 5)  # Less than, prints True
print(4 > 5)  # Greater than, printsFalse
print(4 <= 5) # Less than or equal to, prints True
print(4 <= 4) # Also less than or equal to, prints True
print(4 != 5) # Not equal, prints True
```

### Order of operations

What does `5 + 2 * 3` equal? Well naively you might say 27 because `5 + 2` is `7` and `7 * 3 = 21`. But you know that's not right. In elementary school we learn about the order of operations: PEMDAS or Parentheses, Exponentiation, Multiplication, Division, Addition, Subtraction. Python uses order of operations too.

```python
print(5 + 2 * 3) # Prints 11
```

We have learned about a whole bunch of new operators though, what order are they evaluated in?

Well it starts pretty much the same. You can make sure that part of an expression goes first by wrapping it in parentheses. For example `(5 + 2) * 3` evaluates to `21` because `5 + 2` is wrapped in parentheses so it is calculated first. Then the expression becomes `7 * 3`.

The comparison operators come after the math operators so `5 + 6 < 8` first evaluates `5 + 6` and then checks if `11 < 8`. Imagine if this worked the other way, `6 < 8` evaluates to `True` so then Python would have to evaluate `5 + True` which doesn't make a lot of sense and would throw an error.

Checking for equality happens after the other comparisons. 

### Using Functions and Modules

Through this section we have been making liberal use of the `print` function. What is a function? Well I like to think of it as a tool. You have some operation that needs to be done in many different places so you use a function. Typically these accept one or more inputs and return one or more outputs. Our `print` function is followed by parentheses and whatever is within those parentheses is printed to the console. `print` does not return anything however.

In the section on arithmetic operators we used another function `int`. 

```python
print( int(2.5) ) # Prints 2
```

The `int` function accepts some value and *tries* to convert it into an integer. This process can fail so for example the following will throw an error:

```python
print( int("five") ) # This code results in an error "invalid literal for int() with base 10: 'five'"
```

Never mind about that for right now. The point is that the `int` function accepts some value as input and returns an integer as output.

Sometimes you might need a function that isn't built into Python like `print` and `int` are. For this you can import functions from modules. Python comes with a "standard library" of helpful modules, Anaconda has a ton built in, and you can always install more with a package manager like `pip` or `conda`. More on that later.

`random` is one of those modules that are part of the standard library. It shouldn't surprise you to learn that it provides a bunch of functions related to random (technically pseudorandom) numbers. Consider the following:

```python
import random
print( random.random() ) # prints out a number x where 0 <= x < 1
```

The first thing to note in this snippet is the `import` command. That tells Python we would like to use an installed module. `random` is the name of that module. Then on the next line we use the function `random.random()`. This might look a little odd but the first random refers to the random module, the `.` means we want to use a function inside of that module, and the second `random` refers to the a function called `random` in the `random` module. Let's look at another example.

```python
import random
print( random.randint(1, 6) ) # prints out a number x where 1 <= x <= 6
```

This is the first function we have looked at that accepts multiple arguments. Again we are using the `random` module but this time we are calling the `randint` function from that module. You might have guessed `randint` is short for "random integer". You'll see that instead of passing zero or one arguments to the function we are passing two, the integer values `1` and `6` separated by a comma. The first number is the minimum random value and the second one is the maximum value. So the snippet will print out a number between `1` and `6` inclusive. Why did I pick those numbers? Because it's like a die, a regular six sided die. 

This has been a short introduction to modules. We'll make more use of them later on and eventually write our own!

#### Exercises

### Dice Simulator

## Statements

We have looked at expressions in some detail but so far we have been using Python as a fancy calculator. Now we can talk about statements. Unlike expressions, statements do not return a value. They are designed to change the state of the program. 

What is state? Well kind of what it sounds like. Imagine playing a video game like Super Mario. At any time there is a bunch of information the game is keeping track of like Mario's x and y position, what powerups he has, what frame of animation he is using, and so on. This goes for the enemies and hazards on the level too. All that information at a particular time is the game's state. Similarly we will store and manipulate information with our program. Every time we change a bit of data we are changing the program's state and the mechanisms we use to do that are statements.

### Assignment

The first kind of statement we will look at is assignment. 

```python
a = 10
print(a) # prints 10
```

Here we are creating a variable called `a` and assigning it a value of `10`. Then we print the contents of the variable `a`. Crazy bananas. 

That operator `=` is the assignment operator. Do not confuse it with the equality operator `==`. The equality operator is asking a question "is this equal to that?" The assignment operator is a command "Set this equal to that." Note that reading from a variable is an expression but setting a variable is a statement. It changes the state of the program from that point on.

Check out the following snippet:

```python
a = 10
b = 5
c = a + b # a + b evaluates to 15 so set c to 15
print(c) # prints 15
```

It should be pretty clear that the code prints a `15` to the console. Consider the statement `c = a + b`. On the left of the equals sign is the variable we are assigning and on the right is an expression. That expression is evaluated and the result is assigned to the variable `c`. Why am I making such a big deal about this? Well...

```python
a = 10
b = 5
c = a + b
b = 10
print(c) # what does this print?
```

You might reasonably say the answer is `20`. Or if you have a particularly mathematical mindset you might think this would be an error, the code suggests `b` should be equal to both `5` and `10`. But the assignment operator is not describing a mathematical relationship between `a`, `b`, and `c` nor for that matter between `b` and `5`. We set `c` to the *result* of `a + b`. After assignment `c` does not know or care about `a` or `b`, it simply holds the value 15. 

I like to think of variables like buckets. One of the buckets has an `b` painted on the side, that's the name of the bucket. That bucket also has some contents in this case initially the integer value `5`. When we reference the contents of `b` in `a + b` we are taking a peek inside the bucket and passively observing its state. When we set `b` equal to `10` later on we are actively dumping out the bucket's old value and replacing it with a new one. Take a look at the following:

```python
a = 0
a = a + 1
print(a) # what does this print?
```

Mathematically `a = a + 1` is nonsense. In Python however we are simply setting `a` to its old value plus `1`. So the snippet prints out `1`. What about the next one?

```python
a = 0
a = a + 1
a = a + 1
a = a + 1
a = a + 1
print(a) # what does this print?
```

What does the above print? Well, `a` starts with a value of `0` and then `1` is added to it four times, so the answer is `4`! In fact performing an operation on a variable and then putting the result in the same variable is so common we have a whole class of operators for it. The above code and the code below are equivalent.

```python
a = 0
a += 1
a += 1
a += 1
a += 1
print(a) # what does this print?
```

The `+=` operator adds some value to the variable and sets the value to the result of that expression. This syntax is a little confusing for newcomers so I'll weave it in gradually as we go.

### If, Elif, and Else

We are still in fancy calculator land. What we really want is to be able to make decisions based on some data. We want conditional execution. Thus:

```python
age = 16

if age < 18:
    print("You are not old enough.")
```

What will the above code print out? `"You are not old enough."` of course! Take a look at the syntax. We start with the keyword `if`, then an expression that evaluates to a Boolean (hereon referred to as a conditional), and then `:` (a colon). The line after the `if` statement must be indented. The indentation in Python is very important. Other programming languages indicate that code "belongs" to an `if` statement with curly braces but Python uses indentation. Most IDEs will automatically indent the line after an `if` statement as required but you'll have to unindent at the end of a block.

What if we set the `age` variable to `18`, what will it print out then?

Diddly squat! The indented code will only execute if the expression `age < 18` evaluates to `True`. To check the other case we'll need to write a little more code.

```python
age = 18

if age < 18:
    print("You are not old enough.")
else:
    print("You are old enough!")
```

Now, let's make our club a little harder to get into.

```python
age = 18

if age < 18:
    print("You are not old enough.")
elif age < 21:
    print("You are almost old enough.")
else:
    print("You are old enough!")
```

The above code will print out `"You are almost old enough."`. The screwy `elif` keyword is short for "else if". Let's talk through what happens when the code is run.

* First `age` is set to some value, in this case `18`.
* Then the expression `age < 18` is evaluated. If it is `True` the code in the indented block is run. In this case it is `False` so we go to the next check.
* If the last conditional was `False` evaluate `age < 21`. If that expression is `True` execute the indented block of code. In our case it is `True` so Python prints `"You are almost old enough."` to the console and exits the block.
* Finally if both the above conditions were `False` run the code in the indented block after the `else`. In our case the last conditional evaluated to `True` so this does not happen.

As always, I encourage you to take the code, modify it, and play with it. But what about this silly `elif` keyword? What if we remove it so the code becomes

```python
age = 16

if age < 18:
    print("You are not old enough.")
if age < 21:
    print("You are almost old enough.")
else:
    print("You are old enough!")
```

So if we set `age` to something over twenty like `30` the code prints out `"You are old enough!"`

If we keep `age` at `18` the code prints out `"You are almost old enough."`

So far so good. But what happens if we set `age` to something like `16`? It will print out

```python
"You are not old enough."
"You are almost old enough."
```

It prints two lines! What happened? Well let's mentally step through the code.

* First `age` is set to `16`.
* Then we evaluate the expression `age < 18`. In this case the expression evaluates to `True` so we execute the indented block of code and print `"You are not old enough."`
* Then we move on to the next `if` statement and evaluate `age < 21`. This is also `True` and so we print `"You are almost old enough."`
* We do not get to the `else` statement because the last conditional evaluated to `True`.

So what's different? When you combine `if`, `elif`, and `else` statements they act as an unbroken chain of control flow statements. You can be guaranteed that one and exactly one of the indented blocks of code will be executed. You can chain together as many statements as you like this way. We could introduce more `elif` statements and have, for example, unique messages for any age we like.

### While, Break, and Continue

So we just learned about control flow. An `if` statement can decide to run code or not. What will the following print?

```python
count = 3
i = 0

if i < count:
    print(i)
    i = i + 1
```

Take your time, read the code slowly, step through it keeping in mind what is stored in the variables when. Got your answer?

You might have said it prints `1` and that is almost right. It actually prints `0`. Notice that in our `if` statement `i` is printed *before* it is incremented. After the code is run `i` is floating around with a value of `1` but we don't print it.

```python
count = 3
i = 0

if i < count:
    print(i)
    i = i + 1

if i < count:
    print(i)
    i = i + 1
```

I've added another `if` statement identical to the first one. What will this script print?

```python
0
1
```

The first `if` statement prints out `0` as before. The second one prints a `1` because `i` was modified by the first `if` statement.

```python
count = 3
i = 0

if i < count:
    print(i)
    i = i + 1

if i < count:
    print(i)
    i = i + 1

if i < count:
    print(i)
    i = i + 1

if i < count:
    print(i)
    i = i + 1
```

So what's that going to print out? You might expect it to print out `0` `1` `2` `3` but it actually stops at `2`. Again we can follow the code step by step and see `i` be incremented by `1` once, twice, thrice and then, at the fourth and final `if` statement we evaluate `i < 3` where `i` equals `3`. So really it evaluates `3 < 3` which is `False`. Three is not less than three! So the last block isn't executed. Now, wouldn't it be marvelous if we could "loop" over some code over and over again until some condition is met? Behold:

```python
count = 3
i = 0

while i < count:
    print(i)
    i = i + 1
```

This code sample and the last will print exactly the same thing. That's what `while` does, it checks a conditional, executes its block of code if that conditional evaluates to `True`, and repeats until the conditional becomes `False`. What if it never becomes false? Well then you have yourself an infinite loop and that's no good. 

#### Exercises

1: Write a loop that prints the even numbers up to `10`. And don't just use five print statements you goof.

Output:
```python
0
2
4
6
8
```

2: Write a loop that prints all of the numbers less than `10` that are evenly divisible by `3` or `5`. Remember the modulo operator!

Output:
```python
0
3
5
6
9
```

3: Sum up all the numbers 

### The Collatz Conjecture

Let's indulge in a little recreational math. I promise it's more fun than it sounds. Consider the following steps:

1. Start with a number `n`
2. If `n` is even divide it by `2`.
3. If `n` is odd multiply it by `3` and add `1`.
4. Repeat steps 2 and 3 until `[REDACTED]`. 

What is `[REDACTED]`? All shall be revealed. 

## Functions

What is a function? Well if you ask a mathematician they'll answer (in layman's terms) that it is a one to one relation between the elements of two sets. 
So for example `f(x) = y*2` is a function that maps real numbers to real numbers of twice the magnitude. Every value of `x` has one and exactly one corresponding value of `y`.

Functions in most programming languages are related but have a number of important differences which we will go over. For our purposes you can think of functions as tools. A function might do some tedious task that we would need to repeat many times. Instead of copy and pasting code everywhere we can create a function to make the task easier.
### Anatomy of a Function
Let's look at an example of a function.

```python
def add(x, y):
    return x + y
```
So we have some new keywords `def` and `return`. `def` means that we are defining a function, in this case a function called `add`. Just like variable names function names can be whatever we like but their name should indicate what they are for.
After the name we get parentheses and between them are two variables `x` and `y` separated by a comma. I say variables but these are technically parameters. I'll get into the distinction in a moment. After the parentheses we get a colon and an indented block of code just like an `if` statement. That brings us to the `return` keyword and the expression `x + y`.

Now if we run a script with only those two lines in it nothing will happen. We have defined our function but we have not used it. If functions are tools then we have made a hammer but we haven't swung it yet. Let's finish the snippet:
```python
def add(x, y):
    return x + y

a = add(10, 5)
print(a) # should print 15 or something is very wrong
```

Fabulous. I'm going to overexplain what happens when we execute these four lines of code. We can think about functions like black boxes. They accept one or more values and return a value. (This is a bit of a fib but it's accurate enough for now).
The values we supply to a function are called arguments. In this case our arguments are `10` and `5`. 

When you run a script Python reads through it line by line and executes whatever it is told to. The first lines it reaches define the function. After the definition we tell Python what we want the function to do in its body, in that indented block of code. After that we get to `a = add(10, 5)` where we are saying "pass `10` and `5` to the function `add` and store whatever the function returns to the variable `a`". 

This act of using a function is called "calling" a function. When we call a function you can think of Python as "jumping" to where that function is defined, arguments in tow. It stores those arguments in the variables `x` and `y`. Variables that contain arguments are called parameters.

When we get to the body of the function we find the line `return x + y`. First we evaluate the expression `x + y` which is `15` in our case. Then we use the `return` statement. When we return from a function we "jump" back to where we called it with the returned value. So in our case `add(10, 5)` evaluates to `15`. We set `a` to `15` and we print it out!

Woof that was a lot to say about some very simple code. Get yourself a glass of water or something.

### Arguments, Parameters, and the Power of Return

So I said I fibbed earlier. It turns out a function does not have to accept any arguments. Check out the following:

```python
def pi():
    return 3.14159
```

That is totally valid Python. Our `pi` function does not accept any arguments but it returns an approximate value for pi.

A function also doesn't have to return anything.

```python
def greet(name):
    print("Hello " + name + "!")

a = greet("Jill") # prints "Hello Jill!"
print(a) # prints 'None'
```

That `greet` function doesn't return anything! It is useful for something besides that, its "side effects" (more on these later). When we try to assign the result of `greet` to a variable that variable `a` is set to `None`. What is `None`? Well it's a null value that Python uses in situations like this where you ask for a value that doesn't exist. The side effect we want is to print to the console and we can do that simply by calling the function. We don't need to assign its return value to anything.

### Function Scope

Let's return to the idea of a function as a "black box". The body of a function lives in a "scope", a sort of one way barrier making the contents of a function unavalible to the rest of a program except via `return`. That sounds a little abstract let's look at an example.

```python
# WARNING! Code has an intentional error

def adder(x, y):
    total = x + y
    return total

a = adder(10, 5)
print(a) # prints 15
print(total) # error! 'total' is not defined
```

So what happened here? We tried to use the variable `total` but it was defined inside of the function's scope and so is not accessible outside that function.

```python
name = "Jill"

def greet():
    print("Hello " + name + "!")

greet() # prints "Hello Jill!"
```

I mentioned scope is a one way barrier. The variable `name` is floating out there in the top level of the script, what we call "global scope". The scope of `greet` is inside global scope so it can read from the `name` variable just fine. But! Reading is all it can do.

```python
name = "Jill"

def greet():
    # we only greet Bob around here
    name = "Bob"
    print("Hello " + name + "!")

greet() # prints "Hello Bob!"
print(name) # what will this print out?
```

In almost every language besides Python when we print `name` at the end of the function it would print out "Bob". Inside of the `greet` function we set the `name` variable to `"Bob"` and we can see that it does indeed print out "Hello Bob!". But Python likes to do things differently, the last line of this script prints out "Jill". 

Variables in the global scope are called "global variables" and they are usually discouraged. We'll talk about why soon. Python is happy to let you read values from global variables but if you want to assign to a global variable you need to tell Python explicitly. Otherwise as in our example above Python makes a local variable called `name` and assigns to it. The variable in the function body and the variable in the global scope are different even though they are both called `name`.

```python
name = "Jill"

def greet():
    # we only greet Bob around here
    global name
    name = "Bob"
    print("Hello " + name + "!")

greet() # prints "Hello Bob!"
print(name) # prints "Bob"
```

We've only added one line: `global name` at the top of the function. `global` is another one of those reserved keywords and it tells Python "no, for real, this variable is global" and now the script works as expected. 

There is another keyword `nonlocal` which works essentially the same way but lets you mutate the state of a variable that is not global but is in a function's outer scope. As always it's best to look at an example.

```python
def printSum(x, y):
    def sum():
        nonlocal x, y
        return x + y
    spam = sum()
    print(spam)

printSum(5, 10)
```

Our function `printSum` accepts two numbers. Inside of that function we define a function called `sum`. 

### Globals and Purity

### Bits and bobs
This section covers some more advanced aspects of functions. Most texts would save them for much later or elide them entirely but this is not most texts. I'm bringing up these topics now because they shouldn't intimidate you and your picture of functions in Python would be incomplete without them. So strap in!

#### Default arguments

#### Multiple return

#### Recursion

We have seen that functions can call other functions. But... what if I told you functions could call themselves? What would that even look like?

```python
def countDown(count):
    if count > 0:
        print(count)
        countDown(count - 1)

countDown(10) # prints the numbers 10 to 1
```

Look at that. We have looping behavior without a `while` in sight. Counting up is slightly more complicated because we need to know when to stop.

```python
def countUp(count, i = 0):
    if i < count:
        print(i)
        countUp(count, i + 1)

countUp(10) # prints the numbers 0  to 9
```

Compare that code to the `while` loop that does the same thing and you'll see basically the same bits in a different arraingement. Now both of these functions have an `if` statement inside of them and there is a good reason for that. Just like with `while` it is easy to get in infinite loops with recursion. Fortunately Python will actually throw an error if you recurse too many times.The condition that stops recursion is called 

```python
def factorial(x):
    if x > 1:
        return x * factorial(x-1)
    return 1
```

```python
def fibonacchi(n):
    if x > 1:
        return fibonacchi(n-1) + fibonacchi(n-2)
    return 1
```

#### First class functions

Python supports first class functions which basically means functions are values that you can store in variables and datastructures and you can even pass to and return from functions. 

```python
def doubler(x):
    return x * 2

def power(x):
    return 10 ** x

def transform(f, x):
    return f(x)

print( transform(doubler, 3) ) # prints 6
print( transform(power, 3) ) # prints 1000
```

Here we define a couple of functions `doubler` and `power` which return twice the input and ten to the input's power respectively. They both accept a number (either an `int` or `float`) as an argument and return a number. Finally we have the `transform` function. It accepts two arguments: a function and a number. It passes that number to whatever function was passed to it and returns the results.

First class functions are a very powerful feature, there is a reason they have crept into basically every major programming language. As we move on we'll see more use cases.

#### Lambdas

A lambda or an anonymous function is a scary mathy sounding name for function that doesn't have a name. 

```python
doubler = lambda x: x * 2
print( doubler(3) ) # yep still prints 6
```

We could rewrite our `doubler` function as the above. You can see that it has all the same bits as the original function but arrainged differently. `lambda x: x * 2` is an expression, it evaluates to a function. It starts with the reserved keyword `lambda` followed by our parameter `x`. Then a colon then the expression we were returning. You'll notice there is no `return` keyword. Lambdas can only have a single expression as their function body and they return what it evaluates to automatically. This means that a lambda cannot contain statements like `if`, `while` or even assignment. These are all very deliberate limitations. What I did above, assigning a variable to a lambda function is actually bad style. You should use `def` for named keywords. But consider our `transform` function again.

```python
def transform(f, x):
    return f(x)

a = transform(lambda x: x * 2, 5)
print(a) # prints 10
```

This is arguably a bit harder to read and is definitly a silly example. But at least now it is obvious when you call transform exactly what operation it will apply to the argument you pass it.

Finally you can pass multiple arguments to a lambda. I'm going to be bad again and assign a lambda straight to a variable. Forgive me Guido for I have sinned...

```python
product = lambda x, y: x * y

print( product(3, 10) ) # prints 30
```

The parameters of this function are just seperated by commas, no parenthises needed. 

Like I indicated lambda functions have taken the programming language world by storm. Understanding them will help you not just with Python but with languages that make much heavier use of them like JavaScript.

#### Factory functions

Last section we saw how to pass functions to functions. Now let's return some functions.

```python
def math(operator):
    if operator == "add":
        return lambda x, y: x + y
    elif operator == "sub":
        return lambda x, y: x - y
    elif operator == "mul":
        return lambda x, y: x * y
    elif operator == "div":
        return lambda x, y: x / y

spam = math("add")(5, 9)
print(spam) # prints 14
div = math("div")
eggs = div(5, 10)
print(eggs) # prints 0.5
```

Ok that's a longer snippet than usual. What's going on here?

Well we're using lambdas as you can see. We'll see a factory function that uses regular `def`s soon. We've got a block of `if` and `elif` statements and return a different function based on a string that is passed as an argument. So when we call `math("add")` that returns the function `lambda x, y: x + y`. 

`math("add")(5, 9)` becomes `(lambda x, y: x + y)(5, 9)`. We pass `5` and `9` as arguments to the function, the function adds them together and returns `14`.

#### Closures

Closures are a huge topic and are definitly something that we will come back to later on. Again my goal with this section is to introduce and demistify. So what is a closure? Well it's a way of binding mutable data to a function. What does that mean? Let's see:

```python
def makeCounter(name):
    count = 0
    def counter():
        nonlocal count
        count += 1
        print(name, " is: ",count)
    return counter

spam = makeCounter("Spam")
eggs = makeCounter("Eggs")
spam() # prints "Spam  is:  1"
spam() # prints "Spam  is:  2"
spam() # prints "Spam  is:  3"
spam() # prints "Spam  is:  4"
eggs() # prints "Eggs  is:  1"
```

What the heck is going on here? Well we have a function called `makeCounter` that accepts a name. The first thing `makeCounter` does it sets a variable called `count` to zero. Then it defines a function called `counter` which brings in that `count` variable via the `nonlocal` keyword, increments it, and prints it along with the counter's `name`. Then `makeCounter` returns that function.

We call `makeCounter` a couple of times, once with the name "Spam" and once with "Eggs". We store those functions in variables called, appropriately enough, `spam` and `eggs`. And when we call those functions they count up! How is that possible?

Our `makeCounter` function is a factory function, it makes and returns functions. Each one of those functions is unique and it carries the scope of `makeCounter` with it. Basically each function we make has its own copy of `count` to manipulate and print. 

As always it's ok if you find this confusing. Confusion is to your brain what the strain of working out is to your muscles. Closures are are powerful and really leverage a good understanding of scope which is why we are talking about them so early. 

## Data Structures
In this section we are learning about Python's built in data structures. So far the only things we have been able to store are the basic datatypes I described at the beginning. By the end of this section we'll be able to store anything.

### Lists and Tuples
```python
l = [3, 7, 9, 2, 4]
```
The above is a list. We are storing it in the variable `l`. You can think of a list as a row of cubby holes. The first hole contains a `3`, then a `7`, and so on. Each one of these cubby holes is a variable, we can look inside and change the contents of each. We get the contents of an entry in the list with brackets containing an index.

```python
l = [3, 7, 9, 2, 4]

print(l[3]) # 3 is the index. What does this print out?
```

What does `l[3]` evaluate to? `2`. But that's the fourth element! In Python, as in most languages, list indicies start at `0`. So `l[0]` evaluates to `3`. This can be tricky for new programmers to remember but soon enough it'll be second nature.

I mentioned that we could assign to entries in a list. Let's do that. 

```python
```

### Sets and Dictionaries

### Iterators, Generators, and Comprehensions

### Pass by Object

## Inputs and Outputs

### Handling User Input

### File IO

### Command Line Arguments

## Objects

### Why Object Oriented?

### Anatomy of an Object

### Dunder Methods

### Inheritance

## Modules

### If Name equals Main

### Importing your Modules

### PEP-8

### Using pip and conda

## Async