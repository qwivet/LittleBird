# LittleBird Documentation

## Table of Contents

1. [Introduction](#Introduction)
2. [Including Namespaces](#Including-Namespaces)
3. [Variable Declaration and Types](#Variable-Declaration-and-Types)
4. [Function Creation and Call](#Function-Creation-and-Call)
5. [Control Flow Statements](#Control-Flow-Statements)
6. [Pointers](#Pointers)
7. [Arrays](#Arrays)
8. [Object-Oriented Programming](#Object-Oriented-Programming)

## Introduction

LittleBird is a highly optimized yet straightforward programming language designed with game development and prototyping in mind. The language supports both procedural and object-oriented programming paradigms and leverages static typing for improved efficiency and error-checking. It also utilizes manual memory management, providing programmers with fine-grained control over resources.

## Including Namespaces

In LittleBird, namespaces are included using the `use` keyword followed by the namespace names, separated by commas:

```littlebird
use:name1,name2;
```

As for the implementation of namespaces, using the "implement" keyword is a good way to specify which namespace you want to use in your code. Here's an example of how you can use it:

```littlebird
use: console, convert;
implement: console;

Write(convert.ToInt(Read()) * 2);
```

In this code, we're using the "console" and "convert" namespaces, and implementing only the "console" namespace. This allows us to use the "Write" and "Read" functions from the "console" namespace without having to qualify them with the namespace name.

Alternatively, you can implement all the namespaces you're using with just the "implement" keyword:

```littlebird
use: console, convert;
implement;

Write(ToInt(Read()) * 2);
```

This code achieves the same result as the previous example, but it implements all the namespaces instead of just one.


## Variable Declaration and Types

Variables in LittleBird are declared using their name followed by an optional type:

```littlebird
name = expression;
name:type;
```

In variant with `name = expression;` this can be initialization of variable if this var didn't initialized before. So, variant
``` littlebird 
a=1;
```
is the same as
``` littlebird 
a:int;
a=1;
```
And the first option is more desirable

LittleBird supports the following standard types:

- `int` 1
- `short` 1s
- `long` 1l
- `char` 1c
- `string` "1"
- `float` 1f
- `double` 1.
- `decimal` 1d
- `arrays` [1]
- `pointers` \<a\>

## Function Creation and Call

Functions in LittleBird are defined using their name followed by a list of parameters and their types enclosed in parentheses. The function body is enclosed in braces `{}`:

```littlebird
name (param1:type, param2:type){}
```

Functions are called using their name followed by a list of arguments enclosed in parentheses:

```littlebird
name(params);
namespace.name(params);
namespace.class.name(params);
var.name(params);
```

In function we can use `=>` to return value from this function (in other languages often use `return`)

Control flow statements and functions that have a `{}` after their declaration can also be written without `{}` and with `:` after their declaration (don't write `:` after function initialization and else):

```littlebird
i from 0 to 10:
    console.Write(i);
```

## Control Flow Statements

### If-Else Statements

The `if` statement in LittleBird is used to test a condition:

- `if <condition>`: If the condition is true, the code within the braces is executed.
- `else`: The code within the braces is executed if the condition of the preceding `if` statement is false.

```littlebird
if i < 10:
    console.Write(i);
else
    console.Write("i is not less than 10");
```

### While Loops

LittleBird provides several variations of the `while` loop using the keywords `until` and `to`.

- `while until <condition>`: The loop continues as long as the condition is true.
- `while to <condition>`: The loop continues until the condition becomes true. This is similar to a `do-while` loop in other languages; it guarantees that the loop will run at least once.
- `while <condition>`: The loop continues as long as the condition is true. This is the standard while loop.

```littlebird
while until i < 10 // Loop continues as long as i is less than 10

while to i > 10 // Loop continues until i is greater than 10, but runs at least once

while i < 10 // Loop continues as long as i is less than 10
```

### From, To, and Until

LittleBird supports a flexible form of the `for` loop, allowing for a variety of loop declarations using a simple set of keywords: `from`, `to`, `until`, `step`, and `do`.

The general syntax for a `for` loop in LittleBird is as follows:

```littlebird
i from <start> [to|until] <end> [step <step_size>] [do <action>]
```
The `from` keyword indicates the starting point of the loop. The `to` and `until` keywords specify the end condition of the loop.

- `to` includes the end value in the loop, equivalent to `<=` in other languages.
- `until` excludes the end value from the loop, equivalent to `<`.

```littlebird
i from 0 to 10 //equivalent to for(int i = 0; i<=10; i++)

i from 0 until 10 //equivalent to for(int i = 0; i<10; i++)
```

The `to` and `until` keywords can also be used with a condition instead of a simple end value. This allows for more complex loop termination conditions.

- `to` will continue the loop as long as the condition after `to` is false, similar to a `while` loop.
- `until` will continue the loop as long as the condition after `until` is true.

Here are the corrected examples:

```littlebird
i from 0 to i > 10 do i.Do() //equivalent to for(int i = 0; !(i>10); i.Do())

i from 0 until i < 10 do i.Do() //equivalent to for(int i = 0; i<10; i.Do())
```

In the first example, the loop will continue as long as `i` is not greater than 10. In the second example, the loop will continue as long as `i` is less than 10. The `do` keyword is used to specify the action to be performed on each iteration of the loop.

Please note that these examples assume the default step size of 1. If a different step size is required, it can be specified using the `step` keyword as shown in the previous examples.

### Step

The `step` keyword allows you to specify a step size different from the default of 1.

```littlebird
i from 0 to 10 step 2 //equivalent to for(int i = 0; i<=10; i+=2)

i from 0 until 10 step 2 //equivalent to for(int i = 0; i<10; i+=2)
```

### Do

The `do` keyword is used to specify an action to be performed on each iteration of the loop.

```littlebird
i from 0 to 10 do i.Do() //equivalent to for(int i = 0; i<=10; i.Do())

i from 0 until 10 do i.Do()//equivalent to for(int i = 0; i<10; i.Do())
```

These keywords can be combined to create complex loop structures that are still easy to read and understand.

## Extra keyword

`->;` used to skip one repetition in a cycle (in other language often used `continue`)

`<-;` is used to exit the cycle (in other language often used `break`)


## Pointers

LittleBird supports pointers, providing direct access and manipulation of memory addresses.

- `a:<int>`: Declare a pointer `a` to an `int`.
- `b = <a>`: Assign the address of `a` to `b`.
- `>a<`: Dereference the pointer `a` to access the value stored at the memory address it points to.

```littlebird
a:<int>; // Declare a pointer to an int

b = <a>; // Assign the address of a to b

console.Write(>b<); // Print the value at the address pointed to by b
```

## Arrays

Arrays are used to store multiple values of the same type.

- `a:[int; 5]`: Declare an array `a` of `int` with a size of 5.
- `a:[int]`: Declare an array `a` of `int` with no specified size.
- `a = [1,4,8,8]`: Declare and initialize an array `a` with the specified values.

```littlebird
a:[int; 5]; // Declare an array of ints with size 5

a:[int]; // Declare an array of ints with no specified size

a = [1,4,8,8]; // Declare and initialize an array with specified values
```
## Object-Oriented Programming

### Class Definitions

In LittleBird, class definitions start with the keyword `class` followed by the class name:

```littlebird
class ClassName:
```

### Abstract Classes

Abstract classes are declared using the `abstract` keyword:

```littlebird
abstract ClassName:
```

### Sealed Classes

Sealed classes are declared using the `sealed` keyword:

```littlebird
sealed ClassName:
```

### Static Classes

Static classes are declared by prefixing the class name with a `|` character:

```littlebird
class |ClassName:
```

### Nested Classes

Classes can be nested within other classes. The nested class is declared as an `offspring` of the parent class:

```littlebird
ClassName1 offspring ClassName2:
```

### Interfaces

Interfaces are declared with the `contract` keyword:

```littlebird
contract IName:
```

### Structs

Structs are declared with the `data` keyword:

```littlebird
data StructName:
```

### Main Method

The entry point of a LittleBird program is declared with the `main:` keyword.

### Inheritance

Inheritance is defined by using the `class` keyword between the subclass and the superclass names:

```littlebird
SubclassName class SuperclassName:
```

This syntax can also be used with `abstract` and `sealed` classes.

### Implementing Interfaces

Classes implement interfaces using the `signed` keyword:

```littlebird
class ClassName signed IInterface1 IInterface2:
```

### Methods

Different types of methods are declared with special symbols in LittleBird:

- `:` is used for constructors.
- `~` is used for destructors.
- `@MethodName` is used for abstract methods.
- `#MethodName` is used for virtual methods.
- `*MethodName` is used to override methods.
- `:MethodName` is used for new methods.

For instance, a constructor for a class `ClassName` can be declared and called as follows:

```littlebird
: (params): //code // constructor declaration
:ClassName(params) // constructor call
```

### Access Modifiers

Access modifiers in LittleBird are determined based on naming conventions:

- `Name` - public
- `_Name` - private
- `_name` - protected
- `name` - internal
- `-name` - private protected
- `-Name` - internal protected

### Static and Constant Members

- Static members are denoted by prefixing the member name with a `|` character: `|MemberName`.
- Constant members are denoted by prefixing the member name with an `=` character: `=MemberName`.
