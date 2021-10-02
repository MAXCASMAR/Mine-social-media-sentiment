# Python Basics
## 1. Strings

Formatting strings

name = "John"
print("Hello {}".format(name))
print("Hello {}, you are {} years old!".format(name, 28))

# Chapter 1. #

Changing directories.

cd /Users/maxcasas/Documents/GitHub/Mine-social-media-sentiment

# Go backward, out of a folder
cd ..

Checking the directory.

# To the left of your username 

Making directories.

mkdir python_bootcamp

Creating files.

# cd int our python_bootcamp folder
cd /Users/maxcasas/Documents/GitHub/Mine-social-media-sentiment/python_bootcamp

# Type
touch example.txt

Checking a version number.

version

Clearing the terminal output.

clear

Using the Python Shell.

Python is a language that requires an interpeter to read an run the code we create. When the Python shell is activated, it acts as a local interpreter within the terminal session that is open. 

# To start the Python shell up, while we are in the directory of "python_bootcamp", type:
python

# Chapter 2: Python Basics. #

Comments.

# This is a comment

"""
This is a multi-line comment
"""

print("Hello") # This is a comment

What are data types?

Data types are how we define values. They define what we can do and how these values are stored in memory on the computer. 

# Data types   Sample Value    Description
# Integer      5               Whole numbers
# Float        5.7             Decimal numbers
# Boolean      True            True or False values
# String       "Hello"         Characters within quotes

The print statement.

It allows us to output information to the user, a function. 

Integers: They are positive or negative whole numbers with no decimal point.

# the following are all integers
print(2)
print(10)

Floats: Any time a number has a decimal point, floating point data types. 

# the following are all floats
print(10.953)
print(8.0) # even this number is a float

Booleans: A True or False value. One of the most common is for tracking whether something ocurred.

# the following are booleans
print(True)
print(False)

Strings: The most complex. String in Python are arrays of bytes representing unicode characters. Strings are a set of characters, symbols, numbers, whitespace, and even empty space between two sets of quotation marks. In Python we can use either single or double qutotes to create a string. Whatever is wrapped inside the quotation marks will be a string, even if it's a number. 

# the following are strings
print(" ")
print("There's a snake in my boot!")
print('True')

Exercises.

# print your name
print("Maximiliano")

# check the type of a value by using type()
type("Maximiliano") # str

**Variables.**

Variables allow us to save values into memory using a name that we assign. Python automatically handles memory storage and garbage collection for us.

How they work.

first_name = "John"

When you create a variable, the line where you assign the value is a step called declaration. Variable names can contain only letters, underscores, and numbers, and they cannot start with a number.

Handling naming erros.

Python is case-sensitive.

Integer and float variables.

num1 = 5         # storing an integer into a variable
num2 = 8.4       # storing a float into a variable
print(num1, num2)# you can print multiple items using commas

Boolean variables.

# storing a boolean into a variable
switch = True
print(switch)

String variables.

The use of single or double quotes matters.

# storing string into a variable
name = 'John Smith'
fav_number = '9'
print(name, fav_number) # will print 9 next to the name

Using multiple variables.

# using two variables to create another variable
result = num1 + num2
print(result)

Using operators on numerical variables.

# adding, deleting, multiplying, dividing from a variable
result += 1 # same as saying result = result + 1
print(result)
result *= num1 # same as saying result = result *num1
print(result)

Overwriting previously created variables.

# defining a variable and overwriting it's value
name = 'Jhon'
print(name)
name = 'Sam'
print(name)

Whitespace.

Whitespace just means characters which are used for spacing and have an empty representation. In the context of python, it means tabs and spaces. 

name = 'John Smith'

It makes reading the code easier. The computer ignores whitespace when compiling the code. Within the string, the space is NOT whitespace, a spacing character.

Excercises.

x = 3
y = 10
result = x * y
print("3 * 10 =",result)

**Strings**

Working with strings.

String concatenation.

# using the addfition operator without variables
name = "John" + " " + "Smith"
print(name)

# using the addition operator with variables
first_name = "John"
last_name = "Smith"
full_name = first_name + " " + last_name
print(full_name)

Formatting strings.

Write an entire string and inject the variables we want to use in the proper locations.

.format()

It works by putting a period directly after the ending string quotation, followed by the keyword format. Within the parenthesis after the keyword are the variables that will be injected into the string. No matter what data type it is, it will insert it into the string in the proper location. The order of the curly brackets is the same order for the variables within the format parenthesis. To include multiple variables, separate each by a comma. 

# injecting variables using the format method
name = "John"
print("Hello {}".format(name))
print("Hello {}, you are {} years old!".format(name, 28))

f Strings.

By putthing the letter f in front of a string, you're able to inject a variable into a string directly in line. It makes the string easier to read when it gets longer, making this the preferred method to format a string. To inject a variable in a string, simply wrap curly brackets around the name of the variable.

# using the new f strings
name = "John"
print(f"Hello {name}")

String Index.

How they are stored. When a computer saves a string into memory, each character within the string is assigned an index. An index is a location in memory. If you were at the front of the line, you would be given and index number of zero.

# using indexes to print each element
word = "Hello"
print(word[0]) # will output 'H'
print(word[1]) # will output 'e'
print(word[-1]) # will output 'o'

In order to index a specific element, you use square brackets to the right of the variable name. Within those square brackets, you put the index location you wish top access. Using negative index number will result in trying to access information from the back.

String Slicing.

When you want a piece of the variable.

print(word[0:2]) # will output 'He'

The first number in the brakcet is the starting index, the second is the stopping index. The syntax of slicing:

variable_name[start:stop:step]

The step is optional and defaults to incrementing by one each time. 

print(word[0:5:2]) # will output 'Hlo'

Exercises. 

w = 23
x = 4.5
y = False 
z = "Jhon"
print("{} {} {} {}".format(w, x, y, z))

name = "Maximiliano"
fav_sport = "tennis"
language = "Python"
print("{}'s favorite sports is {}.".format(name, fav_sport))
print("{} is working on {}.".format(name, language))

String Manipulation.

Alter string in one way or another. We want to alter what the current string is.

.title()

It capitalizes all first letters in each word of a string.

# using the title method to capitalize a string
name = "john smith"
print(name.title())
print(name.lower())
print(name.upper())

.replace()

Like a find and replace tool. It takes in two values within its parenthesis, one that it searches for and the other that it replaces the searched value with:

# replacing an exclamation point with a period
words = "Hello there!"
print(words.replace("!", "."))

For the replace to be stored properly afterward, we would havve to declare our words variable:

words = words.replace("!", ".")

.find()

It will search for any string we ask it to.

# finding the starting index of our searched term
s = "Look over that way"
print(s.find("over"))

It returns the starting index position of the match. 

.strip()

Where you want to get rid of a certain character on the left and right side of a string, you would use the strip method. By default, it will remove spaces.

# removing withe space with strip
name = "   john   "
print(name.strip())
print(name.lstrip())
print(name.rstrip())

.split()

It separates the words in the sentence into a group of words, stored within a list. 

# converting a string into a list of words
s = "These words are separated by spaces"
print(s.split(" "))

Exercises.

word = "uppercase"
print(word.upper())

string = "$$John Smith"
string.lstrip("$")

Creating a Receipt Printing Program.

Initial Process.

Whenever you begin a project, you must always understand where to start.No matter th size of the proje, tehre are certain dependencies. 

Defining our variables.

# create a product and price for three items
p1_name, p1_price = "Books", 49.95
p2_name, p2_price = "Computer", 579.99
p3_name, p3_price = "Monitor", 124.89

# create a company name and information
company_name = "coding temple, inc."
company_address = "283 Franklin St."
company_city = "Boston, MA"

# declare ending message
message = "Thanks for shopping with us today!"

# create a top border
print("*" * 50)

# print company information first, using format
print("\t\t{}".format(company_name.title()))
print("\t\t{}".format(company_address))
print("\t\t{}".format(company_city))

# print a line between sections
print("=" * 50)

# print out header for section of items
print("\tProduct Name\tProduct Price")

# create a print statement for each product
print("\t{}\t\t${}".format(p1_name.title(), p1_price))
print("\t{}\t\t${}".format(p2_name.title(), p2_price))
print("\t{}\t\t${}".format(p3_name.title(), p3_price))

# print a line between sections
print('=' * 50)

# print out header for section of total
print("\t\t\tTotal")

# calculate total price and print out
total = p1_price + p2_price + p3_price
print("\t\t\t${}".format(total))

# print a line between sections
print("=" * 50)

# output thank you message
print("\n\t{}\n".format(message))

# create a bottom border
print("*" * 50)

## 2. Lists

It is a data collection type, which can store multiple items. A list is a data structure in Python that is a mutable, ordered sequence of elements. Mutable means that you can change the items inside, whilde ordered sequence is in reference to index location. The first element is located at index 0. Each element or value that is inside of a list is called an item. Lists are defined by having different data types between square brackets []. Each item within a list is assigned an index, or location, for where that item is saved in memory.

Declaring a List of Numbers.

# declaring a list of numbers
nums = [5, 10, 15.2, 20]
print(nums)

Accessing elements within a list.

Use an index. When we declare our list variable, each item is given an index.

# accessing elements within a list
print(nums[1]) # will output the value at index 1 = 10
num = nums[2]  # saves index value 2 into sume
print(num)

Declaring a list of mixed data types.

Lists can hold any data type.

# declaring a list of mixed data types
num = 4.3
data = [num, "word", True] # the power of data collection
print(data)

Lists within lists.

# understanding list within lists
data = [5, "book", [34, "hello"], True] # lists can hold any type
print(data)
print(data[2])

Accessing lists within lists.

How we can access the items within the inner list. When the item is another list, you simply add another set of brackets.

# using double bracket notation to access lists within lists
print(data[2][0]) # will output 34
inner_list = data[2] # inner list will equal [34, "hello"]
print(inner_list[1]) # will output "hello"

Strings can also be indexed.

print(data[1][0]) # will output "b"

Changing values in a list.

# changing values in a list through index
data = [5, 10, 15, 20]
print(data)
data[0] = 100 # change the value at index 0 - (5 to 100)
print(data)

Variable storage.

When variables are declared, the value assigned is put into a location in memory. These locations have a specific reference ID. Use the id() to check the storage location in memory for a variable.

a = [5, 10]
print(id(a)) # large number represents location in memory

When a list is stored in memory, each item si given its own location. Changing the value using index notation will change the value stored within that memory block. If a variable's value is another variable:

a = [5, 10]
b = a

Changing the value at a specific index will change the value for both lists. 

# understanding how lists are stored
a = [5, 10]
b = a
print("a: {}\t b: {}".format(a, b))
print("Location a[0]: {}\t Location b[0]: {}".format(id(a[0]),id(b[0])))
a[0] = 20 # re-declaring the value of a[0] also changes b[0]
print("a: {}\t b: {}".format(a, b))

They share the same memory location. 

Copying a list.

How do you create a similar list without altering the original?

# using [:] to copy a list
data = [5, 10, 15, 20]
data_copy = data[:] # a single colon copies the list
data[0] = 50
print("data : {}\t data_copy: {}".format(data, data_copy))

You can also use the method .copy()

Exercises.

# 1. Define a list of strings, where each string is a sport. Then output each sport with the following line "I like to play {}"...
sports = ["fut", "futbol"]
for x in sports:
    print("I like to play {}".format(x))
# 2. First Character: For the following list, print out each item's first letter
names = ["John", "Abraham", "Sam", "Kelly"]
print(names[0][0], names[1][0], names[2][0], names[3][0])

Working with lists.

Checking length.


How many items are within a list with len().

# checking the number of items within a list
nums = [5, 10, 15]
length = len(nums) # len() returns an integer
print(length)

Slicing Lists.

Slicing follows the same arguments as the range function start, stop, step:

# accessing specific items of a list with slices
print(nums[1:3]) # will output items in index 1 and 2
print(nums[::2]) # will print every other index - 0, 2, 4, etc.
print(nums[:2]) # will output items in index 0 and 1
print(nums[-2:]) # will output the last two items in list

By default, start is zero and step is one. If you use a negative number in the start or stop positions, then the slice will either start or stop further from the back. 

Adding items.

Two methods.

.append()

Add the value withing the parenthesis to the back of the list. 

# adding an item to the back of the list using append
nums = [10, 20]
nums.append(5)
print(nums) # outputs [10, 20, 5]

.insert()

This method requires an index to insert a value into a specific location. 

# adding a value to the beginning of the list
words = ["ball", "base"]
nums.insert(0, "glove") # first number is the index, second is the value

Removing items.

.pop()

The pop method removes the last item in the list, but you can specify an index to remove. This method is used to save the removed item.It removes the item and returns it.

# using pop to remove items and saving to a variable to use later
items = [5, "ball", True]
items.pop() # by default removes the last item
removed_item = items.pop(0)
print(removed_item, "\n", items)

.remove()

Remove items from a list based on their given value:

# Using the remove method with a try and except
sports = ["baseball", "soccer", "football", "hockey"]
try:
    sports.remove("soccer")
except:
    print("That item does not exist in the list")
print(sports)

Working with Numerical List Data.

# using min, max and sum
nums = [5, 3, 9]
print(min(nums)) # will find the lowest number in the list
print(max(nums)) # will find the highest number in the list
print(sum(nums)) # will add all numbers in the list and return the sum

Sorting a list.

sorted()

It will work on numerical or alphabetical lists, but one that is mixed. It returns a copy of the list, so it doesn't alter the original. If you need to keep the original intact, use this function:

# using sorted on lists for numerical and alphabetical data
nums = [5, 8, 0, 2]
sorted_nums = sorted(nums) # save to a new variable to use later
print(nums, sorted_nums) # the original lists is intact

.sort()

It will change the original list directly.

# sorting a list with .sort()
nums = [5, 0, 8, 3]
nums.sort() # alters the original variable directly
print(nums)

Conditionals and lists.

Check if values exist. 

Using "in" and "not in" Keywords.

When working with lists, they serve a purpose to find values withing the list quickly.

# using conditional stataments on a list
names = ["Jack", "Robert", "Mary"]
if "May" in names:
    print("found") # will run since Mary is in the list
if "Jimmy" not in names:
    print("not found") # will run since Jimmy is not in the list

Checking an empty list.

# using conditionals to see if a list is empty
nums = [ ]
if not nums: # if nums == []
    print("empty")

Loops and lists.

Using for loops.

# using a for loop to print all items in a list
sports = ["Baseball", "Hockey", "Football", "Basketball"]
for sport in sports:
    print(sport)

Using while loops.

# using the while loop to remove a certain value
names = ["Bob", "Jack", "Rob", "Bob", "Robert"]
while "Bob" in names:
    names.remove("Bob") # removes all instances of "Bob"
print(names)

