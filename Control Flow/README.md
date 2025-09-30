# Control Flow

In programming we use control flow to create more complex behaviors to solve problems. This includes conditional branches that only run when a certain condition is met, and blocks of code that run repeatedly until a condition is met.

Without control flow, programming is dumbed down to a less user friendly calculator.

# Conditional Branching

Conditional branching describes code that only runs when specific conditions are met. This adds a situational aspect to code which is required for some problems. The most basic form of conditional branching is the **if else statement**.

### If Statement:

The if else statement basicly states, **if** this condition is **True**, run this section of code, **else** run this section of code. Thankfully this expressed almost in human language which makes it simpler to think about and hopefully to understand.

A basic if statement is created by using the keyword if, followed by parenthesis containing a conditional statement. A conditional statement is simply an expression that either results in a boolean value, or is a boolean value.

```cpp
x = 5;
y = 2;

// Checks if X is equal to 5, if so, prints the following
if (x == 5){
    std::cout << "x is equal to 5" << std::endl;
}

// Checks if x + y is greater than or equal to 7, if so, prints the following
if (x + y >= 7){
    std::cout << "x is equal to 5" << std::endl;
}

```

### Else If Statement:

We can expand this idea by introducing branches. This is a single if else statement with multiple conditions and blocks of code. This is created by following the previous "if" block with an "else if" block. 

Conditions in an "if else" block are checked consecutively, so if the first condition isn't true, it moves on to the second, and so on. 

```cpp
int score = 70;

if (score >= 90) {
    std::cout << "Grade: A" << std::endl;
} 
else if (score >= 80) {
    std::cout << "Grade: B" << std::endl;
} 
else if (score >= 70) {
    std::cout << "Grade: C" << std::endl;
} 
else if (score >= 60) {
    std::cout << "Grade: D" << std::endl;
} 
else if (score < 60){
    std::cout << "Grade: F" <<std::endl;
}
```

### The Else Block:

Notice how, the block of code that handles scores below 60 essentially covers all other grades. We can clean this up by using an else statement. The else statement is triggered if all other conditions in the if else statement are false. This serves as a default condition.

```cpp
int score = 70;

if (score >= 90) {
    std::cout << "Grade: A" << std::endl;
} 
else if (score >= 80) {
    std::cout << "Grade: B" << std::endl;
} 
else if (score >= 70) {
    std::cout << "Grade: C" << std::endl;
} 
else if (score >= 60) {
    std::cout << "Grade: D" << std::endl;
} 
else {
    std::cout << "Grade: F" <<std::endl;
}
```

## Switch Statements

The switch statement is a little bit trickier but ultimately fullfills a similar purpose to the if else statement, but is more efficient under certain circumstances. Let's talk about how we use it, and when we should use it.

The syntax of a switch statement can make it easier to read when there are many conditions. Additionally, the compiler can often optimize a switch statement better than the "if else" statement. This is because "if else" statements always run consecutively, whereas the switch statement does not.

To write a switch statement we use the syntax below.

```cpp

    int test_case = 1;

    switch (test_case) {
        case 1:
            std::cout << "Case 1" << std::endl;
            break;
        case 2:
            std::cout << "Case 2" << std::endl;
            break;
        case 3:
            std::cout << "Case 3" << std::endl;
            break;
        default:
            std::cout << "Default Case" << std::endl;
    }

```

There are a couple things new here. Firstly we define a switch block and pass it a case. Whenever this case value is equal to one of the defined cases, it will run everything within that case block, along with everything below it. This is often unwanted behavior so we use the break statement, once this statement is reached in code it will exit any loop, switch statement, or if else block.

Notice how we don't use a conditional in the switch statement. In a switch statement we are only able to use enums and integers as the case. This is both a limitation of the switch statement but also the reason why they can be optimized so heavily.

Here is an example of a switch statement utilizing an enum:

```cpp

enum Day {
    Monday,
    Tuesday,
    Wednesday,
    Thursday,
    Friday,
    Saturday,
    Sunday
};

Day today = Wednesday;

    switch (today) {
        case Monday:
            std::cout << "It's Monday";
            break;
        case Tuesday:
            std::cout << "It's Tuesday";
            break;
        case Wednesday:
            std::cout << "It's Wednesday";
            break;
        case Thursday:
            std::cout << "It's Thursday";
            break;
        case Friday:
            std::cout << "It's Friday";
            break;
        case Saturday:
            std::cout << "It's Saturday";
            break;
        case Sunday:
            std::cout << "It's Sunday";
            break;
        default:
            std::cout << "Unknown day";
    }
```

# Loops

A loop is a type of control flow that repeats a block of code until a condition is met. This is one of the most useful types of control flows as it allows us to do things such as, iterate through lists, continuously modify a value, and can serve as a program loop such as in arduino or video game code.

## While Loop

The most basic loop is the while loop. This loop will check the intial condition, run code within the block, then check the condition again, repeatedly, as shown in the diagram below. 

![While loop diagram](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAALcAAAEUCAMAAABeT1dZAAAA8FBMVEX///+y1Ov5tGEAAAC5ubn8/PwyMjL5+fnq6ur/uWSWlpZjY2Pd3d3w8PC32vLOzs6vr6/pq1yCgoKkw9h4d3aLi4txTiFfc4Bxb25YbHlLS0sdHR2Pq73FkU2MZTQ0OT3i4uLDw8O3t7f/vmbD6f+dnZ0nLjOkpKSPj4/Ly8trf413jp08PDxVVVUPDw9nZ2dZQCNtUiyBmqqbuMw+SlJRYGoXGx6VscRDQ0MoKCihdD/XnlVINBxIVl+qyuCEna4kJCS2hEcvIhMOER)

Here is an example below:

```cpp
int x = 0;
while(x < 5){
    std::cout << x;
    x++
}
```

This program simply increments x until x is 5. This program would output 01234.

I often like to use a while statement with a (True) condition paired with a condition within the for loop to break out of it. This can give more control on when and where your loop ends.

```cpp

int list[] = {1, 2, -2, 4, 5};
int i = 0;

while(true){
    if(list[i] < 0){
        std::cout << "Integer is negative" << std::endl;
        break;
    }
    else{
        std::cout << "Integer is positive" << std::endl;
    }
    i++
}
```

This example will simply iterate through the list printing whether a number is positive to the terminal then ending once a negative number is encountered.


## Do While Loop

A do while loop is similar to the while loop except for the order it checks its condition. Instead of checking the conditional statement before code is executed, it checks afterwards.

This is useful if you want your code to run at least once. Here is an example.

```cpp
char input;
    do {
        std::cout << "Message" << std::endl;
        std::cout << "Print message again (Y/N): ";
        std::cin >> input;
    } while (input == 'Y' || input == 'y');
```

This example will ask the user if they want to see the message again and wait for input. If the input is 'y' or 'Y' it will repeat. A do while loop is used here because we want to display the message at least once before prompting the user if they want to see it again.

## For Loop

In a previous example of the while loop we did a few things. We instantiated an integer to increment, we incremented this integer, and we used this integer to create a condition. Fortunately, a for loop can do all of this for us, making it easier to write, understand, and read. Here is an example.

```cpp
int numbers[] = {10, 20, 30, 40, 50};
int size = sizeof(numbers) / sizeof(numbers[0]);

for (int i = 0; i < size; i++) {
    std::cout << numbers[i] << std::endl;
}
```

This example will print every number within the array