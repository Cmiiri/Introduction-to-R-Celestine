##Decision making in R we use if ,if else and else

Signs(comparison operators) TRUE and FALSE

Equals to we use ==

Not equal to we use !=

Greater than we use \>

Less than we use \<

Greater than or equal to we use \>=

Less than or equal to we use \<=

#create a vector of ages of students

```{r}
age <- c(15,20,25)
# who is older than 18
age > 18
```

```{r}
##[1] FALSE TRUE TRUE

```

```{r}
# who is younger than 30
age < 30

```

```{r}
##  who is younger than 30?

```

## Operators

These are used to ask questions ,more than one question at once

AND & - meaning both conditions must be TRUE

OR \| meaning at least one condition must be TRUE

```{r}
# sudent ages
age <- c(15,20,25)

#who is between 19 and 29?
(age>18) & (age<30)
```

[1] FALSE TRUE TRUE

```{r}
# Who is younger than 18 OR older than 24?
(age<18)| (age>24)
```

[1] TRUE FALSE TRUE

## if statement

This is a command used to execute a decision if the condition is TRUE

```{r}
age <- 20
if(age>=18){print("You are an adult")}
```

[1] "You are an adult'

```{r}
a <- 30
b <- 220

if (b>a){print("b is greater than a")}
```

[1] " b is greater than a"

## else if statements

Used when we have more than one condition to check

if the first condition is FALSE ,R checks the else if condition next

This means:

1.Check condition 1,if FALSE , check condition 2

2.  if still FALSE , check condition 3 and so on

3.  if no are TRUE go to else

    ```{r}
    a <- 30
    b <- 30

    if(b>a){print("b is greater than a")} else if(a==b){print("b is equal to a")}


    ```

```{r}
age <- 16
if(age>=18){print("Adult")}else if(age>=13){print("Teenager")}else {print("Child")}
```

[1] "Teenager"

## else statement

used to specify what should happen when all previous conditions are FALSE

```{r}
a <- 30
b <- 220

if(b<a){print("b is less than a")}else {print("b is greater than a")}
```

[1] "b is greater than a"

```{r}
age <- 10

if(age>=18){print("Adult")}else if (age>=13) {print("Teenager")} else {print("Child")}
```

[1] "Child"

## Loops in R

This is a way to repeat a set of instructions multiple times without writing the code again and again/perform iterations.

It saves time ,reduces errors and produces a readable code.

In R we have two primary loops ;for and while.

## For loop

This is used when you want to repeat over a sequence or a list.

```{r}
for (x in 1:10) {print(x)}
```

[1] 1

[1] 2

[1] 3

[1] 4

[1] 5

[1] 6

[1] 7

[1] 8

[1] 9

[1] 10

you can nest if.....else statements in for loops

```{r}
dice <- 1:10
for (x in dice) {if(x==6){print(paste("The dice is",x,"football"))}else{print(paste("The dice is not football"))}}
  

```

## while loop

Used to repeat as long as the condition is TRUE

```{r}
i <- 1
while(i < 6){
  print(i)
  i <- i+1
}
```

we can combine while with if...else statement

```{r}
#create a while loop that prints `play a game football` if the player number is 6
player <- 1
while(player <= 6){
  if (player < 6){
    print("No football")
  }else{
    print("play a game football")
  }
  player <- player + 1
}
```

## Functions in R

A function is an object that has many related statements,accepts input and gives out an outcome

You can pass data called parameters into a function

It is used to automate tasks

## User-defined functions

The user writes them for tasks he or she does often

we use function() to create

```{r}
my_function <- function(){
  print("hello")
}
my_function()
```

[1] "hello"

```{r}
# A function to add two numbers
add_numbers <- function(a, b) {
  result <- a + b
  return(result)
}

add_numbers(5, 3)   # ??? 8
```

[1] 8

```{r}
# Function to check if someone is an adult or minor
check_age <- function(age) {
  if (age >= 18) {
    return("Adult")
  } else {
    return("Minor")
  }
}

check_age(20)   # ??? "Adult"
```

[1] "Adult"

```{r}
check_age(15)   # ??? "Minor"
```

[1] "Minor"

-   When you create a function in R, you can have either local or global variables

-   Local variables: exist only inside the function, are forgotten after the function finishes

-   Global variables: exist outside the function. Functions can read them Note: If you create a variable inside a function, it's local by default

    ```{r}
    #y is local variable

    add_five <- function(x) {
      y <- x + 5   
      return(y)
    }

    add_five(10)  
    ```

[1] 15

```{r}
#y is local variable
#let us confirm if y is actually a local variable by calling it outside the function
add_five <- function(x) {
  y <- x + 5   
  return(y)
}

add_five(10)  
```

[1] 15

```{r}
y
```

[1] 9

```{r}
#global variable
#z is a global variable

z <- 100    

multiply <- function(x) {
  result <- x * z  
  return(result)
}

multiply(2)   
```

[1] 200

-   When calling a function, you must provide the same number of arguments as the function expects.

-   In the example below, the function requires three pieces of information: fname, mname, and lname.

-   We pass all three as arguments when calling the function:

    ```{r}
    my_function1 <- function(fname, mname ,lname){
      paste(fname, mname, lname)
    }

    my_function1("Celestine", "Miiri", "Celestine")
    ```

[1] "Celestine Miiri Celestine"

-   This approach avoids relying on global variables outside the function.

-   Good coding practice: always pass everything a function needs as arguments to make your functions self-contained, predictable, and reusable.

    ## Built -in functions

    -   These are in base R, you just need to call and use them

        ```{r}
        # create a vector of numbers 1 to 10
        a1 <- 1:10

        #add the numbers in the vector
        sum(a1)        
        ```

        [1] 55

        ```{r}
        #obtain the mean/ average of the numbers
        mean(a1)     
        ```

[1] 5.5

```{r}
#get the square root of each number in the vector
sqrt(a1)         
```
