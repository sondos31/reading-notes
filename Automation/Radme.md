# regex,
 are a sequence of characters used to check whether a pattern exists in a given text (string) or not. If you've ever used search engines, search and replace tools of word processors and text editors - you've already seen regular expressions in use. They are used at the server side to validate the format of email addresses or passwords during registration, used for parsing text data files to find, replace, or delete certain string, etc. They help in manipulating textual data, which is often a prerequisite for data science projects involving text mining.
 
 
 # Regular Expressions in Python
In Python, regular expressions are supported by the re module. That means that if you want to start using them in your Python scripts, you have to import this module with the help of import:

import re
The re library in Python provides several functions that make it a skill worth mastering. You will see some of them closely in this tutorial.

# Basic Patterns: Ordinary Characters
You can easily tackle many basic patterns in Python using ordinary characters. Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.

# Most alphabets and characters will match themselves, as you saw in the example.

The match() function returns a match object if the text matches the pattern. Otherwise, it returns None. The re module also contains several other functions, and you will learn some of them later on in the tutorial.

For now, let's focus on ordinary characters!

Do you notice the r at the start of the pattern Cookie?
This is called a raw string literal. It changes how the string literal is interpreted. Such literals are stored as they appear.

For example, \ is just a backslash when prefixed with an r rather than being interpreted as an escape sequence. You will see what this means with special characters. Sometimes, the syntax involves backslash-escaped characters, and to prevent these characters from being interpreted as escape sequences; you use the raw r prefix.

TIP: You don't actually need it for this example; however, it is a good practice to use it for consistency.

# There is a predefined set of special sequences that begin with '\' and are also very helpful when performing search and match. Let's look at some of them up close...

\w - Lowercase 'w'. Matches any single letter, digit, or underscore.
\W - Uppercase 'W'. Matches any character not part of \w (lowercase w).



