# Everything About Hello World
Let's breakdown our Hello World Script line by line.

```cpp
#include <iostream> 

int main() {
    std::cout << "Hello World!" << std::endl;
    return 0;
}
```

## Line 1

```cpp
#include <iostream>
```

This is one of the more intimidating files in our Hello World script as from a beginners perspective it has no logical connection to printing "Hello World!" to the screen. Before I get into this though I need to introduce one of the most import parts of C++. The Standard Library.

### C++ Standard Library (STL)

Flashback to the 1980's. C (the predecessor to C++) was an amazing programming language which was efficient, small, and ran close to the machine (code written in C directly mirrors that of machine code). This finegrained nature of C was a big strength but also a great weakness, as building large complex programs with C was tedious and prone to bugs. Writing code in C is like building a house brick by brick, everything is in your control which is fine for smaller buildings, but if you want to build a skyscraper by laying bricks out 1 by 1, you will not have a good time. The C++ Standard Library aims to take some of these bricks and make premade, reusable components out of them. Think stairs, arches, etc. Now the excrutiating task of building a skyscraper is much easier.

### C++ STL in Code

Back to the code, what does ```#include <iostream>``` have to do with the STL. This line of code actually takes a small portion of the STL named "iostream" and gives us the ability to use it in our own script. The "iostream" is short for "input output stream" and allows us to both read and write text from and to the terminal using a few simple commands. This level of **abstraction** prevents us from having to write our own code for interacting with the terminal, and instead allows us to use our precious brain power and allows us to focus on other things.

## Line 3, 5 and 6
```cpp
int main() {
  return 0
}
```
This is another intimidating section of code, but is actually very simple and will be used within every single C++ project. 

First let me explain the term "main".

### Main

When we run a line of code, our script goes through a series of consecutive steps that we outline for it in code. But in order for there to be consecutive execution of code, there needs to be a starting point. That is exactly what main is. Whenever we run a script, it runs the code within main first. As a result, every script we write will have a main "section".

### Main in Code

Look back at the lines of code defined in the section above. This structure defines a **function**, I don't want to get to much into functions right now, but all you need to know is that a function is a defined section of code that is run when it is called. By default, the function named main is run first as discussed earlier.

"int" stands for integer (number without decimal value) meaning that this function will "return" an integer. Return simply means that it will pass this number somewhere in code, not exactly print it to the terminal. In that same line we have ```main()``` this simply gives our function the name "main".

On line 5 we have ```return 0```. On line 3 we state that this function should return an integer, this line of code fulffills that by returning the integer 0, everytime it is run.

Finally, we have the curly brackets. These brackets incapsulate sections of code that will be part of the main function. We will go more in depth on this in the syntax section.

This likely created more questions than it answered, but for the time being, the main takeaways should be the following.
1) Main is the entry point of our code, anything in this section will be run first.
2) Main is a function, which is a grouping of code that is run when **called**. When our code is run the **main function** is always called first.
3) We define what kind of data a function is allowed to return. Main should always return an integer defined by int.


# Line 4

```cpp
std::cout << "Hello World!" << std::endl;
```
This is the only line of code that actually carries out our intended function. Everything else is commonly referred to as **boiler plate**, boiler plate code is simply the repetitive portion of code which must be written for everything else to work. It is our setup code.

### Cout

We start of this line of code with ```std::cout```. Cout is a portion of code that we previously imported from the standard libarary. It stands for "character output" and allows us to print text characters to the terminal. The ```std::``` portion of this code states that we are going to call a portion of code within the standard libarary where ```cout``` states what function from that library we are calling. This is followed by ```<<```, this states that we are going to print whatever follows this to the terminal, in our case ```"Hello World!" << std::endl;```. This simply will print "Hello World!" followed by an endline character, which as you could have guessed, is a part of the standard library iostream.
