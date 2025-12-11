# Python Week 8 Assessed Workshop

---

#### Note on workshop attendance...

For advanced workshops completion of the activities must be under invigilated conditions.

Please make sure you sign the workshop attendance sheet. 

Code should autosave, but you must still commit your work at the end of the workshop before leaving.

---

**Do all coding in CodeSpaces only** 

You may use the following cheat sheets if you need to look up any Python commands.

https://github.com/phil-lewis-exe/PythonCheatSheets

**This week you should not use any other websites to help you code.**

**You must ask if you need to use a website to translate the task questions**

**Mobile phones may not be used in class**

---

## TASKS

# Workshop 8b

This workshop has three sections.  **Core students should stop after exercise 2a.**

The **average 2:1** student is expected to complete **most of parts 1 and 2** within the time allocated. 

It is expected that the only the **few fastest high 1st class** students in the class will complete **all of the tasks** in the time allocated.

The weighting for each section in the advanced workshops is approximately: part 1 (40%) part 2 (35%) part 3 (25%), but may be moderated to reflect difficulty of different workshops.

---

### part1a.py

Look at the following example that defines
variable: `var1` then displays info about 
the type of object `var1` is. 

```python
var1 = "hello"
print("var1: str")
```

Edit the print lines below so they display 
the right object types for `var2` and `var3`  
following the format from the example above.

choose from:
int float bool str list dict tuple

```python
var2 = "42.5"
var3 = [ 1, 'one', 2, 'two' ]

print("var2: ")
print("var3: ")
```

---

### part1b.py

Write code to do the calculation below and 
store the result as variable: `z`

your code should make use of the variable `x`
as defined below so it would work if a 
different value is used 


               1
 z =  x + -------
             x + 2 


test your code with: `print(z)`

```python
x = 2
```

add your code below

---

### part1c.py

Create a dictionary with name: `mydict`
that stores the following data

key        value
"name"     "Einstein"
"born"     1879
"died"     1955


test your code using: `print(mydict)`

add code below

---

### part1d.py

The following code defines a list
that stores individual letters

```python
word = [ "H", "e", "l", "l", "o" ]
```

write a line of code that adds the value: "!"
to the end of `word`

your code should work even if `word` stored a different number of entries.

test your code has worked using: `print(word)`

add code below

---

### part1e.py

Write a function named: `get_last_letter`
that takes a single argument: `mystr`
storing a string

The function should return the final letter in the string

e.g. 
if we pass in the value 'apple' the
value returned should be: 'e'


Add code to demonstrate the function
using argument: hello
storing the output in variable: `last_letter`

test your code has worked using: `print(last_letter)`

---

### part1f.py

The following code defines a list
storing a set of strings

```python
numbers = [ "one", "two", "three", "stop", "four", "five", "six" ]
```

Write code to loop over the strings 
in the list and print out the length
of each string (one per line)
 with expected output:

  3
  3
  5
  4
  4
  3

add code below

---

### part1g.py

A program is designed to take user input 
of a single character `y` or `n`
to check if a user wants to continue like:

```python
print('Enter your choice: y/n')
user_input = input('> ')
```

Add code below that will print a
corresponding message 
depending on the input made

"User selected yes"
"User selected no"
"User input invalid"


add code below

---

### part2a.py

A student is writing code to run a times-table quiz
that will ask questions like: What is 5x6?
(for which the answer should be 30)

Write a function named: `make_times_table`

This should take two arguments: `z` and `max_val`

    `z`        -  the times table to generate
    `max_val` -  an integer 0-9 for the maximum value 

it should return a list of the questions e.g.

for `z` = 4 and `max_val` = 6

the function should return

[ "0x4", "1x4", "2x4", "3x4", "4x4", "5x4", "6x4" ]

In addition the function should use default value of 9 for `max_val`

Add lines of code demonstrating how to call the function

i. with `z` set to 4 and `max_val` set to 6
ii. with `z` set to 5 and `max_val` left so its default value is used

---

### part2b.py

The previous question created a list of questions like

```python
qlist = [ "0x6", "1x6", "2x6", "3x6", "4x6", "5x6" ]
```

Use shuffle function from the random module
so that you can use code like below to 
shuffle the list contents using code like

```python
print(qlist) # before
random.shuffle(qlist)
print(qlist) # after
```

Then code that can loop over the list 
and create a text file storing the questions
(one question per line)
in a file named "questions.txt"

write code below

---

### part2c.py

The questions for the quiz are of form:

```python
q_str = "5x4"
```

Each question contains a 3 character string like: "axb"
where `a` and `b` are single digit numbers

Write a function called: `get_answer()`

that takes single argument: `q_str`
which is a 3 character string of form "axb"

it should return the correct answer for the question (as a integer).

Your code will need to do the following:

- obtain the first number from the string and convert it to an integer
- obtain the second number from the string and convert it to an integer
- calculate and return the correct result

Your code should also handle the case when 
an invalid question is provided by returning
a None value i.e. 

    return None

This should occur when either:

- provided string is not length 3
- middle character of string is not 'x'
- first / last character are not valid numbers 
 
in the final case your code should ensure that
any exceptions thrown by the integer conversion 
steps are handled correctly so the code returns 
without raising an exception

Check your function works correctly by showing its output
with each of the following input arguments: 
"5x4"  "99x99"  "3+3" "?x8"

---

### part3a.py

Write code that can ask a student to enter 
a custom set of times table questions

You should display a message:

"Enter questions (type `q` when done)"

Then allow the student to type in their questions one by one.

After each entry valid questions should be stored
and the appropriate message from below displayed:

    "question stored" or
    "question invalid"
 
(valid questions are 3 characters of form "axb" or "aXb"
 where `a` and `b` are digits in range 0 to 9)

Once the student types `q` to indicate they have finished
all valid questions should be saved in a file named
"custom_questions.txt"

---

### part3b.py

Write code that can load in questions
from the file: 'all_questions.txt'

It should load these into a list of questions named: `q_list`
and then double the number of questions in the list
by adding flipped entries

e.g. for question "3x5"
the flipped question is "5x3" 

It should then shuffle this list, and use them to run a quiz
 
This should start with the following message:
 
"Welcome to the Quiz" 
 
and display each question, then giving students a prompt using code

```python
ans = input("> ")
```

If a student gets a question wrong they should be given a message "try again"
and must continue to enter their answer until they get the answer correct
enter the correct answer.

Your quiz should calculate the time taken to answer the questions

This can be done by using the `time.time()` from the time module
using the commands below in the appropriate place

```python
start_time = time.time()
end_time = time.time()
time_taken = round(end_time - start_time)  
```

When the student completes the quiz they should recieve a message
showing the time taken:
 
 You took ___ seconds!
 
---

### Submitting your work

Run the following lines in the terminal to stage, commit and push your code back to your GitHub repository:

```
git add .
git commit -m "completed 11b"
git push
```

To check your work has been saved you can run the line of code below in the terminal to get the web address of the repository in GitHub. Goto the repository and check the completed code files are stored.

```
git config --get remote.origin.url
```
