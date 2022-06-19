# List Comprehensions in Python

List comprehension is a powerful and concise method for creating lists in Python that becomes essential the more you work with lists, and lists of lists.

# Syntax

my_new_list = [ expression for item in list ]
#
# You can see three ingredients are necessary for a python list comprehension to work.

First is the expression we’d like to carry out. expression inside the square brackets.
Second is the object that the expression will work on. item inside the square brackets.
Finally, we need an iterable list of objects to build our new list from. list inside the square brackets.
Notes about Lists Comprehensions
List comprehension methods are an elegant way to create and manage lists. 
In Python, list comprehensions are a more compact way of creating lists. 
More flexible than for loops, list comprehension is usually faster than other methods
# Create a List with range()
#construct a basic list using range() and list comprehensions
#syntax
#[ expression for item in list ]
digits = [x for x in range(10)]

print(digits)


Output

[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

Create a List Using Loops and List Comprehension in Python
# create a list using a for loop
squares = []

for x in range(10):
    # raise x to the power of 2
    squares. Append(x**2)

print(squares)

[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# benefits of List comprehensions:

List comprehensions can make solving issues involving strings much easier using simplified expressions. These methods can save time and precious lines of code.

Using list comprehension to loop through a string in Python, it’s possible to convert strings from lower case to upper case, and vice versa. 

Making use of Python’s lower() and upper() methods, we’ll use list comprehension to achieve this common task.

Parsing a file using list comprehension

It’s also possible to read files in Python using list comprehension. To demonstrate, I’ve created a file called dreams.txt and pasted the following text, a short poem by Langston Hughes.

# Using functions in list comprehensions
#list comprehension with functions
#create a function that returns a number doubled
def double(x):
    return x*2

nums = [double(x) for x in range(1,10)]
print(nums)


Output

[2, 4, 6, 8, 10, 12, 14, 16, 18]


also we can use Filtering elements from the list can be done using additional arguments

