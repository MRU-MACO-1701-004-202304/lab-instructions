# Lab-16: More Loops

**Will this madness never end?!?**

## Overview

This lab will give you further practice working with loops. Because loops are cool.

## Do These Things

You can do these exercises in any order you'd like.

### Exercise: Factorial Finder

The "factorial" of an integer is the product of that integer and all the integers less than it. It is denoted with an exclamation mark (!). So,

    n! = n * (n-1) * (n-2) * ... * 2 * 1
    
1. Write a function called `factorial` that computes the factorial of a given integer using a while loop. 

    ```python
    # example use
    factorial(0)  # should return 1
    factorial(1)  # should return 1
    factorial(2)  # should return 2
    factorial(3)  # should return 6...
    ```

2. Write a simple `main()` that tests your function using `assert` statements.

---

### Exercise: Password Validation

Imagine you are creating an online service, and are writing the code that handles creation of user accounts. 
You must write write two Python functions to help you with your job:

1. The first function should be called `invalid_password`. It takes in a string and returns true if that string is an **invalid password**, and false otherwise. A password is considered invalid if it has fewer that 8 characters (use the `len()` function you used in laborial-08) or is one of these poor password choices:  
    - "password"  (case sensitive)
    - "12345678"

    ```python
    # example use
    invalid_password("h1")           # should return True; too short!
    invalid_password("12345678")     # should return True; poor choice
    invalid_password("password")     # should return True; another poor choice
    invalid_password("PASSWORD")     # should return False; not exactly "password"
    invalid_password("w00tw00tWOO!") # should return False; everything OK!
    ```

2. The second function should be called `valid_password_from_user`. It should prompt the user for a password and validate that password using a sentinel loop and the `invalid_password` function. It should return the validated password.


3. Once you think you have these functions working, use this code to test them:

    ```python
    def main():
        validated_password = valid_password_from_user()
        print(f"Yay - '{validated_password}' is a valid password!")


    main()
    ```

    Here is an example run of a working final result:
    <pre>
    choose a password: <b>1234</b>  
    Oops - password must be at least 8 characters long and not 'password' or '12345678'!   
    choose a password: <b>password</b>  
    Oops - password must be at least 8 characters long and not 'password' or '12345678'!  
    choose a password: <b>12345678</b>  
    Oops - password must be at least 8 characters long and not 'password' or '12345678'!  
    choose a password: <b>password1</b>  
    Yay - 'password1' is a valid password!
    </pre>

---

### Exercise: Right-angled Triangle

Design and write a complete Python program that prompts the user for a base size (in `*` symbols), and then prints an right-angled triangle with that base width. If the input is **even** or **negative** then the program must terminate with an appropriate error message. 

For example:

<pre>
enter base (must be positive and odd): <b>4</b>
Base is not a positive odd number. Exiting.
</pre>

<pre>
enter base (must be positive and odd): <b>-5</b>
Base is not a positive odd number. Exiting.
</pre>

<pre>
enter base (must be positive and odd): <b>3</b>

*
***
</pre>

<pre>
enter base (must be positive and odd): <b>5</b>

*
***
*****
</pre>

As always, a good way to help in problem solving is to draw pictures, and to see what should happen with sample data (e.g. we have shown you base sizes 3 and 5 – try drawing out 7 and 9). Examine the required output to find a pattern....

Come up with a high-level solution in pseudocode, then implement and test your solution.