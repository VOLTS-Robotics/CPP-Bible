# Data Types

## Bits and Bytes

In digital electronics everything is binary, on or off. This can be used to represent numbers using a counting system called binary. A single binary number is called a **bit**. 

By itself a single bit can only represent either 1 or 0, so we usually refer to a combination of 8 bits, called a **byte**.

When you store a value in memory, a combination of bytes is stored in ram at a specific memory address. By doing this we can store, retrieve and manipulate the given value.

## Primitive Data Types

Primitives are concept in programming which refer to the most basic data types within a language. These data types include the following:

* **Integer** - Stores whole numbers (4 bytes)
* **Float** - Stores floating point numbers (numbers with decimal places) (4 bytes)
* **Double** - Stores floating point numbers with double the precision (8 bytes)
* **Char** - Stores characters (1 byte)
* **Bool** - Stores binary, true or false, 1 or 0 (1 byte)

## Derived Data Types

Derived data types are data types built upon primitives.

* **Arrays** - A series of values stored side by side in memory
* **Strings** - A series of characters stored side by side in memory
* **Enumerations** - Defines a set of named integer values
* **Functions** - Defines a block of reusable code to be called later in a program

# Primitives in Code

Instantiating variables using data types is simple. First you choose what data type you want your variable to store, proceeded by the name of the variable. 

You can instantiate a variable without an assigned value, this effectively saves the corresponding amount of bytes within memory or you can assign a value at instantiation, which will assign that value to the address in memory immediately.

Once you have a variable, you can use it as if it were that data type but with the additional functionality of having a single stored value.

## Integers

Integers abide by simple algebraic operations with an additional operation you mey be unfamiliar with called **modulo**.

Modulo simply returns the remainder after a division operation. This is incredibly important for control flow which will be discussed in the next section.

```cpp
int x = 5;
int y = 4;

//Addition with inline integer
std::cout << x + 5 << std::endl; //prints 10

//Addition
std::cout << x + y << std::endl; //prints 9

//Multiplication
std::cout << x * y << std::endl; //prints 20

//Division
std::cout << x / 2 << std::endl; //prints 2

//Modulo
std::cout << x % 2 << std::endl; //prints 1

//Exponent
std::cout << x ** 2 << std::endl; //prints 
```

## Floats and Doubles

Floats and doubles also abide by basic algebraic operation but without the modulo operator as any division that occures will have its remainder expressed as a decimal value.

```cpp
float a = 5.0f
float b = 2.0f;

//Addition
std::cout << a + b << std::endl; // 7

//Subtraction
std::cout << a - b << std::endl; // 3

//Multiplication
std::cout << a * b << std::endl; // 10

//Division
std::cout << a / b << std::endl; // 2.5
// no modulus with floats

```

## Characters

Characters behind the scenes are actually just integers representing a character within the ascii table. When arithmetic is done on characters they are cast into integers and will return an integer value, unless cast back into a character.

```cpp
char c1 = 'A';
char c2 = 2; 

//Print character to terminal
std::cout << c1 << std::endl;        // prints 'A'

//Characters are integers mapped to the ASCII table
std::cout << c1 + c2 << std::endl;   // 67 ('A' is 65 in ASCII)

//Adding char
std::cout << char(c1 + c2) << std::endl; // 'C'

```

## Bools

Boolean values deal with binary information and therefore have their own operators for boolean algebra. These values being AND, OR, and NOT. 

* AND returns True if both bool values are the same.

* OR returns True if at least one of the bools is True.

* NOT returns the opposite of a single bool value.

```cpp
bool t = true;
bool f = false;

// AND statement
std::cout << (t && f) << std::endl;  // 0

// OR statement
std::cout << (t || f) << std::endl;  // 1

// NOT statement
std::cout << (!t) << std::endl;      // 0

// Conditional statement
std::cout << (3 > 2) << std::endl;   // 1
```


# Derived Data Types in Code

## Array

Arrays are one of the most important data types in C++ when we are dealing with anything that is represented by multiple values, geographic data, surveys, census data, a deck of cards, etc.

Each value within the list acts as its defined data type, the only difference is that they are stored together in memory. This makes grouping values together much easier as it is expressed as a single variable.

For the time being we can only do simple modification and indexing until we learn control flow. Just know that an arrays index starts at 0, so an array 5 long actually has indexes 0 to 4. We can access and modify values within an array by using the square brackets [], along with what index we want to access.

```cpp
int numbers[5] = {10, 20, 30, 40, 50};

//Retrieving information from arrays via index
std::cout << numbers[0] << std::endl; //Prints the character at index 0 (the first)
std::cout << numbers[4] << std::endl; //Prints the character at index 4 (the last)

//Modify a value in an array
numbers[2] = 99;
std::cout << numbers[2] << std::endl;
```

## String

A string is a  list of characters stored together in memory. It is effectively an array for characters with the extended functionality to be displayed as text. Instantiating a string is much simpler and indexing works just the same.

Note that this data type is a part of the standard library and must be imported from the standard library before use.

```cpp
#include <string>

...

string text = "Hello";

// print the string
std::cout << word << std::endl;

//Access characters by index
std::cout << word[0] << std::endl; //Prints the character at index 0 (the first)
std::cout <<  word[word.size() - 1] << std::endl; //Prints the last character in a string

//Modify a character
word[1] = 'a';
std::cout << "Changed word: " << word << std::endl;

//Concatenate strings
std::string greeting = word + " World!";
std::cout << greeting << std::endl;
```