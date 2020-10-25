# Python Tutorial


## Running code

Use the following website to run and test code:

[Online Python Code Runner](https://www.tutorialspoint.com/execute_python_online.php)

To write code, type in the left window. To run the code, click the "Execute" button in the top right. Output will be displayed in the right window.

</br>


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
