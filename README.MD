# Python Tutorial


## Running code

Codecademy course:

[Link to course](https://www.codecademy.com/learn/learn-python)

I think these are the lessons that you should focus on:

1. [Syntax](https://www.codecademy.com/courses/learn-python/lessons/python-syntax/exercises/print-statements)
2. [Strings & Console Output](https://www.codecademy.com/courses/learn-python/lessons/strings--console-output/exercises/strings)
3. [Conditionals & Control Flow](https://www.codecademy.com/courses/learn-python/lessons/conditionals--control-flow/exercises/go-with-the-flow)
4. [Functions](https://www.codecademy.com/courses/learn-python/lessons/python-functions/exercises/what-good-are-functions)
5. [Lists and Dictionaries](https://www.codecademy.com/courses/learn-python/lessons/python-lists-and-dictionaries/exercises/introduction-to-lists)
6. [Loops](https://www.codecademy.com/courses/learn-python/lessons/python-2-loops/exercises/while-youre-here)

</br>

You can also use the following website to run and test code:

[Online Python Code Runner](https://www.tutorialspoint.com/execute_python_online.php)

To write code, type in the left window. To run the code, click the "Execute" button in the top right. Output will be displayed in the right window.

</br>

- - -
## Variables

Variables are things that hold values. It's the same concept as in Math, where you may have "x + 5", and you say that x = 5. "x" is simply a variable that is holding the value 5.

</br>

### **Data Types**

As mentioned before, we have variables that hold values. There are various types of values that we can assign to a variable. The most basic types of values that we can store are:

1. numbers
    * Numbers can be broken into two types:
        1. ints: integer numbers
        2. floats: floating point (decimal) numbers
2. strings
    * Strings are anything that is wrapped by quotation marks
    * ex:
        * "Hello"
        * "Hello World"
        * "High 5"
    * It's important to consider that numbers in strings are different from normal numbers
        * For example, "5" is different from 5. "5" is a string, but 5 is a number value.
3. booleans
    * booleans represent two values, either true or false
    * they are especially useful for conditionals (if else statements) that will be covered later

In summary, numbers, strings, and booleans are the most basic data values that can be stored in a variable.

</br>

### **Assigning values to variables**

Link for reference: [Link](https://www.w3schools.com/python/python_variables.asp)

When we have variables, we need to assign them values

Let's say we have a variable x, we want to assign it the value of 5. To do so, we use "=".

    x = 5

So now we know how to assign number values.
Next, we want to learn how to assign string values. As mentioned before, strings are enclosed by quotation marks. So let's say we have a variable called name, and we want to assign it the value "John", we do:

    name = "John"

Let's say we want a variable that holds whether someone is in school (where true means they are in school), we would do:

    inSchool = true

One thing to notice with the last example is how we wrote the variable name. Variable names cannot have any spaces in them. Here are some rules for naming variables:

1. a variable name must start with a letter or the underscore character
2. a variable name cannot start with a number
3. a variable name can only contain letters, underscores, and numbers

Another important rule is that variable names are case sensitive. So

    xy = 5
    xY = 5

are two different variables.

Variables can also be reassigned, which means that we can assign new values to variables and replace their old value.
For example

    x = 5
    x = 6

Here, the final value of x is actually 6. We first give x the value of 5, then we reassign it to store the value of 6.
We now have the basic concept of variables and assignment, now let's see what we can do with variables.

</br>

### **Arithmetic and String concatenation**

For variables that store numbers, we can do arithmetic operations with them.
The following operations are supported

    + : add
    - : substract
    * : multiply
    / : divide
    % : modulus, returns the remainder of a division operation
    ** : exponent

Here are some examples of the above operations
Note that the text on the same line following the pound sign (#) are comments. Comments are text that is not run, it is simply just plain text that can be used within your code to add any comments that might explain logic, etc.

    x = 5
    y = 6

    # we assign variable z to the value of x + y, so z equals 11
    z = x + y 

    # we reassign z to the value of x - y, so z equals -1
    z = x - y

    # we reassign z to the value of x * y, so z equals 30
    z = x * y

    # we reassign z to the value of x / y, so z equals 0.83333333333
    z = x / y

    # we reassign z to the value of x % y, so z equals 5. This is because y goes into x 0 times, and has a remainder of 5.
    z = x % y

    # we reassign z to the value of x ^ y, so z equals 15625
    z = x ** y

    # Note, arithmetic operations can occur by just using the values, we don't need to use variables
    # here we reassign z to the value of 1 + 2, so z equals 3
    z = 1 + 2

Another important consideration is to think about order of operations. Just like in math, we can use parenthesis to indicate what things might be calculated first.

    x = (5 + 5) * 2

Here, x ends up equaling 20, not 15.

Another thing to consider is that whatever is to the right of the equals sign is going to occur first. So the right of the equal sign will be calculated and then assigned to the variable on the left side. This means that we can do some modification of a variable like

    x = 5
    x = x + 1

Here, the final value of x is 6. If we look at the second line, we are doing the following things in order:

1. calculating x + 1, x was assigned to 5, so we are essentially doing 5 + 1
2. assigning the previous calculated sum to x, so 6 is assigned to x

We can do other things like

    x = 3
    x = x + x + x  

    y = 5
    y = 2 * y  

In the first example with x, x ends up being 9. In the second example with y, y ends up being 10.

</br>

So now we have an idea of some basic operations that we can do between variables that store numbers. Now let's consider strings.
Sometimes, we may want to add two string together. For example, we may have

    first = "John"
    last = "Smith"

and we want to generate a new variable called fullName that stores someones full name. To do so, we can concatenate the first variable and the last variable. To concatenate, we use the **+** symbol.

    fullName = first + last

fullName now holds the string value: "JohnSmith"
So we're almost there, but we want to have a space between "John" and "Smith". To do so, we can just use our **+** operation.

    fullName = first + " " + last

fullName now holds the string value: "John Smith"
What we essentially did was similar to what we did before with the numbers. For example we might have

    x = 5
    y = 2
    z = x + 1 + y

We are just directly adding the value. So when we add the space string " ", we are just adding a string value

    major = "math"
    degree = "B.S."
    diploma = degree + " in " + major

Here, diploma has a final value of "B.S. in math"

Now we've covered some basic operations for string and numbers. Let's test that knowledge.

</br>

    x = 5
    y = 6
    z = (x + y - 5) % x

What's the final value of z?

<details>
    <summary>Click for Answer</summary>
    z = 1
</details>

</br>

    name = "John Smith"
    job = "office"
    hobby = "biking"
    description = name + " works at an " + job + " and enjoys " + hobby

What's the final value of description?
<details>
    <summary>Click for Answer</summary>
    description = "John Smith works at an office and enjoys biking"
</details>

</br>

- - -

## Conditionals

Link for reference:
[Link](https://www.w3schools.com/python/python_conditions.asp)

### **What is a conditional?**

A conditional is something that we use when we want code to only run under certain conditions.
In Python we have 3 conditionals:

1. if: code runs if a condition is met
2. elif (aka else if): if the previous condition was not met, we check this condition and run some code if it is met
3. else: if the previous condition was not met, we run some code

So I've mentioned the word condition a lot, let's look at what that actually means.

### **Conditions**

Conditions are essentially things that we check for. For example, a common condition is you have to be over 18 to vote. The condition there is that they have to be over 18. Here, we see that our conditions are often dealing with comparison between numbers.

Let's look at how we might compare two numbers:

    a == b : a is equal to b
    a != b : a is not equal to b
    a < b : a is strictly less than b
    a <= b : a is less than or equal to b
    a > b : a is strictly greater than b
    a >= b : a is greater than or equal to b

Great, now we have an understanding of how we might create our conditions. Let's combine that with the different conditionals (if, elif, else).

### **Conditional Statements**

Let's start with if statements. Let's take a look at a simple if statement

    a = 5
    b = 6
    if (a < b):
        print("Hello")

Here, we have two variables a and b. We then see our if statement where the condition is wrapped by parentheses. Then, we have the code that we want to run if a is less than b. Let's try to generalize this form

    if (...condition...):
        code
        that
        we
        want
        to
        run if condition is true

We can even nest if statements under each other

    if(a < b):
        print("A was less than B)
        if(a + 1 < b):
            print("A + 1 was less than B)

Here we first check if a < b, if that's true, we print "A was less than B". Additionally, if a was less than b, we also check if a + 1 < b., and if that's true, we print "A + 1 was less than B".

Now that we have the if statement down, let's add the else statement.
It's important to understand that the else statement needs to follow an if statement.

    if (a < b):
        print("A is less than B")
    else:
        print("A is not less than B")

The biggest thing to notice is that the else statementr does not have an condition. Instead, thinking about it as the negative of the condition in the if statement. Let's generalize this like we did before with the if statement

    if (...condition...):
        code
        to
        run
        if condition is true
    else:
        code
        to
        run
        if condition is false

Once again, we can nest if and else statements

    if(a < b):
        print("A < B")
    else:
        if(a == b):
            print("A == B")
        else:
            print("A > B")

Here, we see a conditional that first checks if a < b. Then if it isn't, it checks if a == b, and if that is not true, we know that since a < b and a == b are both false, then a > b.

Great, now the only issue that we have with the else statement, is that it does not accept any conditions. As we saw with the previous example, we had to add a nested if statement under the else to check if a == b. What if we could have an else and have it also check for a condition, we can do this using elif.

    if(a < b):
        print("A < B")
    elif(a == b):
        print("A == B")
    else:
        print("A > B")

As we can see, we are able to specifically check for the condition a == b in addition to have the else there. For else, we can only have one else statement. However, for elif, we can have mulitple.

    if(a < b):
        print("A < B")
    elif(a == b):
        print("A == B")
    elif(a + 1 == b):
        print("A + 1 == B")
    else:
        print("A > B")

Now what happens if we want to test multiple conditions at once, or if we want to do something only if some conditions are not met?

This is where three keywords come in:

    and
    or
    not

Let's discuss the first keyword. "and" is used when we want to check if a set of conditions are all met.

    if(a < b and a != 5):
        print("A < B and A != 5")

Here, we see that "A < B and A != 5" will only get printed if the two conditions are met. So if a < b but a == 5, nothing will be printed.

Now, let's discuss the second keyword. "or" is used when we want to check if at least one condition in a set of conditions are met.

    if(a < b or a != 5):
        print("A < B or A != 5")

Here, we see that "A < B or A != 5" will only get printed if at least one condition is met. So if a < b but a == 5, it will still get printed because the condition a < b is met.

Lastly, let's discuss the last keyword. "not" is used when we want to check if conditions are not met.

    if not(a == 5):
        print("A is not 5")

Here, we see that we have the condition a == 5, and we are only going to print "A is not 5" if the condition a == 5 is not met.
We can combine this with and & or.

    if not(a < b and a != 5):
        print("A > B or a == 5)

Here, we see that if either condition is not met, we will print something. The trick for understand conditions when "not" is used is think about the conditions as the following:

    not(condition_a and condition_b) 
    is the same as 
    not(condition_a) or not(condition_b)

So with the previous example we can think about it as

    not(a < b and a != 5) 
    is the same as 
    not(a < b) or not(a != 5)


Let's test some conditionals

    if(a < 60):
        print("F")
    elif(a < 70):
        print("D")
    elif(a < 80):
        print("C")
    elif(a < 90):
        print("B")
    else
        print("A")


What is printed if a = 50?
<details>
    <summary>Click for Answer</summary>
    F
</details>

 </br>

What is printed if a = 65?
<details>
    <summary>Click for Answer</summary>
    D
</details>

 </br>

What is printed if a = 75?
<details>
    <summary>Click for Answer</summary>
    C
</details>

 </br>

What is printed if a = 85?
<details>
    <summary>Click for Answer</summary>
    B
</details>

 </br>

What is printed if a = 95?
<details>
    <summary>Click for Answer</summary>
    A
</details>

 </br>

What is printed if a = 200?
<details>
    <summary>Click for Answer</summary>
    A
</details>

</br>

- - - 

## Functions

Link for reference:
[Link](https://www.w3schools.com/python/python_functions.asp)

A very important concept is the idea of functions (sometimes called methods). Functions are essentially pieces of code that you can call. If we think of it from a math standpoint, we have might have a function f(x) = x + 1. Here we would call the function f(x) and give it some value for x. So f(5) would return 6. Functions in Python behave exactly the same.

Let's start with some functions that you might be familiar with.

The print function is very common.

    print("Hello!")

This prints out

    "Hello"

As we can see, the print function takes in one argument, the string that you want to print.

Functions can essentially be broken into two components:

1. the function name
2. the arguments it accepts

</br>

### **Why functions**

Before we look at how to implement functions, let's look at why we want to use functions.

Look at the following code

    x1 = 5
    y1 = 5

    x2 = 3
    y2 = 3

    # dist is the euclidian distance
    dist = (((x2 - x1)**2) + ((y2 - y1)**2))**0.5

If we look here, we see that we are finding the distance between two points (x1, y1) and (x2, y2). Now here, it doesn't seem like there is anything to change, but let's consider if we have 500 pairs of points that we want to find the distance between. We don't want to have to write out the euclidian distance formula every single time. Instead, wouldn't it be easier if we had some distance function that accepted 4 arguments

    dist(x1, y1, x2, y2)

and return the distance. So here, we would have some function that has the code to calculate the distance. Let's look at that function next.


### **Defining Functions**

Let's first take a look at the dist function before:

    def dist(x1, y1, x2, y2):
        return (((x2 - x1)**2) + ((y2 - y1)**2))**0.5

There's a lot to cover in this example. First, let's look at how this function might fit into our program as a whole:

    def dist(x1, y1, x2, y2):
        return (((x2 - x1)**2) + ((y2 - y1)**2))**0.5

    def main():
        distance = dist(1, 1, 5, 5)

Here, the function main() is what is actually run by Python. So whenever you run a Python program, it will run what was in the main() function.

So the main() function is first going to get the distance between (1,1) and (5,5) by calling the function dist(x1, y1, x2, y2). You'll notice that we called dist by doing

    dist(1,1,5,5)

When we actually look at the dist function after calling it, the variables in dist get the values we passed to the dist function

    x1 = 1, y1 = 1, x2 = 5, y2 = 5

This may seem confusing but let's think back to our mathematical functions. In math we have some function f(x) = x + 1. We don't know the value of x, but we can pass the value of x to function f by doing

    f(5)

This means that the function f will now return 5 + 1.

You might also notice that in our function code, we have this keyword "return". This represents the value that we want to return back to whoever called the function. So when we did

    distance = dist(1, 1, 5, 5)

what is happening is

    dist function is called => the distance is calculated => the distance is returned and assigned to the variable called distance

The best way to think about it is that whatever is returned essentially replaces where we called the function.
So with our example

    distance = dist(1, 1, 5, 5)

dist returns 5.656 (with more digits). So in our head we can imagine that 5.656 replaces "dist(1, 1, 5, 5)" so that now

    distance = 5.656

So let's say we wanted to multiple that distance by 2, we might do

    distance = 2 * 5.656

And with what I just mentioned where whatever is returned replaces "dist(1,1,5,5)", we could instead do

    distance = 2 * dist(1,1,5,5)

and achieve the same result.

Now that we know a bit about functions, why don't we try to define a general form

Defining a function

    def function_name(arg1, arg2, arg3, ...):
        code
        that
        we
        want
        to run
        when the function is called

Calling a function

    function_name(value1, value2, value3, ...)

Now with the "return" keyword, we only use it when we actually want to return a value. Sometimes we may not want to return anything, and instead we want to just run some code. For example

    def printName(name):
        print(name)

In the above function, when the function is called, we will print whatever string is passed to it. When I say something is "passed" to a function, I mean the arguments/parameters that are in the parentheses

    printName("John")

Here we are passing "John" to the printName function.

Let's test some knowledge for functions

</br>

    def sum(num1, num2):
        return num1 + num2

What is the value of a in
    
    a = sum(1,5)

<details>
    <summary>Click for Answer</summary>
    a = 6
</details>

</br>

What is the value of a in

    a = sum(1,5) + sum(5,10)

<details>
    <summary>Click for Answer</summary>
    a = 21
</details>

</br>

    def isLess(num1, num2):
        return num1 < num2

What is printed if a = 5 and b = 6 in

    if(isLess(a, b)):
        print("A is less than B")
    else:
        print("A is not less than B")

<details>
    <summary>Click for Answer</summary>
    "A is less than B"
</details>

Notice for the above example, we actually used the return value of isLess as our condition. How does this work?
num1 < num2 is true if num1 is less than num2. As a result, isLess return true if num1 < num2. So the if statement is checking the return value of isLess, and will print "A is less than B" if isLess returns true.
