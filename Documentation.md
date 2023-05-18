

# LittleBird Programming Language Documentation

## Content

-  [Introduction](#introduction) 
	- [About LittleBird](#about-littlebird) 
	- [Basic Syntax](#basic-syntax)
	- [Installing and Setting Up](#installing-and-setting-up)
- [Understanding Variables and Types](#understanding-variables-and-types)
	- [Declaring and Initializing Variables](#declaring-and-initializing-variables)
	- [Primitive Data Types](#primitive-data-types)
	- [Arrays](#arrays)
	- [Pointers](#pointers)
	- [Data Type Conversions](#data-type-conversions)
	- [Dynamic Types](#dynamic-types)
	- [Type Checking](#type-checking)
	- [Type Casting with Dynamic Types](#type-casting-with-dynamic-types)
	- [Conclusion](#conclusion)
- [Control Flow and Looping Constructs](#control-flow-and-looping-constructs)
	- [If-Else Statements](#if-else-statements)
	- [For Loops](#for-loops)
	- [While Loops](#while-loops)
		- [Basic While Loop](#basic-while-loop)
		- [While Until Loop](#while-until-loop)
		- [While To Loop](#while-to-loop)
	- [Control Flow in Loops](#control-flow-in-loops)
	- [Switch Statement](#switch-statement)
	- [Foreach Loop](#foreach-loop)
- [Functions](#functions)
	- [Declaring Functions](#declaring-functions)
	- [Calling Functions](#calling-functions)
	- [Returning Values from Functions](#returning-values-from-functions)
	- [Generic Functions](#generic-functions)
		- [Calling Generic Functions](#calling-generic-functions)
		- [Restrictions on Generic Functions](#restrictions-on-generic-functions)
	- [Function pointer and event](#function-pointer-and-event)
- [Error handling](#error-handling)
- [Asynchronous Programming](#asynchronous-programming)
	- [Promise Types](#promise-types)
	- [Automatic Async](#automatic-async)
	- [Return Syntax](#return-syntax)
- [Classes and Objects](#classes-and-objects)
	- [Declaring CLasses](#declaring-classes)
	- [Abstract and Sealed Classes](#abstract-and-sealed-classes)
	- [Nested Classes](#nested-classes)
	- [Interfaces and Structs](#interfaces-and-structs)
	- [Inheritance and Polymorphism](#inheritance-and-polymorphism)
	- [Method Overriding and Hiding](#method-overriding-and-hiding)
	- [Constructors and Destructors](#constructors-and-destructors)
	- [Access Modifiers](#access-modifiers)
	- [Usage of Access Modifiers](#usage-of-access-modifiers)
	- [Special Keywords in LittleBird](#special-keywords-in-littlebird)
	- [Constructor Usage in LittleBird](#constructor-usage-in-littlebird)
	- [Static and Constant Members](#static-and-constant-members)
	- [Generic Classes](#generic-classes)
	- [Kingdoms and Classes](#kingdoms-and-classes)
		- [Defining Methods and Variables](#defining-methods-and-variables)
		- [Creating a Class within a Kingdom](#creating-a-class-within-a-kingdom)
		- [Special Keywords](#special-keywords)
- [Namespaces](#namespaces)
	- [Declaring and Using Namespaces](#declaring-and-using-namespaces)
	- [Implementing Namespaces](#implementing-namespaces)
	- [Manipulating Namespaces](#manipulating-namespaces)
- [Overloading Operators](#overloading-operators)
- [Type Conversions](#type-conversions)
### [Go to Libraries](#default-libraries)


## Introduction

  

### About LittleBird

  

LittleBird, often abbreviated to LiBi, is a high-level, versatile programming language designed to offer programmers an intuitive and easy-to-read syntax without compromising on power and flexibility. LittleBird takes inspiration from several popular programming languages and combines their strengths to provide a coding experience that is both user-friendly and highly effective.

  

LittleBird's design philosophy emphasizes readability and simplicity, making it an ideal choice for programmers of all experience levels. It includes modern programming concepts such as namespaces, pointers, dynamic types, generics, and even operator overloading, providing advanced users with the tools they need to write efficient and robust code.

  

The language's unique syntax and keyword choices set it apart from other programming languages. For example, control flow and looping constructs are uniquely structured to improve code readability. The language also makes use of special symbols for various method declarations, and its access modifiers are determined by naming conventions. These features, while different from what you might find in other languages, are intended to make your code easier to write, read, and maintain.

LittleBird's two-stage compilation process is another feature that makes it unique. In the first stage, LittleBird code is compiled into C++ code. This process takes advantage of C++'s robust, well-tested, and highly optimized compilers, making it possible to write efficient and performant code in LittleBird. It also means that LittleBird can leverage libraries and frameworks written in C++, further extending its capabilities and use-cases.

In the second stage of the compilation process, the C++ code is then compiled into machine code, the low-level code that can be directly executed by the computer's hardware. This means that LittleBird programs can run directly on the hardware without the need for an interpreter or a virtual machine, resulting in more efficient execution.
    

LittleBird's unique combination of a user-friendly syntax, advanced programming concepts, and a powerful two-stage compilation process makes it a versatile and effective tool for programmers of all skill levels. Whether you're a beginner looking to learn the ropes or an experienced programmer seeking a more efficient way to write robust code, LittleBird offers a comprehensive solution.

### Basic Syntax

  

The basic syntax of LittleBird focuses on readability and clarity. Keywords are used to define the structure of the code, such as declaring variables, defining functions, implementing control flow, and more.

  

Here's a basic example of LittleBird code:

  

```littlebird
use: console, convert;
implement;

Write(Read() * 2);
```

  

In this code, we're using the "console" and "convert" namespaces, implementing all the namespaces, and then reading a value from the console, converting it to an integer, doubling it, and writing the result back to the console.

  

### Installing and Setting Up

  

Installing and setting up LittleBird on your machine is a straightforward process. (тут якусь ссиль на гайд хуйнуть, но я чесно пока хз як установку робити, подивлюсь по ситуації)

  

In the following sections, we will explore the various aspects of LittleBird in detail, from variables and data types to functions, classes, and beyond. We will also provide examples and best practices to help you get the most out of LittleBird.

  

Whether you're a beginner just starting out with programming or an experienced developer looking to learn a new language, we hope this documentation will serve as a valuable resource in your journey with LittleBird. Let's get started!

  

## Understanding Variables and Types

  

In programming, data is often manipulated through containers known as variables. These variables have specific types that define what kind of data they can hold and what operations can be performed on them. In this section, we'll explore how variables and types are used in LittleBird.

  

### Declaring and Initializing Variables

  

Variables in LittleBird are declared using their name followed by an optional type. You can declare a variable without specifying its type. If you do so, the type is inferred from the value you assign to the variable.

  

Here's how you declare a variable:

  

```littlebird
name:type;
```

  

And here's how you declare and initialize a variable:

  

```littlebird
name = expression;
```

  

In the first example, `name` is the name of the variable, and `type` is the type of the variable. In the second example, `expression` is the initial value assigned to the variable. The type of the variable is inferred from the type of the expression.

  

For instance, to declare an integer variable named `a`, you would write:

  

```littlebird
a:int;
```

  

To declare and initialize `a` with the value `1`, you would write:

  

```littlebird
a = 1;
```

  

### Primitive Data Types

  

LittleBird supports several standard types:

  

-  `int`: An integer number. Example: `1`

-  `short`: A shorter integer number. Example: `1s` 

-  `long`: A longer integer number. Example: `1l`

-  `char`: A single character. Example: `49c` or `'1'`

-  `string`: A sequence of characters. Example: `"hello"`

-  `float`: A floating-point number. Example: `1f`

-  `double`: A double-precision floating-point number. Example: `1.`

-  `decimal`: A decimal number. Example: `1d`

  

You can declare and initialize variables of these types as follows:

  

```littlebird
i = 1;         // int

s = 1s;        // short

l = 1l;        // long

c = '1';       // char

str = "hello"; // string

f = 1f;        // float

d = 1.;        // double

dec = 1d;      // decimal
```

  

### Arrays

  

An array is a data structure that can store a fixed-size sequence of elements of the same type. You can declare an array with a specified size or with no size. If no size is specified, the array size will be determined by the number of values you assign to it.

  

Here's how you declare an array:

  

```littlebird
name:[type; size];
```

  

And here's how you declare an array without a specified size:

  

```littlebird
name:[type];
```

  

For instance, to declare an array of integers named `a` with a size of `5`, you would write:

  

```littlebird
a:[int; 5];
```

  

To declare an array of integers named `a` without specifying its size, you would write:

  

```littlebird
a:[int];
```

  

You can also declare and initialize an array as follows:

  

```littlebird
a = [1,2,3,4,5];
```

  

In this case, `a` is an array of integers with a size of `5`.

  

### Pointers

  

In LittleBird, we declare a pointer using `<type>`. This means the variable will hold the memory address of a data item rather than holding a data item itself.

  

As we mentioned before, to declare a pointer to an integer named `a`, you would write:

  

```littlebird
a:<int>;
```

  

Here, `a` doesn't contain an integer value but rather the memory address where an integer value is stored.

  

#### Initializing and Using Pointers

  

To assign a memory address to a pointer, we use the `><` operator, which retrieves the memory address of a variable.

  

For example, if we have an integer variable `b` and we want to store its address in our pointer `a`, we can do this:

  

```littlebird
b = 10;

a = >b<; //a:<int>
```

  

Now, `a` holds the memory address of `b`.

  

To get the value stored in the memory location that `a` is pointing to, we use the `<>` operator, also known as the dereference operator.

  

```littlebird
value = <a>; //value:int
```

  

Here, `value` will be assigned the value that `a` points to, which is the value of `b`, i.e., `10`.

  

### Data Type Conversions

  

Sometimes, you need to convert a value from one type to another. This is known as type casting. To cast a value to a different type, you use the type cast operator `::`. The syntax is as follows:

  

```littlebird
newValue = value::newType;
```

  

For example, if you have an integer `a` and you want to convert it to a float, you can do the following:

  

```littlebird
a = 10; //int

b = a::float; //float
```

  

Here, `b` will be a float with a value of `10.0`.

  
### Dynamic Types

In addition to the static types mentioned before, LittleBird also supports dynamic types. A dynamic type variable can hold a value of any data type and its type can be changed during the runtime of the program. 

Dynamic types in LittleBird offer a lot of flexibility by allowing variables to hold any type of value and change type during the execution of a program. However, with this flexibility comes the responsibility to manage types carefully to avoid errors and this negatively affects the performance of the code. By understanding how to use dynamic types and the associated features like type checking and type casting, you can make the most of this powerful feature.

Here's how you declare a dynamic type variable:

```littlebird
a:dynamic;
```

In this example, `a` is a variable that can hold any type of data. 

You can assign a value to a dynamic type variable just like you would with any other variable:

```littlebird
a = 1;     // a is now an int
a = "hi";  // a is now a string
a = 1.0f;  // a is now a float
```

As you can see, the type of `a` changes based on the type of value you assign to it. This provides a lot of flexibility, but it also means you need to be careful. If you try to use a dynamic type variable in a way that's not compatible with its current type, you might get unexpected results or even an error.

### Type Checking 

Since dynamic types can change during runtime, it might be necessary to check the type of a variable before performing operations on it. LittleBird provides a `is` operator for this purpose. Here's how you can use it:

```littlebird
a = 1;
Write(a is int); // Outputs true

a = "hello";
Write(a is int); // Outputs false
```


### Type Casting with Dynamic Types

As with static types, you can use type casting to convert a dynamic type variable to a different type. However, because dynamic types can hold any type of value, you need to be sure that the type you're casting to is compatible with the current value of the variable. If it's not, you'll get an error.

Here's an example:

```littlebird
a = 1;          // a is an int
b = a::float;   // b is a float with a value of 1.0

a = "hello";
c = a::int;     // Error: cannot cast string to int
```

In the first part of this example, `a` is an integer, so it can be cast to a float without any problems. In the second part, `a` is a string, which cannot be cast to an integer, so trying to do so results in an error.



### Conclusion

  

Variables and types are fundamental concepts in any programming language, including LittleBird. By understanding how to declare, initialize, and use different types of variables, you can manipulate data and build complex programs.

  

## Control Flow and Looping Constructs

  

In any programming language, control flow and looping constructs are critical for creating logic and performing repetitive tasks. In LittleBird, this is achieved through various constructs such as `if-else` statements, `for` loops, `while` loops, and special keywords like `->;` and `<-;` for skipping loop iterations or breaking out of loops.

  

### If-Else Statements

  

`If-else` statements in LittleBird are used for conditional branching in the code. The general syntax for an `if-else` statement is as follows:

  

```littlebird
if <condition>:

// code to execute if condition is true (only one statement)

else

// code to execute if condition is false (only one statement)

```

 or
```littlebird
if <condition>{}
else{}

// code to execute if condition is false
```

In the `if` part, you replace `<condition>` with your condition to test. If the condition is true, the code following the `if` statement (up to the `else` statement) gets executed. If the condition is not true (i.e., it's false), the code following the `else` statement gets executed.

  

Here's an example:

  

```littlebird
if i < 10:
	console.Write(i);
else
	console.Write("i is not less than 10");

```

  

In this example, the program checks if the variable `i` is less than 10. If it is, it writes the value of `i` to the console. If `i` is not less than 10, it writes the string `"i is not less than 10"` to the console.

  

### For Loops

  

`For` loops in LittleBird are used for repeating a block of code a certain number of times. They're especially useful when you know in advance how many times the code should run.

  

Here's the general syntax for a `for` loop in LittleBird:

  

```littlebird
i from <start> [to|until] <end> [step <step_size>] [do <action>]
```

  

The `from` keyword indicates the starting point of the loop. The `to` and `until` keywords specify the end condition of the loop. The `step` keyword allows you to specify a step size different from the default of 1. The `do` keyword is used to specify an action to be performed on each iteration of the loop.

  

Here are a few examples:

  

```littlebird
i from 0 to 10 //equivalent to for(int i = 0; i<=10; i++)

i from 0 until 10 step 2 //equivalent to for(int i = 0; i<10; i+=2)

i from 0 to 10 do i.Do() //equivalent to for(int i = 0; i<=10; i.Do())

i from 0 until i < 5 do i.Do() //equivalent to for(int i = 0; i < 5; i.Do())

i from 0 to i > 5 do i.Do() //equivalent to for(int i = 0; !(i > 5); i.Do()) or for(int i = 0; i <= 5; i.Do())
```

  

In the first example, the loop starts at 0 and ends when `i` is equal to 10, incrementing `i` by 1 on each iteration. In the second example, the loop starts at 0 and ends when `i` is less than 10, incrementing `i` by 2 on each iteration. The third example does the same as the first but also calls the `Do()` function on `i` at each iteration.  The fourth example continues to be executed until the condition becomes false. The fifth example is executed up to the point where the condition turns true.

  

### While Loops

  

While loops are a fundamental control structure used to repeat a block of code as long as a certain condition is true. In LittleBird, there are three variations of the while loop: `while until`, `while to`, and `while`.

  

#### Basic While Loop

  

The simplest form of a while loop continues as long as a specified condition is true.

  

Here's the syntax:

  

```littlebird
while <condition>:
	// code to execute (only one statement)

```
or
```littlebird

while <condition>
{
	// code to execute
}
```

  

And here's an example:

  

```littlebird
i = 0;

while i < 10
{
	console.Write(i);
	i++;
}
```

  

In this example, the loop will continue to run as long as `i` is less than 10. Each time the loop runs, it will print the current value of `i` and then increment `i` by 1.

  

#### While Until Loop

  

The `while until` loop is a variation of the while loop that continues as long as the condition after `until` is true.

  

Here's the syntax:

  

```littlebird
while until <condition>:
	// code to execute
```

  

And here's an example:

  

```littlebird
i = 0;

while until i == 10
{
	console.Write(i);
	i = i + 1;
}
```

  

In this example, the loop will continue to run until `i` equals 10. The code within the loop will print the current value of `i` and then increment `i` by 1.

  

#### While To Loop

  

The `while to` loop is another variation of the while loop. It continues to run until the condition after `to` becomes true. This is similar to a `do-while` loop in other languages, where the loop is guaranteed to run at least once, regardless of the condition.

  

Here's the syntax:

  

```littlebird
while to <condition>:
	// code to execute
```

  

And here's an example:

  

```littlebird
i = 0;

while to i > 10:
	console.Write(++i);
```

  

In this example, the loop will continue to run until `i` is greater than 10. The code within the loop will print the current value of `i` and then increment `i` by 1.

  

### Control Flow in Loops

  

In addition to these variations of the while loop, LittleBird also provides two keywords to control the flow of execution within loops: `->;` and `<-;`.

  

-  `->;` is used to skip one iteration in a loop. This is equivalent to the `continue` statement in other languages.

-  `<-;` is used to break out of a loop. This is equivalent to the `break` statement in other languages.

Here's an example that uses both of these keywords:

  

```littlebird
i = 0;
while i < 10
{
	i++;
	if i == 5: ->;
	console.Write(i);
	if i == 8: <-;
}
```

  

In this example, when `i` equals 5, the `->;` keyword will cause the loop to skip to the next iteration, so "5" will not be printed. When `i` equals 8, the `<-;` keyword will cause the loop to terminate, so "9" and "10" will not be printed. The output of this code will be "1 2 3 4 6 7 8".

### Switch Statement

In LittleBird, a `from` block is used as a switch statement. It checks the variable `i` against a series of values (`value1`, `value2`, etc.), and executes the corresponding block of code if it finds a match. For example:

```littlebird
from i 
{ 
	value1{}, 
	value2{} 
} 
```

is analogue of 

```csharp
switch(i) 
{ 
	case value1:
	break; 
	case value2:
	break; 
}
```

### Foreach Loop

In LittleBird, a `from` loop can also be used as a foreach loop. `i from j` loops over each item in `j`, and the corresponding block of code modifies the item. For exaple:

```littlebird
i from j:
	i++; 
```

is analogue of 

```csharp
foreach (var i in j)
	i++;
```


## Functions

Functions in LittleBird are essential components of structured and object-oriented programming. They provide a way to encapsulate reusable pieces of code that can perform a specific task. This chapter will cover how to declare, call, and use functions in LittleBird.

### Declaring Functions

In LittleBird, functions are declared using their name followed by a list of parameters and their types enclosed in parentheses. The function body is enclosed in braces `{}`:

```littlebird
name (param1:type, param2:type){}
```

For example, here's a function named `Add` that takes two integers as parameters and adds them together:

```littlebird
Add (a:int, b:int) => a + b;
```

The `=>` symbol is used to indicate the return of a value from the function. In this case, the function returns the sum of `a` and `b`.

The function parameters are declared in the same way as variables, with their names followed by their type. Multiple parameters are separated by commas.

### Calling Functions

Functions are called using their name followed by a list of arguments enclosed in parentheses:

```littlebird
name(params);
```

Here's how you can call the `Add` function defined earlier:

```littlebird
sum = Add(5, 3);
```

This will call the `Add` function with the arguments `5` and `3`, and assign the result to the variable `sum`.

When calling a function, it's important to provide the correct number of arguments that match the function's parameter list, both in type and in order.

You can also call functions from a specific namespace or class by qualifying the function name with the namespace or class name:

```littlebird
namespace.name(params);
namespace.class.name(params);
```

### Returning Values from Functions

In LittleBird, functions use the `=>` symbol to return a value:

```littlebird
name (params) => expression;
```

The `expression` after the `=>` symbol is the value that the function will return. This can be a simple value, a variable, or a more complex expression.

Here's an example of a function that returns the product of two integers:

```littlebird
Multiply (a:int, b:int) => a * b;
```

And here's how you can call this function and use its return value:

```littlebird
product = Multiply(4, 2);
```

This will call the `Multiply` function with the arguments `4` and `2`, and assign the result to the variable `product`.

### Generic Functions

Generic functions in LittleBird, as in many other programming languages, are functions that can operate on variables of different types. These functions are called "generic" because they can be used with many different types of arguments. Generics make it possible to create a function template that can work with any type, as specified by the caller.

Here's how to declare a generic function in LittleBird:

```littlebird
Func<T>(){}
```

In this example, `Func` is the name of the function, and `T` is a placeholder for a type that will be provided when the function is called. The angle brackets `<>` are used to enclose the type placeholder(s).

A generic function can have multiple type parameters:

```littlebird
Func<T1, T2>(){}
```

In this example, the function `Func` can accept arguments of two different types, `T1` and `T2`.

You can use these type parameters as if they were actual types:

```littlebird
Func<T>(param1:T, param2:T){}
```

In this example, the function `Func` accepts two parameters, both of the same type `T`.

### Calling Generic Functions

To call a generic function, you need to provide the type(s) to replace the placeholder(s) in the function definition. This is done by placing the actual type(s) in angle brackets `<>` after the function name:

```littlebird
Func<int>(1, 2);
```

In this example, the function `Func` is called with `int` as the actual type for `T`, and the arguments `1` and `2` are passed to the function.

#### Restrictions on Generic Functions

While generic functions are powerful and flexible, there are some restrictions on how they can be used:

1. You cannot use operators like `+`, `-`, `*`, etc., directly on variables of the generic type, because these operators might not be defined for all possible types that could replace `T`. You will need to define these operations separately for each type that `T` might represent.

2. You cannot create an instance of `T` using the `new` keyword inside a generic function, because not all types have a parameterless constructor. 

3. You cannot use `T` as the type of an array or a list directly within a generic function, because not all types can be used to create arrays or lists.

4. You cannot use the `typeof` operator with `T` within a generic function, because `T` is not a specific type but a placeholder.

Despite these restrictions, generic functions can significantly improve the flexibility and reusability of your code, allowing you to write more efficient and maintainable programs.

### Function pointer and event

The LittleBird programming language introduces a special way to use function pointers as variables, utilizing two distinct types: `Func` and `Action`. 

`Func` is a type that represents a function with a return type and any number of parameters. The first parameter in the `Func` type declaration represents the output or return type, and the rest represent the input parameters of the function. For instance, `i:Func<int, int>;` declares a function variable `i` that takes an integer as a parameter and returns an integer.

`Action`, on the other hand, represents a method that has no return type (void) and takes any number of parameters. All parameters in the `Action` declaration are input parameters. For example, `j:Action<int>;` declares an action variable `j` that takes an integer as a parameter and doesn't return a value.

These variables can be used like regular functions. For example, `a = i(5);` calls the function pointed by `i` with `5` as the argument, and `j(6);` calls the action pointed by `j` with `6` as the argument.

Furthermore, LittleBird introduces an `event` type. An `event` can hold multiple function pointers (that should have a void return type), and when the event is triggered, all the associated functions are called. You can add functions to an event with the `=>` operator, and trigger the event by calling it like a function. For instance:

```littlebird
e:event<int>; // declare an event e that takes an integer as a parameter
e=>j; // add the action j to the event e
e=>printNum(i:int) Write(i); // add another action to the event e
e(5); // trigger the event e with 5 as the parameter
```

In this example, when `e(5);` is called, both `j(5);` and `printNum(5);` are called, in the order they were added to the event.

Certainly! Here's how the chapter on async might look like in the LittleBird Interactive (LiBi) programming language documentation:

## Error handling

In LittleBird, error handling is done using the symbols `!=>` and `=>`. The `!=>` block is equivalent to the `try` block in traditional languages, where you place the code that might throw an error. The `=>` block is equivalent to the `catch` block, where you handle the error. The second `=>` block is equivalent to the `finally` block, where you put code that should run regardless of whether an error occurred.

To throw an error, you can use `!=> :Exception;`, which is analogous to `throw new Exception();` in other languages.

Example:
```littlebird
{ }!=> { }=> { }
{ }(x:Exception)!=> { }=> { }
```

is analogue of 

```csharp
try {} catch {} finally {}
try {} catch (Exception x) {} finally {}
```
and
```littlebird
!=>:Exception;
```

is analogue of 

```csharp
throw new Exception();
```
## Asynchronous Programming

LittleBird Interactive (LiBi) supports asynchronous programming through the use of `promise` types and automatic async functionality. This allows you to write code that can perform tasks in the background, making your applications more efficient and responsive.

#### Promise Types

In LiBi, a function that performs an asynchronous operation returns a `promise` of a certain type. This is declared using the syntax `promise<type>`. For instance, a function that asynchronously retrieves an integer would be declared as `promise<int>`. 

A `promise` has a `.state` property, which can have one of the following values:

- `0`: The asynchronous operation is not yet completed.
- `1`: The asynchronous operation has completed successfully.
- `2`: The asynchronous operation has failed.

#### Automatic Async

In LiBi, any function that returns a `promise` is automatically considered to be asynchronous. This means that you don't have to explicitly use an `async` keyword to declare such functions, unlike in some other programming languages. This makes writing asynchronous code more straightforward and less error-prone.

#### Return Syntax

LiBi uses the `=>` operator to return a result from a function. This concise syntax makes your code easier to read and write. 

Here's an example of how you can write an asynchronous function in LiBi:

```littlebird
myFunction()
{
    result = someOtherAsyncFunction();
    => result;
}
```

In this example, `myFunction()` is automatically asynchronous because it returns the result of `someOtherAsyncFunction()`, which is a `promise`. The state of this `promise` can be checked using the `.state` property.

## Classes and Objects

In LittleBird, classes are the primary building blocks for creating objects. They define the structure, behavior, and attributes that objects of a particular type will have. Classes are essentially blueprints that allow you to create instances of objects.

### Declaring Classes

To declare a class in LittleBird, use the `class` keyword followed by the class name:

```littlebird
class ClassName:
```

### Abstract and Sealed Classes

Abstract classes are classes that cannot be instantiated, and are intended to be inherited by other classes. They can contain abstract methods, which have no implementation in the abstract class. Declare an abstract class using the `abstract` keyword:

```littlebird
abstract ClassName:
```

Sealed classes are classes that cannot be inherited by other classes. They can be instantiated, but their functionality and structure are fixed. Declare a sealed class using the `sealed` keyword:

```littlebird
sealed ClassName:
```

### Nested Classes

Classes can be nested within other classes. The nested class is declared as an `offspring` of the parent class:

```littlebird
ClassName1 offspring ClassName2:
```

### Interfaces and Structs

Interfaces define a contract that classes can implement. They specify a set of methods that implementing classes must provide. Declare an interface using the `contract` keyword:

```littlebird
contract IName:
```

To implement this contract, use keyword `signed` after class:

```littlebird
contract IName:
//code
class ClassName signed IName:
//code
```

Structs are lightweight classes that can be used to store data. They are defined using the `data` keyword:

```littlebird
data StructName:
```

### Inheritance and Polymorphism

Inheritance is the mechanism by which a class can inherit properties and methods from a base class. The derived class can also override or extend the functionality of the base class. Inheritance is defined by using the `class` keyword between the subclass and the superclass names:

```littlebird
SuperclassName class SubclassName:
```

This syntax can also be used with `abstract` and `sealed` classes:

```littlebird
SuperclassName abstract SubclassName:
```

### Method Overriding and Hiding

LittleBird supports method overriding using the following special symbols:

- `@MethodName` is used for abstract methods.
- `#MethodName` is used for virtual methods.
- `*MethodName` is used to override methods.
- `:MethodName` is used for new methods (hiding the base method).

### Constructors and Destructors

Constructors are special methods that are called when an object is created. They are used to initialize the object's state. Destructors are special methods that are called when an object is destroyed. In LittleBird, constructors are denoted with a `:` symbol, and destructors are denoted with a `~` symbol.


### Access Modifiers

In the LittleBird programming language, access modifiers are determined based on naming conventions. The access level of a member variable is determined by the prefix of its name:

- `Name` signifies a public member.
- `_name` signifies a private member.
- `_Name` signifies a protected member.
- `name` signifies an internal member.
- `__name` signifies a private protected member.
- `__Name` signifies an internal protected member.

### Usage of Access Modifiers

When defining member variables within a class, you must follow these naming conventions. For example:

```littlebird
class Book:
__name:string; //private protected member
```

When using private protected and internal protected member variables, you should write two underscores when defining and one underscore when using them. For example:

```littlebird
class Book:
__name:string; //private protected

:(name:string)
	_name = name; //usage of private protected member
```

So, situation like this is restricted:

```littlebird
class Book:
_name:string; //private
__name:string; //private protected

:(name:string)
	_name = name; //error
```


### Special Keywords in LittleBird

In LittleBird, there are two special keywords used to represent the current instance of a class (akin to `this` in other languages) and to call to the superclass (like `super` or `base` in others). These are represented by `_` and `-` respectively.

```littlebird
class Book:
_name:string; //private member

class Novel:
_rate:float; //private member

:(name:string, rate:float)
{
	-._name = name; //calling to superclass (Book) and setting private member
	_._rate = rate; //setting private member of current instance (Novel)
}
```

### Constructor Usage in LittleBird

These keywords can also be used to call constructors of the superclass or the current class.

```littlebird
class Book:
_name:string; //private member

:(name:string)
	_name = name; //setting private member

class Novel:
_rate:float; //private member

:(name:string, rate:float)
{
	-(name); //calling superclass (Book) constructor
	_._rate = rate; //setting private member
}
:(name:string) _(name, 5.0); //calling current class (Novel) constructor
```

In this example, `-(name);` calls the constructor of the superclass `Book`, and `_(name, 5.0);` calls another constructor of the current class `Novel`.

### Static and Constant Members

Static members are shared across all instances of a class and are denoted by prefixing the member name with a `|` character: `|MemberName`. Constant members are read-only and cannot be modified after they are assigned. They are denoted by prefixing the member name with an `=` character: `=MemberName`.

### Generic Classes

LittleBird allows the creation of generic classes that can work with any data type. You can create a generic class by using the `<T>` notation after the class name:

```littlebird
class Gen<T>:
```

In this code, `T` is a placeholder for any data type. You can use `T` just like any other data type within the class definition.

You can create an instance of a generic class by replacing `T` with a specific data type. For instance, if you wanted to create an instance of `Gen` that works with integers, you would do the following:

```littlebird
a:Gen<int>;  // Declare a variable of type Gen<int>.
```

In this code, `a` is an instance of `Gen` that works with `int` values.

Definitely! Here's a chapter on kingdoms, classes, and special keywords for the LittleBird Interactive (LiBi) documentation:

---

### Kingdoms and Classes

In LittleBird Interactive (LiBi), a `kingdom` represents a broad category or module of functionality. The classes within a kingdom provide specific implementations of the functionality that the kingdom represents.

#### Defining Methods and Variables

In a kingdom, all methods and variables must be defined, unless they are abstract or virtual methods, or if the variable has been initialized.

#### Creating a Class within a Kingdom

You can create a class within a kingdom using the following syntax:

```littlebird
[abstract|sealed] <kingdomName> <className>:
```

This creates a class `<className>` within the kingdom `<kingdomName>`. The class can be declared as `abstract` or `sealed` depending on the desired behavior.

#### Special Keywords

Kingdoms in LiBi provide several special keywords to provide flexible functionality:

- `collect`: This keyword allows you to get a pointer to an array of all classes within the kingdom.
- `attach`: This keyword allows you to bind a function to another function within the kingdom, so that when the kingdom's function is called, the attached function is also called.
- `call`: This keyword allows you to call every instance of a specific function within the kingdom.
- `avoid`: This keyword allows you to exclude a particular function, variable, constructor, or destructor from being necessary in the class within the kingdom.

Here's an example of how you can use these concepts:

```littlebird
kingdom script:
Start();
Update();

script Player:
Start() _init();
avoid Update();
```

In this example, a kingdom named `script` is defined with two methods, `Start()` and `Update()`. A class `Player` is created within the `script` kingdom, which implements the `Start()` method and avoids the `Update()` method.

```littlebird
call script.Start(); // Calls the Start method for all classes in the script kingdom

attach UpdateBotAI() to script.Update(); // When the Update method is called, it will also call UpdateBotAI
```

Here, the `Start()` method is called for all classes within the `script` kingdom. Additionally, the `UpdateBotAI()` function is attached to the `Update()` method of the `script` kingdom, so that `UpdateBotAI()` is also called whenever `script.Update()` is invoked.


## Namespaces

Namespaces in LittleBird, commonly referred to as LiBi, are a way of grouping related code together. They help to prevent naming conflicts by providing a way to disambiguate identifiers that may be the same but belong to different namespaces.

### Declaring and Using Namespaces

In LiBi, namespaces are included using the `use` keyword followed by the namespace names, separated by commas:

```littlebird
use:name1,name2;
```

The above example includes two namespaces: `name1` and `name2`. By including these namespaces, you can now use the classes, methods, and other identifiers defined within these namespaces.

To use a specific identifier from a namespace, you can qualify the identifier with the namespace name, using a period (`.`) to separate the namespace name from the identifier:

```littlebird
namespace.name;
namespace.class.name;
```

### Implementing Namespaces

In LiBi, you can specify which namespace you want to use in your code with the `implement` keyword. When you implement a namespace, you can use the identifiers from that namespace without having to qualify them with the namespace name:

```littlebird
use: console, convert;
implement: console;

Write(convert.ToInt(Read()) * 2);
```

In this example, we are using the `console` and `convert` namespaces, and implementing only the `console` namespace. This allows us to use the `Write` and `Read` functions from the `console` namespace without having to qualify them with the namespace name.

If you want to implement all the namespaces you're using, you can use just the `implement` keyword without any namespace name:

```littlebird
use: console, convert;
implement;

Write(ToInt(Read()) * 2);
```

In this example, we are implementing all the namespaces that we are using: `console` and `convert`. This allows us to use the identifiers from both namespaces without having to qualify them with the namespace names.

### Manipulating Namespaces

Namespaces in LiBi can be treated like variables. You can assign namespaces to variables and manipulate them as you would with any other variable:

```littlebird
i = get(<namespace>); // Assigns the value of <namespace> to variable i.
i = :namespace; // Assigns a new empty namespace to i.
```

LiBi provides several ways to add elements to namespaces:

```littlebird
i => Func(string,int); // Adds a function with parameters of type string and int to namespace i.
i => a; // Adds variable a to namespace i. If a is a namespace, a becomes a nested namespace of i.
i => :Class; // Adds a new class to namespace i.
```

You can also modify the elements of a namespace:

```littlebird
i.Func()=Func2(); // Changes function Func to function Func2 in namespace i.
i.a = 42; // Changes the value of variable a to 42 within namespace i.
```

The elements within a namespace can be retrieved as an array of strings:

```littlebird
i:[Functions|Classes|Namespaces|Variables] // Returns an array of all corresponding elements.
```

LiBi allows you to add comments to the elements of a namespace:

```littlebird
i.name.comment = "This is a comment."; // Adds a comment to the element 'name' in namespace i.
```

This covers the basics of namespaces in LiBi. Remember that namespaces are a powerful tool for organizing your code and preventing naming conflicts. They are particularly useful in large codebases where the same identifier might be used in different contexts. But of course, this negatively affects the performance of the code.

## Overloading Operators

LittleBird allows the overloading of operators for custom classes, which means you can redefine the behavior of standard operators for instances of your classes. 

To overload an operator, use the `operator` keyword, followed by the operator you want to overload, and then the `binary` or `left` keyword (depending on the operator), and finally the parameters:

```littlebird
operator + binary (a:Class1, b:Class2){} // Overloads the + operator for instances of Class1 and Class2.

operator ++ left (a:Class1, b:Class2){} // Overloads the ++ operator for instances of Class1 and Class2.
```

In the first example, the `+` operator is overloaded for instances of `Class1` and `Class2`. In the second example, the `++` operator is overloaded for instances of `Class1` and `Class2`.

## Type Conversions

LittleBird allows you to define type conversions for your custom classes, which means you can specify how to convert objects of your class to objects of another class. 

To define a type conversion, use the class name followed by the `to` keyword, and then the code block for the conversion. Please note that type conversions must return a value and cannot be void:

```littlebird
Class1 to { /*Some code that return Class2*/ } // Defines a conversion from Class1 to Class2.
```

In this code, a conversion is defined from `Class1` to `Class2`. The code block should contain the logic for converting an instance of `Class1` to an instance of `Class2`.

This concludes our discussion on classes and objects in LittleBird. With this knowledge, you should have a good understanding of how to define classes, create objects, and manipulate them using methods, properties, and operators. As always, practice is key to mastering these concepts, so try to write as much code as you can. Happy coding!

# Default libraries
## Short description

- [**console**](#console): Functions for control of console
    
-  [**system**](#system): Low-level system functions, such as accessing environment variables, handling signals, or interacting with the operating system.
    
-  [**system.file**](#system.file): Functions for file I/O, such as reading and writing files, and manipulating file paths.

- [**math**](#math): Basic mathematical functions and constants, such as trigonometric functions, logarithms, exponentiation, square roots, and mathematical constants like pi and e.
    
- [**science**](#science): Scientific computing functions, such as linear algebra operations, statistical functions, and possibly numerical calculus functions.
    
- [**http**](#http): Functions for making HTTP requests, such as GET, POST, DELETE, etc.
    
-  [**web**](#web): A broader web development library, possibly including functions for generating HTML, handling websockets, or server-side programming.

-  [**structures**](#structures): Common data structures, such as lists, stacks, queues, trees, and hash maps.
    
-  [**json**](#json): Functions for parsing and generating JSON data.
    
- [**thread**](#thread): Functions for multithreading and concurrency, such as creating and joining threads, and synchronizing access to shared resources.
    
-  [**gui**](#gui): Functions for creating graphical user interfaces, such as windows, buttons, text inputs, and handling user interaction.
    
-  [**test**](#test): Functions for writing and running tests, such as unit tests, integration tests, or property-based tests.
    
- [**android**](#android): Functions for interacting with Android-specific features, such as accessing the device's sensors, creating notifications, or interacting with the Android lifecycle.
- ### LogicBox libraries (game engine, currently develope)
##  console
    
-   `Write(text:string)`: Prints the provided string to the console.
-   `WriteLine(text:string)`: Prints the provided string to the console, followed by a newline character.
-   `Read():string`: Reads a line of text from the console.
-   `Read(text:string):string`: Prints the provided string to the console and after it reads a line of text from the console.
-   `Clear()`: Clears the console screen.
-   `SetColor(color:Color)`: Sets the color of the text that will be printed to the console.
## system
    
-   `GetEnv(varName:string):string`: Returns the value of the environment variable with the given name.
-   `SetEnv(varName:string, value:string)`: Sets the value of the environment variable with the given name.
-   `Exit(code:int)`: Exits the program with the given exit code.
-   `Execute(command:string):string`: Executes the given command in the system shell and returns the output.
-   `Sleep(duration:int)`: Pauses execution of the current thread for the given duration (in milliseconds).
## system.file
    
-   `ReadFile(path:string):string`: Reads the contents of the file at the given path.
-   `WriteFile(path:string, content:string)`: Writes the given content to the file at the given path.
-   `AppendToFile(path:string, content:string)`: Appends the given content to the file at the given path.
-   `DeleteFile(path:string)`: Deletes the file at the given path.
-   `FileExists(path:string):bool`: Returns `true` if a file exists at the given path, `false` otherwise.
-   `CreateDirectory(path:string)`: Creates a new directory at the given path.
-   `DeleteDirectory(path:string)`: Deletes the directory at the given path.
-   `DirectoryExists(path:string):bool`: Returns `true` if a directory exists at the given path, `false` otherwise.
-   `GetFiles(directory:string):array<string>`: Returns an array of the names of all files in the given directory.
-   `GetDirectories(directory:string):array<string>`: Returns an array of the names of all subdirectories in the given directory.

Certainly! Here are potential functions for these libraries in LittleBird:

## math

- `Power(x:double, y:double):double`: Returns x raised to the power y.
- `Sqrt(x:double):double`: Returns the square root of x.
- `Abs(x:double):double`: Returns the absolute value of x.
- `Sin(x:double):double`: Returns the sine of x.
- `Cos(x:double):double`: Returns the cosine of x.
- `Tan(x:double):double`: Returns the tangent of x.
- `Asin(x:double):double`: Returns the arcsine of x.
- `Acos(x:double):double`: Returns the arccosine of x.
- `Atan(x:double):double`: Returns the arctangent of x.
- `Log(x:double):double`: Returns the natural logarithm of x.
- `Exp(x:double):double`: Returns e raised to the power x.
- `Pi:double`: A constant representing the ratio of the circumference of a circle to its diameter.
- `E:double`: A constant representing the base of natural logarithms.

## science

- `DotProduct(v1:array<double>, v2:array<double>):double`: Returns the dot product of two vectors.
- `CrossProduct(v1:array<double>, v2:array<double>):array<double>`: Returns the cross product of two vectors.
- `MatrixMultiply(m1:array<array<double>>, m2:array<array<double>>):array<array<double>>`: Multiplies two matrices.
- `MatrixInverse(m:array<array<double>>):array<array<double>>`: Returns the inverse of a matrix.
- `Mean(v:array<double>):double`: Returns the mean of a set of values.
- `Median(v:array<double>):double`: Returns the median of a set of values.
- `Mode(v:array<double>):double`: Returns the mode of a set of values.
- `StandardDeviation(v:array<double>):double`: Returns the standard deviation of a set of values.
- `Derivative(f:Func<double, double>, x:double):double`: Approximates the derivative of a function at a specific point.
- `Integral(f:Func<double, double>, a:double, b:double):double`: Approximates the integral of a function over a specific interval.
## http
    
-   `Get(url:string):promise<string>`: Makes a GET request to the given URL and returns the response.
-   `Post(url:string, data:string):promise<string>`: Makes a POST request to the given URL with the given data and returns the response.
   -   `Put(url:string, data:string):promise<string>`: Makes a PUT request to the given URL with the given data and returns the response.
   -   `Delete(url:string):promise<string>`: Makes a DELETE request to the given URL and returns the response.
   -   `Request(url:string, method:string, headers:dict<string,string>, data:string):promise<string>`: Makes a custom HTTP request.
## web
    
-   `CreateElement(tag:string, attributes:dict<string,string>, children:array<Element>):Element`: Creates a new HTML element.
   -   `Render(element:Element):string`: Renders an HTML element as a string.
   -   `OpenWebSocket(url:string):WebSocket`: Opens a websocket to the given URL.
   -   `StartServer(port:int, requestHandler:Func<Request, Response>)`: Starts a web server on the given port.
## structures
    
   -   `List<T>:class`: A generic list class with methods like `Add(item:T)`, `Remove(item:T)`, `Insert(index:int, item:T)`, and `Get(index:int):T`.
    -   `Stack<T>:class`: A generic stack class with methods like `Push(item:T)`, `Pop():T`, and `Peek():T`.
    -   `Queue<T>:class`: A generic queue class with methods like `Enqueue(item:T)`, `Dequeue():T`, and `Peek():T`.
    -   `Tree<T>:class`: A generic tree class with methods like `AddChild(parent:T, child:T)`, `Remove(child:T)`, and `GetChildren(parent:T):List<T>`.
    -   `Dictionary<K,V>:class`: A generic hash map class with methods like `Add(key:K, value:V)`, `Get(key:K):V`, `Remove(key:K)`, and `ContainsKey(key:K):bool`.
##   json
    
   -   `Parse(jsonString:string):dynamic`: Parses a JSON string into a dynamic object.
    -   `Stringify(object:dynamic):string`: Converts an object into a JSON string.
    -   `LoadFromFile(path:string):promise<dynamic>`: Asynchronously reads a JSON file from the given path and parses it into a dynamic object.
    -   `SaveToFile(path:string, object:dynamic):promise<void>`: Asynchronously writes an object to a file as JSON at the given path.
    -   `Prettify(jsonString:string):string`: Converts a JSON string into a "pretty" formatted string.
    -   `Minify(jsonString:string):string`: Converts a JSON string into a "minified" string (no unnecessary whitespace).
    -   `IsValid(jsonString:string):bool`: Checks if a string is valid JSON.
## api
    
   -   `CreateClient(baseURL:string):APIClient`: Creates a new API client with the given base URL.
    -   `api:kingdom`: A kingdom representing an API client. It might have attributes like:
       -   `[Get(endpoint:string)]`: Makes a GET request to the given endpoint and parses the response as JSON.
        -   `[Post(endpoint:string, data:dynamic)]`: Makes a POST request to the given endpoint with the given JSON data and parses the response.
        -   `[Put(endpoint:string, data:dynamic)]`: Makes a PUT request to the given endpoint with the given JSON data and parses the response.
        -   `[Delete(endpoint:string)]`: Makes a DELETE request to the given endpoint.
       And virtual methods:
        -   `SetHeader(name:string, value:string)`: Sets a default header for all requests made by the client.
        -   `RemoveHeader(name:string)`: Removes a default header from the client.
        -   `SetAuthToken(token:string)`: Sets an authorization token for all requests made by the client.

## gui
 
 -   `Window`: A class representing a window.
    
    -   `constructor(title:string, width:int, height:int)`: Creates a new window with the given title and dimensions.
    -   `Show()`: Shows the window.
    -   `Close()`: Closes the window.
    -   `SetTitle(title:string)`: Sets the title of the window.
    -   `SetSize(width:int, height:int)`: Sets the size of the window.
    -   `AddElement(element:GUIElement)`: Adds a GUI element to the window.
    -   `RemoveElement(element:GUIElement)`: Removes a GUI element from the window.
    -   `OnClose(callback:Action)`: Sets a function to be called when the window is closed.
-   `Button`: A class representing a button.
    
    -   `constructor(label:string)`: Creates a new button with the given label.
    -   `SetText(label:string)`: Sets the text of the button.
    -   `OnClick(callback:Action)`: Sets a function to be called when the button is clicked.
-   `TextInput`: A class representing a text input field.
    
    -   `constructor()`: Creates a new text input field.
    -   `GetText():string`: Returns the current text of the input field.
    -   `SetText(text:string)`: Sets the text of the input field.
    -   `OnTextChanged(callback:Action<string>)`: Sets a function to be called when the text of the input field changes.
-   `Label`: A class representing a label.
    
    -   `constructor(text:string)`: Creates a new label with the given text.
    -   `GetText():string`: Returns the current text of the label.
    -   `SetText(text:string)`: Sets the text of the label.
-   `GUIElement`: An abstract base class for all GUI elements.
    
-   `Layout`: A class to control the layout of GUI elements.
    
    -   `Horizontal()`: Makes the layout horizontal.
    -   `Vertical()`: Makes the layout vertical.
-   `App`: An application class.
    
    -   `Run()`: Starts the GUI event loop.
   
## android
   
   -   `Activity`: A class representing an Android activity.
    
    -   `constructor()`: Creates a new activity.
    -   `OnCreate(callback:Action)`: Sets a function to be called when the activity is created.
    -   `OnStart(callback:Action)`: Sets a function to be called when the activity is started.
    -   `OnResume(callback:Action)`: Sets a function to be called when the activity is resumed.
    -   `OnPause(callback:Action)`: Sets a function to be called when the activity is paused.
    -   `OnStop(callback:Action)`: Sets a function to be called when the activity is stopped.
    -   `OnDestroy(callback:Action)`: Sets a function to be called when the activity is destroyed.
    -   `StartActivity(activity:Activity)`: Starts another activity.
-   `Sensor`: A class representing a sensor on the device.
    
    -   `constructor(sensorType:int)`: Creates a new sensor object for the specified sensor type.
    -   `GetValue():float`: Returns the current value of the sensor.
    -   `Start()`: Starts collecting data from the sensor.
    -   `Stop()`: Stops collecting data from the sensor.
-   `Notification`: A class representing a notification.
    
    -   `constructor(title:string, text:string)`: Creates a new notification with the specified title and text.
    -   `Show()`: Displays the notification.
    -   `Cancel()`: Cancels the notification.
-   `Preferences`: A class for storing and retrieving user preferences.
    
    -   `constructor(name:string)`: Creates a new preference file with the specified name.
    -   `GetInt(key:string, defaultValue:int):int`: Retrieves an integer preference.
    -   `SetInt(key:string, value:int)`: Stores an integer preference.
    -   `GetString(key:string, defaultValue:string):string`: Retrieves a string preference.
    -   `SetString(key:string, value:string)`: Stores a string preference.
-   `BroadcastReceiver`: A class representing a broadcast receiver.
    
    -   `constructor()`: Creates a new broadcast receiver.
    -   `OnReceive(callback:Action<string, Bundle>)`: Sets a function to be called when the broadcast receiver receives an intent.
## thread
      
In LittleBird, you can create a special type known as `thread`. This type allows you to execute functions concurrently, in a separate thread of execution. This is useful for performing tasks that can run independently of each other, which can improve the efficiency and responsiveness of your program.

Here's a simplified breakdown of the concept:

1.  You can declare a variable of type `thread`. For example: `i:thread;`
2.  You can add functions to a thread, similar to how you add them to an event. However, before adding functions, you need to call the `ZeroSet` method with the function's parameters. This method clears any previously set functions and prepares the thread for a new set of actions. For instance, `i.ZeroSet<int>();` clears the thread `i` and sets it up for functions that take an integer as a parameter.
3.  You can then add functions to the thread using the `=>` operator. For example, `i=>j(int);` and `i=>k(int);` add the functions `j` and `k` to the thread `i`. Both `j` and `k` should be functions that take an integer as a parameter.
4.  To start the execution of the thread, you simply call the thread like a function. For example, `j();` starts the thread `j`, which will concurrently execute all the functions added to it.
5.  If you want to wait for the thread to finish before continuing with the rest of your program, you can use the `Wait` method. For example, `j.Wait();` will pause the execution of your program until the thread `j` has finished executing all its functions.
6.  If you want to retrieve data from a function executed in a thread, you need to pass a pointer as an argument to the function, and then return the pointer. This is because the function is executed in a separate thread, and any data it produces is not automatically available in the main thread.
   -   `Mutex`:class: A class representing a mutual exclusion (mutex) lock, with methods like:
        -   `Lock()`: Locks the mutex. If the mutex is already locked, waits until it is unlocked.
        -   `Unlock()`: Unlocks the mutex.
        -   `TryLock():bool`: Tries to lock the mutex. Returns true if successful, false if the mutex is already locked.
       
## test
    
   -   `AssertEquals(actual:dynamic, expected:dynamic)`: Asserts that two values are equal. If not, throws an assertion error.
    -   `AssertTrue(condition:bool)`: Asserts that a condition is true. If not, throws an assertion error.
    -   `RunTests(func:Action<void>)`: Runs a suite of tests defined in the given function.
