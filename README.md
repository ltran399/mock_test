# mock_test
Notes:
%: remainder
//: integer only
Iterations: 
	1. For i in iterable 
	2. For i in range(start, stop, step)
	3. While condition:
	4. Break: exits the loop prematurely; continue: skip the current iteration and proceed to the next
	5. For index, item in enumerate(utterable): assessing both index and their values
	6. Iterating over dictionaries:
		- use for loop to integrate over keys(), values(), or items()(key-value pairs) 
		-ex: for name, score in students.items():
	7. Nested loop: a loop inside another loop to iterate over multiple sequences
	8. List comprehension:
		numbers = [1, 2, 3, 4, 5]
		squares = [x**2 for x in numbers]

Function:
	1. Fruitful: return a value
	2. Void: not returning any value
	3. Naming conventions: using lowercase letters and underscore
	4. Function documentation: explains purpose and usage of function (triple-quoted strings) “””…..””””
	5. Comment: #…. (Important)
Recursion:
1. Define base case: determine when the recursion stops
2. Recursive case: this is where the function call itself with modified inputs, moving towards the base case
EX:
def fibonacci(n):
    # Base cases
    if n == 0:
        return 0
    elif n == 1:
        return 1
    # Recursive case
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

result = fibonacci(7)  # Calculates the 7th Fibonacci number
print(result)  # Output: 13

Selection:
- If-else: statement (elif)
- Nested conditionals: multiple levels of ‘if’ and ‘else’
- Logical operators: ‘and’, ‘or’, ‘not’

Strings
- concatenation: str1 + str2 
- indexing: char = text[0]
- slicing: substring = text[0:3] ([start:stop:step])
- length: length = len(str)
- Methods: ALL STRINGS METHODS RETURN NEW VALUES. STRING IS NOT MUTABLE
capitalize()	Converts the first character to upper case
casefold()	Converts string into lower case
center()	Returns a centered string
count()	Returns the number of times a specified value occurs in a string
encode()	Returns an encoded version of the string
endswith()	Returns true if the string ends with the specified value
expandtabs()	Sets the tab size of the string
find()	Searches the string for a specified value and returns the position of where it was found
format()	Formats specified values in a string
format_map()	Formats specified values in a string
index()	Searches the string for a specified value and returns the position of where it was found
isalnum()	Returns True if all characters in the string are alphanumeric
isalpha()	Returns True if all characters in the string are in the alphabet
isascii()	Returns True if all characters in the string are ascii characters
isdecimal()	Returns True if all characters in the string are decimals
isdigit()	Returns True if all characters in the string are digits
isidentifier()	Returns True if the string is an identifier
islower()	Returns True if all characters in the string are lower case
isnumeric()	Returns True if all characters in the string are numeric
isprintable()	Returns True if all characters in the string are printable
isspace()	Returns True if all characters in the string are whitespaces
istitle()	Returns True if the string follows the rules of a title
isupper()	Returns True if all characters in the string are upper case
join()	Converts the elements of an iterable into a string
ljust()	Returns a left justified version of the string
lower()	Converts a string into lower case
lstrip()	Returns a left trim version of the string
maketrans()	Returns a translation table to be used in translations
partition()	Returns a tuple where the string is parted into three parts
replace()	Returns a string where a specified value is replaced with a specified value
rfind()	Searches the string for a specified value and returns the last position of where it was found
rindex()	Searches the string for a specified value and returns the last position of where it was found
rjust()	Returns a right justified version of the string
rpartition()	Returns a tuple where the string is parted into three parts
rsplit()	Splits the string at the specified separator, and returns a list
rstrip()	Returns a right trim version of the string
split()	Splits the string at the specified separator, and returns a list
splitlines()	Splits the string at line breaks and returns a list
startswith()	Returns true if the string starts with the specified value
strip()	Returns a trimmed version of the string
swapcase()	Swaps cases, lower case becomes upper case and vice versa
title()	Converts the first character of each word to upper case
translate()	Returns a translated string
upper()	Converts a string into upper case
zfill()	Fills the string with a specified number of 0 values at the beginning
- String formatting: format string using f-string
	formatted_str = f"My name is {name} and I am {age} years old."
- Escape sequences: ‘/n’ for newline and 
 	text = "This is a\nmultiline string."
- Comparison: CASE SENSITIVE, return boolean value
- String iteration: for char in str
- Conversion: num_str = str(num)

Lists: ARE MUTABLE (can change the values inside list)
- Definition: my_list =[a,b,c]
- Index: my_list[0]
- Modify list: my_list[0] = a
- List append: insert element to the end of list
- insert(): my_list.insert(1,10) (index, value)
- remove(): remove first occurrence of a value
- pop(index): remove and return the value popped
- Slicing: same as string
- Concatenation: same as string
- Methods: 
append()	Adds an element at the end of the list
clear()	Removes all the elements from the list
copy()	Returns a copy of the list
count()	Returns the number of elements with the specified value
extend()	Add the elements of a list (or any iterable), to the end of the current list
index()	Returns the index of the first element with the specified value
insert()	Adds an element at the specified position
pop()	Removes the element at the specified position
remove()	Removes the first item with the specified value
reverse()	Reverses the order of the list
sort()	Sorts the list
- Nested list: list contain other lists

Dictionaries: unordered collection of key value pairs, enclosed by braces ‘{}’. Each key is unique and it maps to specific value. 
- Ex: my_dict = {"name": "Alice", "age": 30, "city": "New York"} 
- Assessing values: name = my_dict[‘name’] //return ‘Alice’
- length: num_entries = len(my_dict) //return 3
- Mutability: my_dict[‘age’] = 31
- Check for key existence: if ‘age’ in my_dict:
- Adding and remove key-value pairs:
    - my_dict[‘country’]=‘USA’
    - Del my_dict[‘city’]
    - my_dict.update({key:value})
clear()	Removes all the elements from the dictionary
copy()	Returns a copy of the dictionary
fromkeys()	Returns a dictionary with the specified keys and value
get()	Returns the value of the specified key
items()	Returns a list containing a tuple for each key value pair
keys()	Returns a list containing the dictionary's keys
pop()	Removes the element with the specified key
popitem()	Removes the last inserted key-value pair
setdefault()	Returns the value of the specified key. If the key does not exist: insert the key, with the specified value
update()	Updates the dictionary with the specified key-value pairs
values()	Returns a list of all the values in the dictionary

FILES:
* File Modes: Files can be opened in different modes:
    * "r": Read mode (default). Opens the file for reading.
    * "w": Write mode. Opens the file for writing, truncating the file if it already exists or creating a new file if it doesn't.
    * "a": Append mode. Opens the file for writing, but appends data to the end of the file rather than overwriting it.
    * "b": Binary mode. Used in conjunction with other modes, like "rb" for reading a binary file.
    * "t": Text mode (default). Used in conjunction with other modes, like "rt" for reading a text file.
* Opening and Closing Files: You can open a file using the open() function and close it using the close() method to release system resources. ex: codefile = open("example.txt", "r") # Read or write operations file.close() 
* Reading from Files: You can read the contents of a file using methods like read(), readline(), or readlines(). ex: with open("example.txt", "r") as file: 
    * content = file.read()
* Writing to Files: You can write data to a file using methods like write(). with open("example.txt", "w") as file: file.write("Hello, World!") 
* Appending to Files: You can append data to the end of a file using methods like write() in append mode. with open("example.txt", "a") as file: file.write("\nAppending more data.") 
* Iterating through Files: You can iterate through a file line by line using a for loop. with open("example.txt", "r") as file: 
    * for line in file: # Process each line 
* Checking File Existence: You can check if a file exists using the os.path.exists() function. import os
*  if os.path.exists("example.txt"): # File exists 
* Handling Exceptions: When working with files, it's essential to handle exceptions, such as FileNotFoundError and PermissionError, that may occur during file operations. try: with open("example.txt", "r") as file: # File operations
*  except FileNotFoundError: print("File not found.") except PermissionError: print("Permission denied.") 
* File Management: Python provides modules like os and shutil for file and directory management tasks, such as creating, renaming, moving, and deleting files.
* Using with Statements: The with statement is recommended when working with files as it automatically closes the file when the block of code is exited, ensuring proper resource management.
	with open("example.txt", "r") as file: 
# File operations 
# File is automatically closed when leaving the 'with' block

OOP: typical example
class Animal: 
	def __init__(self, name): 
		self.name = name 
	def speak(self): pass 

class Dog(Animal): 
	def speak(self): 
		return f"{self.name} says Woof!" 

class Cat(Animal): 
	def speak(self):
		 return f"{self.name} says Meow!" 
	# Creating objects 
dog = Dog("Buddy") 
cat = Cat("Whiskers") 
	# Calling the speak method 
print(dog.speak()) # Output: "Buddy says Woof!" print(cat.speak()) # Output: "Whiskers says Meow!"

In this example, the Dog and Cat subclasses inherit from the Animal superclass and provide their own implementations of the speak method.

- Python calls the __str__method when used with your class object:
    - def__str__(self):
        - Return “<“+str(self.x)+”,”+str(self.y)+”>”
