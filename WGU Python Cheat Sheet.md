up:[[Python Course]]

myVar  = 5 # simple, single variable assignment

myVar  = myFunction() # variable assignment... assuming myFunction() **returns** a value

var1, var2, var3 = 1, 2, 3 # multiple variable assignment

 --- Data Types --- myInteger = 12 # variable assigned an integer

myFloat = 12.0 # variable assigned a float

myString = "twelve" # variable assigned a string

mySecondString = '12' # variable assigned a string

myBoolean = False # variable assigned a Boolean

dataType = type(myFloat) # determines data type/class of object

convInt = int(myFloat) # converts float to an integer

convFloat = float(myInteger) # converts integer to a float

convString = str(myInteger) # converts integer to string

print(round(4.8)) # rounds a float value to the nearest whole number

print(var1) # print command

# --- arithmetic operators ---

print( 2 + 2 )# addition

print( 2 - 2 ) # subtraction

print( 2 * 2 ) # multiplications

print( 2.1 / 2 ) # division, always results in float: 2.1 / 2 evaluates to 1.05

print( 2.1 // 2 ) # floor divisiion, gives the result of the last even division. Result will be a "mathematical integer" but whether it's a Python int or float depends on numbers used. 2.1 // 2 evaluates to  the float 1.0, while 5 // 2 evaluates to int 2

print( 5 % 2 ) # modulo (integer remainder), 5 % 2 evaluates to 1 (that's the 1 left over to get to 5 after 2 went into 4 evenly... see how floor division and modulo pair so well... 5 // 2 = 2, 5 % 2 = 1)

print( 2 ** 2 ) # power of.. 2\*\*2 evaluates to 4

# --- assignment/reassignment operators ---

myNumt = 10 # assignment

myNum += 5 # "add and"... adds to previous value

myNum -= 5 # "substract and"... subtract from previous value

myNum *= 5 # "multiply and"... multiply by previous value 

myNum /= 5 # "divide and"... divide by previous value

# --- comparison operators ---

myNum = 4 print( myNum < 2 ) # less than

print( myNum > 2 ) # greater than

print( myNum <= 4 ) # less than or equal to

print( myNum >= 2 ) # greater than or equal to

print( myNum == 2 ) # equal to print( myNum != 2 ) # not equal to

# --- string operations ---

# view all string methods: https://docs.python.org/3/library/stdtypes.html# string-methods

myCourse = "introduction to programming in Python"

courseLength = len(myCourse) # length function 

courseProper = myCourse.title() # capitalizes first letter of each word

confirmLower = myCourse.islower() # determines if the string consists of lowercase characters

statement = "I love Python. Working with Python is amazing because, hello, it's Python!"

countPython = statement.count('Python')

name = 'John Jacob Jingleheimer Schmidt'

name[0:4] # slice a string

username = "Connie"

code = "C859"

userMessage = "Welcome to {}, {}.".format(code, username)

print( userMessage )

myNewPhrase = "cowabunga dude"

mySplitPhraseList = myNewPhrase.split(" ") # split method, returns a list

print(mySplitPhraseList)

# --- function with both input and output ---

def areaOf(width,height):

  # function that accepts two inputs

  return width * height  # function body outputs calculated area

myArea = areaOf(4,6) # function call provides two arguments and saves return value to a variable -- we can assign a value with this function because it RETURNS a value

print( myArea ) # displays myArea

# --- if / elif / else statements ---

age = 16

if age < 16: # condition will evaluate to either True or False

  print('you are not old enough to drive') # if condition is True, execute this block

elif age >= 16 and age <= 18: # second condition will evaluate to either True or False

  print('you may drive with adult supervision') # if second condition is True, execute this block

else:

  print('you may drive a vehicle') # both earlier conditions are False, execute this block

# --- Boolean operations ---

 # Boolean and operation will always be false unless both sides are true 

bool01 = True and False # ... so it's False

x = 3

bool01a = (x == 3) and (x > 9) # False!

bool01b = (x == 3) and (x >2) # True!

bool02 = True or False # but that's True! OR combos are True when any single condition is True (pro tip: generally limit OR to joining 2 conditions -- any more than that and you're likely to have one evaluate True unexpectedly)

bool03 = not (True and False) _# True... since (True and False) is False, so the not flips it to True_

# # --- Lists ---

myNumbers = [1, 4.8, 7, 9.2, 3, 0] # creates list

print(myNumbers[3]) # prints the fourth number from the list

print(myNumbers[-1]) # prints the last element from the list

yourNumbers = myNumbers[1:3] # creates a new list (via a slice) with the second and third values from myNumbers

altNumbers = myNumbers[:3] # creates a new list (slice!) with 1st, 2nd, and 3rd values from myNumbers

newNumbers = myNumbers[3:] # creates a new list (sliced again!) with 4th, 5th, and 6th values from myNumbers

matchList = 9.2 in myNumbers # looks for a match and returns Boolean value... True here

noMatch = 9.3 not in myNumbers # ensures a match does not exist in list... also True here since list does not contain 9.3

listLength = len(myNumbers) # counts items in list

listMax = max(myNumbers) # returns greatest element of list

listMin = min(myNumbers) # returns smallest element of list

listSort = sorted(myNumbers) # returns copy of list ordered smallest to largest

listSortAgain = sorted(myNumbers, reverse=True) # returns copy of list ordered largest to smallest

listSum = sum(myNumbers) # returns total sum of list values

myNames = ['Jessica', 'Connie', 'Amy']

myNames.append('Grace') # new value is added to end of list

myNames.pop() # removes last item from the list

myNames.pop(1) # removes second item from the list

listJoined = ", ".join(myNames) # a string is used to join together values from list

print('Welcome aboard ' + listJoined)

# --- Sets ---

# note that sets aren't nearly as important to the OA as strings, lists, and dictionaries

idNums = set() # creates a new set, empty 

idNums.add(12345) # adds value to set

idNums.add(12367) # adds second value to set

idNums.add(12367) # adds third value to set, but it is duplicate so it will not be added

idNums.discard(12345) # removes value from set, if found

set(myNumbers) # converts the list from line 91 above to a set

list(idNums) # converts the set from line 121 into a list 

# --- For Loop ---

# a FOR loop is a natural fit for looping over a container item by item

cities = ['Albany', 'Chicago', 'Boulder', 'Tampa']

for city in cities: # performs commands for each item within list

  print('Welcome to the city of ' + city) _# or_

  _# print('Welcome to the city of {}'.format(city)) # get to know str.format() or the similar f strings way of building larger strings... concatenation with + gets old fast_

sum = 0

for num in range(1,5): # runs loop for numbers 1 through 4, as range is exclusive of the ending position

  sum += num

# --- While Loop ---

# a WHILE loop is like an IF that repeats as long as its condition stays True

temp = 34

while temp >= 32: # while condition is True loop will iterate

  print(temp) temp -= 1 # variable must change state, moving towards satisfying condition

print('it is freezing') _# loop is done (note indentation is moved back left), so temp must be down below 32 now_

startValue = 0

while startValue < 20:

  startValue += 1

  if startValue == 4: # if statement checks for a specific value

   break # stops the flow of the while loop prematurely

print(startValue) _# it's 4!_

# --- Dictionaries ---

studentGrades = { # dictionary is created

  'Orfu': 83, # first entry is added with key of str 'Orfu' and value of int 83

  'Bismark': 98,

  'Igor': 72

} # end of dictionary

if 'Igor' in studentGrades: # in verifies if key is in dictionary

  print('student is in course')

  print( studentGrades.get('Bismark') ) # get method looks up value by key, or...

  _# print(studentGrades**[**'Bismark'] ) # you can use the key as if it was an index (it's not, but the syntax is the same)_

for student in studentGrades: # for loop iterates over each entry in dictionary

  print('{}, you earned {} on the final exam'.format(student, studentGrades[student]))

# --- Tuples ---

# tuples aren't as important as strings, lists, and dicts either

# think of a tuple as a row of data... it is IMMUTABLE because you shouldn't just change the order of columns of data

myPhone = (877, 435, 7948) # tuple is created with three sections of a phone number

print( 'Call WGU at {}-{}-{}'.format(myPhone[0], myPhone[1], myPhone[2]) )

# --- Reading and Writing Files ---

# older, simpler, but more cumbersome syntax for opening files...

f1 = open('/my_path/my_file.txt','r') # opens a file object for reading (read-mode is default)... you can now use IO/filestream methods like read() and readlines() on f1

f1 = open('/my_path/my_file.txt','w') # opens a file object for writing and deletes what is in the file previously

f1 = open('/my_path/my_file.txt','a') # opens a file object for appending (don't worry about append mode for OA, just read and write modes)

f1.read() # reads the data from file into a string

f1.write('hello, friend') # writes to file

f1.readlines() # returns a list of strings, with each line of the file as one string entry

f1.close() # closes file 

_# a better structure for opening files!_

with open('/my_path/my_file.txt','r') as f: # opens a file, names if f (or whatever you like), performs operations and automatically closes file

  my_lines = []

  for line in f: _# looping directly over the file is also OK_

    my_lines.append(line.strip()) # this does essentially the same as what f.readlines() would do, except usign the string strip() method here removes newline characters

_# when you leave the with/open() block the file closes automatically_

# --- Modules & Python Standard Library---

# The only modules I would focus on for the exam are **math** and **csv**

**# math**

import math # imports the math module

print('The factorial of 3 is: {}'.format(math.factorial(3)))

print('The largest integer less than or equal to 5.6 is: {}'.format(math.floor(5.6))) _# 5_

print('The smallest integer greater than or equal to 5.6 is: {}'.format(math.ceil(5.6))) _# 6_

print('3 to the 5th power is: {}'.format(math.pow(3, 5))) _# 243.0_

print('The math constant e to the power of 3 equals: {}'.format(math.exp(3))) _# don't confuse math.exp() with math.pow()_

print('The square root of 6 is: {}'.format(math.sqrt(6)))

**_# csv_**

_# reading csv and tsv files without the csv module, using plain old IO/filestream methods, is fine...  
# with open("filename.txt", "r") as f:  
#     # when reading, I grab contents and get out of the open block  
#     contents = f.read() # whole file as one big string  
#     contents = f.readlines() # a list of line by line strings, WILL have "\n" at the end of each_

_# but using csv makes it a little easier..._

import csv

_# the reader() method is the only one I suggest knowing_  
contents = list(csv.reader(f)) _# csv.reader(f, delimiter="\t") for .tsv files... I like to recast the reader as a list._   
_# does one more step for us.._. _makes a list (since we recast it) of lists instead of the list of strings we get from readlines()_

_# [_

_# ['1', 'Flossie', 'Levey', 'flevey0@jimdo.com', '129.134.226.30'],_

_# ["2", "Bob"...],_

_# ..._

_# ]_  
print(contents)

_# other Standard Library modules that are great but not really needed for the exam:_

_# random_

_# string (yes, there's a string module beyond the standard str data type)_

_# datetime_

_# os_

_# regex_

_# webbrowser_

_# similarly, useful 3rd Party libraries that are good to know out there in the real world... but NOT NEEDED for exam:_

# pip install pytz # used to install package pytz

# import pytz

# imports the package

# beautiful soup - https://www.crummy.com/software/BeautifulSoup/ - parsing HTML and XML

# NumPy - http://www.numpy.org/ - scientific computing, multi-dimensional arrays and matrices

# pandas - http://pandas.pydata.org/ - data manipulation and analysis

# pillow - https://python-pillow.org/ - work with and manipulate images

# pyglet - http://www.pyglet.org/ - multimedia library for developing games

# pytz - http://pytz.sourceforge.net/ - works with time zone data