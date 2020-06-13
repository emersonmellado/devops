# Resources

[Introduction to Python](https://docs.python.org/3/reference/introduction.html)
[Python TOC](https://docs.python.org/3/contents.html)

# Python programming

- What is Python?
- Python Applications
- Install the environment

![Python 101](images/python/python_101.png)

# What is Python?

- Python is an **object-oriented**, **high-level**, **dynamically typed** and **interpreted** language
- **Platform** independent
- Easy to pickup and code
- Great as **scripting language**
- Plugable
- Full of **modules** that allows automation
- **bash** friendly

#### Example of modules
- boto (AWS)
- google-cloud-storage (GCP)
- gitapi
- ansible *(is written in python)*
- django *(framework for Web dev)*
- flask *(another framework for Web dev)*
- selenium *(extensible with python)*


# The language 

Python is an object-oriented programming language created in 1989. It is designed for rapid prototyping of complex applications.

It can be run in **Linux**, **MacOS**, **Windows** and more and is extensible to C or C++. 

Many large companies use the Python nowadays.

Python is widely used in Artificial Intelligence, Natural Language Generation, Neural Networks and other advanced fields of Computer Science. Python had deep focus on code readability & this class will teach you python from basics

- It is **free** and **simple** to learn. 
- Its primary features are that it is **high-level**, **dynamically typed** and **interpreted**. 

This makes debugging of errors easy and encourages the rapid development of application prototypes, marking itself as the language to code with.

It supports functional and structured programming methods as well as OOP.

It can be used as a scripting language or can be compiled to byte-code for building large applications.

It provides very high-level dynamic data types and supports dynamic type checking.

It supports automatic garbage collection.

It can be easily integrated with C, C++, COM, ActiveX, CORBA, and Java.

# Applications

- Web Development: Some of the most well-known frameworks are Django, Flask, Pyramid
- Game Development: PySoy which is a 3D game engine supporting Python 3, PyGame which provides functionality and a library for game development
- Machine Learning and Artificial Intelligence: libraries such as Pandas, Scikit-Learn, NumPy and so many more
- Data Science and Data Visualization
- Desktop GUI
- Web Scraping
- Audio and Video Applications
- And more….

# Installing python

We’ll be using **PyCharm** that is a cross-platform editor developed by JetBrains. Pycharm provides all the tools you need for productive Python development.
First of all, you have to install Python on your laptop

Visit the official website of Python http://www.python.org/downloads/ and choose the latest version for your OS.

Run the file you downloaded and follow the steps to install it. 


Programs and other executable files can be in many directories, so operating systems provide a search path that lists the directories that the OS searches for executables.

- Setting path at **Linux or Mac** In the bash shell type: 
    - `export PATH="$PATH:/usr/local/bin/python"`

- Setting path at **Windows** At the command prompt type: 
    - Assuming your Python installation is located at *C:\Python*
    - `path %path%;C:\Python`

### PyCharm

- To download PyCharm visit this [website](https://www.jetbrains.com/pycharm/download/) and Click the "DOWNLOAD" link under the Community Section

**Run the Setup** wizard to install PyCharm on your laptop
Once installation finished, you should receive a message screen that PyCharm is installed.

Now you can find PyCharm on your laptop to run it.

Once you see the introductory screen, you can select “Create New Project” 

#### You will need to select a location.

You can select the location where you want the project to be created. If you don’t want to change location than keep it as it is but at least change the name from “untitled” to something more meaningful, like “FirstProject”.

PyCharm should have found the Python interpreter you installed earlier.
- Next Click the **Create** Button.

So to start, as I said, we are going to think about a program that is so simple, it does not make sense to write many lines of code.

Go up to the “File” menu and select “New”. Next, select “Python File”. Now type the name of the file you want (Here we give “hello-world”) and hit “OK”.

Write on the file (and click on Run after saving!):

- `print (“Hello World!”)`


# Your first python program

There is another way to run the program, from outside your IDE.
Let’s say that our script was saved as `hello-world.py`
From the bash or command line, we can type

- `python hello-world.py`

And the result will be

> Hello World!


## Inside the program

The line `print (”Hello World”) `

This is an instruction that tells the Python interpreter to display the text that is within parentheses.

We see that text strings are enclosed in double quotation marks "".

You can print multiple lines or use modifiers to the function print:
```python
print ("Welcome to class!")
print (8 * "\n")
print ("Welcome to class!")
```

---

# Python components
- Comments
- Identifiers and Reserved Words
- Variables and constants
- Operators
- Literals
- Expressions
- Using the console and keyboard

It is necessary to begin to know the rules of the language in which we’ll describe the components of the program.

**There are rules:**
- [**Lexicons**](https://docs.python.org/3/reference/lexical_analysis.html) for writing correct words
- **Syntax** for writing valid sentences with these words
- **Semantics** which allow us to give an interpretation to the "sentences" that we write in this language.


> About **coding**:
- Writing a program equals **to coding**
- Source code can be located in **one** or **more** files
- Every programming language has their own **rules**

## Comments

The comments are ignored by the compiler, they only serve so that we can write annotations that are useful both for us and for people who read the source code.

```python
# Single Line comment    

""" 
Multiline comment 
Another commented line
"""
```

## Identifiers

An identifier is a symbolic name that we give to a program element (**variables**, **objects**, **instances**, etc), which we use to refer to it and use it throughout the program.

### The basic rules for declaring valid identifiers are: 
- The identifier name **must** begin with a letter or a "_" and then an arbitrary sequence of letters, numbers or a "_".
- Punctuation characters such as @, $, and % within identifiers are **not** allowed. 
- Python is a case sensitive programming language. Thus, **Manpower** and **manpower** are two different identifiers in Python.

### Naming conventions for Python identifiers:

- **Class names** start with an **uppercase letter**. All other identifiers start with a lowercase letter.
- Encapsulation:
    - Starting an identifier with a *single leading underscore* indicates that the identifier is **private**
    - Starting an identifier with *two leading underscores* indicates a **strongly private** identifier.
- If the identifier also **ends** with *two trailing underscores*, the identifier is a **language-defined** special name.

### Reserved words

Reserved word is all sequence of characters that is predefined in order to specify what we want to do within the program. 
- Specific Instructions
    - if, while, for, etc.
- Declarations
    - def, class, etc.
- Flow Management
    - continue, break, return, etc.
- Python **does not** allow us to redefine its meaning and can not create new reserved words.


## Lines & Indentation 

Python provides no braces to indicate blocks of code for class and function definitions or flow control. Blocks of code are denoted by line indentation, which is rigidly enforced.

The number of spaces in the indentation is variable, but all statements within the block must be indented the same amount.

```python
if True:
   print("True")
else:
   print("False")
```

Statements in Python typically end with a new line. Python does, however, allow the use of the line continuation character (\) to denote that the line should continue.

```python
total = item_one + \
        item_two + \
        item_three
```

Python accepts **single** ('), **double** (") and **triple** (''' or """) quotes to denote string literals, as long as the **same type** of quote starts and ends the string. The triple quotes are used to span the string across multiple lines.

```python
word = 'word'
sentence = "This is a sentence."
paragraph = """This is a paragraph. It is
made up of multiple lines and sentences."""
```

## Variables and constants

It is a memory space reserved for storing data that will be used later.

Based on the data type of a variable, the **interpreter** allocates memory and decides what can be stored in the **reserved memory**. Therefore, by assigning different data types to variables, you can store integers, decimals or characters in these variables.

According to their mutability
- Variables
- Constants

3 properties:
- An identifier
- Store data (a value)
- Has a type (which we don’t declare, python **infers** it)

### Variables declaration

It is done in the following way:
- `VAR_NAME = EXPR`

Where:
- **VAR_NAME**: name that identifies the variable
- **EXPR**: Initial value

Examples:

```python
counter = 100        # An integer assignment
miles   = 1000.0     # A floating point
name    = "John"     # A string

print(counter)
print(miles)
print(name)
```

The data stored in memory can be of many types. Python has various standard data types that are used to define the operations possible on them and the storage method for each of them.

Python has five standard data types:
- Numbers (int, long, float, complex)
- String
- List
- Tuple
- Dictionary

Example:

```python
counter = 100        # An integer assignment
miles   = 1000.0     # A floating point
name    = "John"     # A string

print(type(counter))
print(type(miles))
print(type(name))
```
### Constants declaration

Similar to the declaration of a variable but with the name in **UPPERCASE**
It tells the compiler that the value can not be changed. 

Example: 

`PI = 3.14159`

## Operators

Operators are special symbols that perform specific operations with one, two or three operands, and then return a result. Operators are used to construct expressions.

### Examples:

- Arithmetic: **+**, **-**, **\***, **/**, **%**
- Logic: **and** or **&&**, **or**, **||**, **!**
- Relational: **<**, **<=**, **>**, **>=**, **==**, **!=**
- Assignment: **=**
- Bitwise: **|**, **^**, **~**
- Membership: **in**, **not in**
- Identity: **==**, **is**, **is not**

### Arithmetic Operators
![Arithmetic Operators](images/python/arithmetic_operators.png)

### Logic Operators
![Logic Operators](images/python/logic_operators.png)

### Relational Operators
![Relational Operators](images/python/relational_operators.png)

### Assignment Operators
![Assignment Operators](images/python/assignment_operators.png)

### Operators precedence
From **Higher Priority** to **Lower Priority**

![Operators precedence](images/python/operators_precedence.png)

## Literals

A literal is a succinct and easily visible way to write a value. Literals represent the possible choices in primitive types for that language. Some of the choices of types of literals are often integers, floating point, Booleans and character strings. Python support the following literals:

#### Supported literals
```
String literals   ::   "halo" , '12345'
Int literals   ::   0,1,2,-1,-2
Long literals   ::   89675L
Float literals   ::   3.14
Complex literals   ::   12j
Boolean literals   ::   True or False
Special literals   ::   None
Unicode literals   ::   u"hello"
List literals   ::   [], [5,6,7]
Tuple literals   ::   (), (9,),(8,9,0)
Dict literals   ::   {}, {'x':1}
Set literals   ::   {8,9,10}
```
**Examples:** *(Identify the types of each one?)*

```python 
result = True; 
cUpper= 'C'; 
b = 100; 
s = 10000; 
i = 100000;
```

## Expressions

Expressions are a combination Operands with Operators that is performed according to the language syntax, which evaluates and returns a single value.

- Operands are the elements to which operations are applied, they can be: variables, literals, constants, invocations to methods that return a value or even subexpressions
- Operators are the elements that carry a specific operation on the operands.

Expressions are part of a sentence.

Two categories:
- Simple Expressions: one operand
- Composed Expressions: several operands combined with operators

Operators combine operands of a certain type


### Simple Expressions
In **bold** we highlight the expressions

- res = **0** # assign 0 to res
- isBroken = **False** # assign false to isBroken.
- character = **'C'** # assign letter 'C' to character.
- res = **varA** # assign the value in varA to res

### Composed Expressions
In **bold** we highlight the expressions

- isBroken = **engineNotworking** or **gearboxNotWorking** # assign isBroken the result of the logic OR that combines other two operands.
- res = **5 + varA** # assign to res the result of the sum between literal 5 and varA.
- res = **(3 * 5) + varA**
- res = **5 + (6 * 5)  / 3 + (66 – 16) * 10**


### Console or (REPL - Read–Eval–Print Loop)

To enter python REPL open a terminal and type: `python3`, hit enter.

You should see something like this, pay attention to the **>>>** symbol, this is where we will enter commands and they will be parsed for now.

```
Python 3.8.2 (default, Apr 27 2020, 15:53:34) 
[GCC 9.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

Displaying text in the console is relatively simpler and Python already has methods for this. 
> The fastest way is by doing this
- print("Text to show")


### Read and print
For Python 3, let’s see an example of how to read:
```python
n = input('Choose a number')
print ('Number %s \n' % (n))
```

Showing text in the console is very simple in Python, and to read from keyboard, is also pretty simple

For Python 2, reading from keyboard changes a little bit:
```python
raw_input('Choose a number')
```

**Note:** remember that this can raise an Exception if the input is not a number. We’ll see how to handle exceptions later



### Flow Controls



### Conditions (If statements)

As we studied in Conditional Logic, applications are written with conditions in mind, so let's see how that works.

The structure of a condition is the following:

```python
if CONDITION:
    # Condition is True
else:
    # Condition is False
```

Example:

```python
random_number = 101
if ( random_number == 100 ): 
    print("Value of the random number is equal to 100")
else:
    print("Value of the random number is NOT equal to 100")
```

We can start to mix and match things:

```python
random_number = input('Input a number: ')
if ( random_number == 100 ): 
    print("Value of the random number is equal to 100")
else:
    print("Value of the random number is NOT equal to 100")
```

We can also chain multiple conditions at once:

```python
random_number = int(input("Please enter an integer: "))
if random_number < 0:
    print('Negative')
elif random_number == 0:
    print('Zero')
elif random_number == 1:
    print('Single')
else:
     print('Higher value')

print("The value of random_number is: ", random_number)
```

### for Statements

```python
countries = ["Canada", "US", "Australia", "Finland", "Nigeria"]
for country in countries:
    print(country, len(country))
```

We can also use range()

```python
for i in range(5):
    print(i)
```

Mixing it all together:

```python
song = ['Mary', 'had', 'a', 'little', 'lamb']
for word in range(len(song)):
    print(word, song[word])
```

We can start to think about some more interesting things, what about a chaining sum?

```python
print(sum(range(4))) # 0 + 1 + 2 + 3
```

Let's check the python [oficial documentation](https://docs.python.org/3/tutorial/controlflow.html) for more details and you can keep going on your own :)