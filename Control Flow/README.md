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




# Loops

## While Loop

## Do While Loop

## For Loop