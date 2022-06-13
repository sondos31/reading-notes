# Scopes:
The concept of scope rules how variables and names are looked up in your code
you can take 
# advantages of scopes: 
advantages of Python scopes to write more reliable and maintainable programs. Using Python scope will help you avoid or minimize bugs related to name collision as well as bad use of global names across your programs
The letters in the acronym LEGB stand for Local, Enclosing, Global, and Built-in scopes

# Scopes types:
1. Global scope: The names that you define in this scope are available to all your code.
2. Local scope: The names that you define in this scope are only available or visible to the code within the scope.
##
For example, if you assign a value to a name inside a function, then that name will have a local Python scope. In contrast, if you assign a value to a name outside of all functions—say, at the top level of a module—then that name will have a global Python scope.
When you can access the value of a given name from someplace in your code, you’ll say that the name is in scope. If you can’t access the name, then you’ll say that the name is out of scope.
#
# LEGB Rule for Python Scope:Python resolves names using the so-called LEGB rule, which is named after the Python scope for names. The letters in LEGB stand for Local, Enclosing, Global, and Built-in.
#

1.Local:
(or function) scope is the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. These names will only be visible from the code of the function
#

2.Enclosing (or nonlocal) scope is a special scope that only exists for nested functions. If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function
#

3.Global (or module) scope is the top-most scope in a Python program, script, or module. This Python scope contains all of the names that you define at the top level of a program or a module. Names in this Python scope are visible from everywhere in your code.
#

4.Built-in scope is a special Python scope that’s created or loaded whenever you run a script or open an interactive session. This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. Names in this Python scope are also available from everywhere in your code. It’s automatically loaded by Python when you run a program or script.


 # Scope Related Built-In Functions

•	globals ()
Python, globals() is a built-in function that returns a reference to the current global scope or namespace dictionary
•	Local ()
This function updates and returns a dictionary that holds a copy of the current state of the local Python scope or namespace
•	vars()
vars() is a Python built-in function that returns the .__dict__ attribute of a module, class, instance, or any other object which has a dictionary attribute
•	dir()
You can use dir() without arguments to get the list of names in the current Python scope.

# summary
The scope of a variable or name defines its visibility throughout your code. In Python, scope is implemented as either a Local, Enclosing, Global, or Built-in scope. When you use a variable or name, Python searches these scopes sequentially to resolve it. If the name isn’t found, then you’ll get an error. This is the general mechanism that Python uses for name resolution and is known as the LEGB rule.


