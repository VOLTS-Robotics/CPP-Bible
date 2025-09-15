# Getting Started

This section aims to help create a barebones programming environment installing the **g++ compiler** and configure Visual Studio Code, which we will refer to as **VS Code** going forward.

## Installing G++

### Windows Users

Installing g++ on windows is a little bit of a hassle, however Microsoft includes good tutorials on getting started. I recommend the tutorial linked here, https://code.visualstudio.com/docs/cpp/config-mingw.

### Linux Users

Linux users will have the easiest time getting started as installing g++ is as simple as running the following commands within the bash terminal.

First you should update your existing packages using the following command.
``` bash
sudo apt update
```

To install g++ run the following command. This will install a myriad of development tools, but we will just be using g++.
```bash
sudo apt install build-essential
```

To verify your installation, run the following command. If installed properly you should see the compiler version. If it doesn't do this I genuinely have no idea what you did to break it.
```bash
g++ --version
```

## Installing and Configuring VS Code.

VS Code is what is called an IDE (Integrated Development Environment). It is essentially a program that wraps together everything you would need for a coding environment, writing, running, testing. There are many other IDE's you can choose from and even some text editors such as VIM and EMACS.

VS Code stands alone as the most popular IDE due to its simplicity. Do not confuse simplicity with beginner friendly though, as this IDE contains everything you may need for most programming tasks and has seen consistent use throughout the industry.

This is genuinely the only one I would recommend to anyone, unless unusual circumstances dictate otherwise.

### Installation

To install VS Code on any device, go to the following link and install it as you would any program. https://code.visualstudio.com/download.

### Configuration

To configure VS Code to work easily with C++, go to the extensions tab in VS Code and search for C/C++ extension. Install this extension.
Assuming you are new to programming a lot of what this extension does will be lost on you for now, but I will be sure to point out how it helps us as we move forward and refine our coding chops.

## The Terminal
The last tool, but definitely the most important is the **terminal**. On Windows you have the command prompt, and Linux the bash terminal. There are some differences between these but they serve the same purpose.

### What is it?
The terminal is an interface that helps us navigate files, and compile and run code. It seems redundant since we have the file explorer, and we can click a button within our IDE to compile and run code. However, when we explore files, and when we click the run code button, all it is doing is opening a hidden terminal and running these commands automatically.

It is imperitive that we build a mental model of what is happening, or else we will struggle to learn the nuance of what is actually happening. And when it comes to **Compilation** and **Runtime** understanding these nuances will help us greatly.

The action of hiding some of these finer details behind some trigger or activation is called **abstraction**, keep this in the back of your mind as it will pop up a lot when we write more complex code.


## Hello World

This is the first script that every beginner programmer writes. You don't need to understand it all right away as this is what we will explore in following sections. Instead we will use this as verification that we have installed everything correctly.

### Setting up your directory

Everytime we write code we will create a folder for it to live in. I will walk you through how to do it within the terminal. The reason why most choose to do this within the terminal is many.

1) The terminal for the most part is OS agnostic, if you know how to work the terminal on one system you know how to work it on others.
2) It seems redundant now but getting comfortable with the terminal will allow you to do things that can only be done within the terminal.
3) It is a smoother workflow, when we create a new directory within a terminal, we can step into that directory and we are all ready to compile and run code. Either way we still need to open the terminal and navigate there anyways, might as well hit two birds with one stone by making the directory in the terminal as well.

So follow me:

1) Open up your terminal (Command Prompt on Windows, Bash Terminal on Linux).
2) To step into folders use the command ```cd "name_of_file"```
3) To step out of folders use the command ``` cd ..``` where ".." is a universal code for "the file before the one I'm in"
4) Step into your Documents folder by running ```cd Documents```
5) Create a new folder called C++_Tutorials by running the command ```mkdir C++_Tutorials``` "mkdir" stands for "make directory" which makes it easy to remember
6) Step into this folder by running ```cd C++_Tutorials```
7) Make a new file called "helloworld.cpp" by running ```touch helloworld.cpp``` in linux and ```type nul > helloworld.cpp``` in windows.
8) Open VS Code within that folder by running ```code .``` where "code" is the command to open VS Code and "." means "in this folder"

VS Code should open within that directory, and you will see your file called "helloworld.cpp" in the file tree on the left hand side. Open this and paste the follwing code:
```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello World!" << endl;
    return 0;
}
```
Save this file and within the terminal compile this code by running ```g++ helloworld.cpp -o helloworld```, this will compile our human readable code into an executable file. To run this executable file in terminal run the command ```./helloworld```, this will print "Hello World!" to the screen.





