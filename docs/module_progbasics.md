# Programming Basics questions

## Computer science

### Data structures


#### What is the purpose of a list (array in some programming languages) data structure? Name some methods of it!

A list is a type of data structure which holds usually more elements (data types, other data structures), in most of the cases related in a certain way. The lists elements are written inside square brackets and separated by comma. Each element has an index (starting from 0) which is used to access the element from outside the list. With the help of lists, we can manipulate more elements in the same time easily. Lists are mutable, which means that we can modify them. 

#### What is the difference between a list/array and a set?

The visible difference is that the list elements stand between brackets, while the set elements stand within curly braces. The elements from set don’t have corresponding indexes and they are unordered. Another important difference is that sets hold only unique elements. Sets have a lot of different methods (compared to lists) used to manipulate elements.

#### What is the purpose and methods of a dictionary/map data structure?

Dictionaries are very useful when we want to create a library of items, each composed from keys and values. The elements from a dictionary are placed within curly braces. An important detail is that the keys should be immutable data types or data structures, while the values can be of any type. The dictionary methods are in general similar with the ones from lists, excepting the methods used to handle the keys and values combination.


### Algorithms

#### Fibonacci sequences. Write a method (or pseudo code), that generates the Fibonacci sequences.

	def fibonacci(n):
		fib_list = [0, 1]
		i = 2
		while i <= n:
			fib_list.append(fib_list[i - 1] + fib_list[i - 2])
			i += 1
		return fib_list


#### How do you find a max value in a list/array if you can’t use any built-in functions?

	def find_max(nums_list):
		max_num = nums_list[0]
		for num in nums_list:
			if num > max_num:
				max_num = num
		return max_num

#### How do you find the average of values in a list/array if you can’t use any built-in functions?

	def find_avg(nums_list):
		nums_sum = 0
		for num in nums_list:
			nums_sum += num
		return nums_sum / len(nums_list)

	
	
#### What do we call an *in-place* sort?

* An in-place sort method mutates the list on which the `sort()` method was used, without returning a new modified list (like `sorted()` is doing).

#### Explain an algorithm which sorts a list!

	def bubble_sort(list)
		# we assign the length of the list to variable n
		n = len(list)
		
		# we iterate over all the elements from the list
		for i in range(n):
			for j in range(n – i – 1):
				# if the current element is bigger than the next
				if list[j] > list[j + 1]:
					# we swap them
					list [j], list[j + 1] = list[j + 1], list[j]
		
		return list

### Programming paradigms - procedural

#### What is the call stack?

* The call stack is a stack data structure that stores information about the active called functions. A call stack is used for several related purposes, but the main reason for having one is to keep track of the point to which each active subroutine should return control when it finishes execution.



#### What is “Stack overflow”?


“Stack overflow” is a website on which people request help regarding all kind of problems they encounter while coding. It’s a very well organized website, accessed by many people and where you can find useful explanations, solutions or advices for similar problems you face during your coding work. Another good aspect of “Stack overflow” is that people who request help on this site are required to formulate their inquiries in a specific way, which will facilitate the process of answering. 



#### What are the main parts of a function?

The first part of the function is the line on which its defined, using the “def” keyword followed by a space, the desired name for the function, closed rounded brackets and a colon (punctuation sign). Between the closed rounded brackets there may or not may be the parameters, which are used inside the function statements.
Follows the function statements, which is the code that has to be executed whenever a function is called. This part of the function is indented. 
It’s a good and recommended practice to add before the function statements a docstring, in which it’s explained what the function does. This docstring is used when requesting info about the function inside the python shell. 
Usually there is also a return statement which returns a value from the function


### Programming languages - Python  

#### How do you use a dictionary in Python?

A dictionary is composed of items which contain a key and a corresponding value. You can access the values for a certain key by writing the dictionary name followed by the key name in brackets. It’s a frequent procedure to add or remove items to dictionaries. There are more ways to do that, either by assigning a value to a non-existing key from the dictionary or using the .update() method and passing as argument the whole item. You can also remove items from the dictionary using the pop() method. Another frequent use of the dictionaries is to get a list of all the keys or all the values from the dictionary.


#### What does it mean that an object is immutable in Python?

An immutable object can’t be modified or updated after it’s created. Examples of immutable objects are strings, integers, tuples.The advantage of the mutable objects is that they are quicker to access (use tuples over lists when the items don’t have to be modified)


#### What is conditional expression in Python?

Conditional expression is a decision making within a script based on a certain condition. The most basic key of conditionally expression is “if”. An if statement runs a piece of code if a condition is met. An if statement is followed by an expression. Then, below it’s one or more indented statements. If the expression evaluates to True, all the statements within the if scope will run. If the expression evaluates to False, the statements will be skipped.


#### What are different types of arguments in Python?

In python there are 3 types of arguments:

 1. **Default arguments**: which are set directly in the function declaration.
 1. **Key arguments**: variables declared in the function declaration between the round brackets. They are used inside the functions

 1. **Args** and **kwargs** arguments: used to pass a list of arguments



#### What is variable shadowing? (context: variable scope)

Shadowing is a concept that refers to the situation when we give the same name to variables from different scopes.


#### What can happen if you try to delete/drop/add an item from a List, while you are iterating over it in Python?

If we modify the length of a list while iterating over it, there is a high risk to receive an index error. As the iteration starts, the program expects a certain number of items, but if we modify the list during the iteration, an indexes inconsistency might occur.


#### What is the "golden rule" of variable scoping in Python (context: LEGB)? What is the lifetime of variables?


A variable can’t be accessed outside its scope. The lifetime of the variable starts when it is created and ends in the same time when the code that created stops its execution.


#### If you need to access the iterator variable after a for loop, how would you do it in Python?

* We can use Python’s `iter()` method, which returns an object that can be iterated one element at a time. The `next()` in-built method is used to iterate over the elements from the object, one by one. After all the values from the iterated object were returned, if we try again the `next()` method, a StopIteration exception will occur.


#### What type of elements can a list contain in Python?

A list can contain data types (integers, strings, booleans, None) or other data structures (lists, dictionaries, sets, tuples)

#### What is slice operator in Python and how to use?

The slice operator in Python is used to create a slicing object, used on an iterator to extract a part of that iterator.  I never used it because I prefer the direct slicing method with syntatic form a[4:5]. Slice operator can be useful when you want to slice more iterators using the same pattern.

#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do?

You can use + * and – operators on lists. + operator is used to add the items from more lists, * operator is used to multiply the elements from a list


#### What is the purpose of the in and not in membership operators in Python?

With the **in** operator you can check if an element is found in an iterable or not. The statement using **in** returns True if the element is found and False if it’s not found. The **not in** operator is similar to **in**, but returns True if an element is not found in an iterator and False if the element it’s not found.


#### What does the + operator mean when used with strings in Python?


The **+** can be used to concatenate strings.


#### Explain f strings in Python?

The **f strings** are used to format strings in an elegant way, offering the possibility to add pieces of code(variables, lists, statements) inside the strings.  The Python code inside **f strings** has to be written between curly braces. The main advantages of the **f strings** compared to its alternatives are: more readable, less prone to error and even faster.


#### Name 4 iterable types in Python!

String, lists, dictionaries and sets. 


#### What is the difference between list/set/dictionary comprehension and a generator expression in Python?


Comprehensions are an elegant way to create lists. Generator expressions are used to create generator objects, which don’t occupy memory space as the list do. The items from the generator objects can be access using iteration.


#### Does the order of the function definitions matter in Python? Why?


The order of function definition doesn’t matter in general. The only problem that you have to avoid is to call a function before it is defined. 


#### What does unpacking mean in Python?


Unpacking it’s used most frequently to pass all the elements from a list as arguments for a function.


#### What happens when you try to assign the result of a function which has no return statement to a variable in Python?

The value **None** is assigned to the variable.



## Software engineering

### Debugging

#### What techniques can you use while debugging a program in Python?
1. Using the `print()` function is the “at hand” technique for debugging. Use `print()` on a  certain piece of your code (variable, data structure, statement) and compare the result printed on the console with what is the result you were expecting. 

1.Logging module. It’s similar with the print method, but it uses a logger object and you can print the logging results to the console, record them in a file or share them. One feature of the logging module is that you can set logging levels, starting from NOTSET (when all the messages are logged) up to CRITICAL (logs only the problems with the highest priority).

1. pdb – The command line debugger. I have never used it.

#### What does step over, step into and step out mean while using the debugger?

* _step into_: A function is about to be invoked and you want to debug into the code of that function, so the next step is to go into that function and continue debugging step-by-step.
* _step over_: A function is about to be invoked, but you’re not interested in debugging this particular invocation, so you want the debugger to execute that function completely as one entire step.
* _step out_: You’re done debugging this function step-by-step and you just want the debugger to run the entire function until it returns as one entire step.

#### How can you start to debug a program from a certain line using the debugger?

* _line breakpoint_: If the execution reaches a particular line of code, you want the debugger to temporarily pause execution there so you can decide what to do.

### Version control

#### What are the advantages of using a version control system?

* Facilitates the collaboration between the members of a team of programmers which work on the same project

* Records copies of different versions of the projects, which can be accessed with ease whenever it’s needed

* The commits (if used properly) organize the projects very efficiently, keeping track of all the changes, the collaborator who did each change and with suggestive subjects and description can explain in details what modifications were done to the projects and why.

* Branches are another useful feature of the version control systems, allowing the collaborators to work independently of the main project, not affecting it and only apply the changes whenever it’s consider that the features added in the new branch are ready to be included in the project.

#### What is the difference between the working directory, the staging area and the repository in git?

The working directory is the local directory on your computer. When the files are found in the working directory you can modify them as you wish, it won’t affect the project present in the github repository. 
In the staging are git starts to track your changes. Git will know at this moment that some of the files from the project have been modified. 
The repository is where all the changes and commits are recorded. 

#### What are remote repositories in git?

* Remote repositories are versions of  projects, which are recorded on a Git repository hosting service, like GitHub. The remote repositories facilitate the collaboration between more people involved in a project. 

#### Why does a merge conflict occur?

* Merge conflicts occur when competing changes are made to the same line of a file, or when one person edits a file and another person deletes the same file. During a merge conflict, Git needs your help to decide which changes to incorporate in the final merge.


#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?

1. Open a terminal window and access the folder in which the local repository is present.
	
1. Stage the file for commit to your local repository.
	- `git add <file name>`
	Adds the file to your local repository and stages it for commit.
1. Commit the file that you’ve staged in your local repository.
	- `git commit -m “Add new file to remote repository”`
	Commits the tracked changes and prepares them to be pushed to a remote repository 
1. Push the changes from your local repository to the remote repository from GitHub.
	- `git push origin <your-branch>`
	Pushes the changes made in your local repository up to the remote repository.


#### What does it mean atomic commits and descriptive commit messages?

* The atomic commits refers to the principle that your commits should be made for a single feature, fix or improvement. This way, you can manage better the versions of your project and return, when needed, to the precise desired moment, withing your work history. 
* Descriptive commits are used to explain what was the purpose of that specific modification and why it was needed. 


#### What’s the difference between git and GitHub?

* Git is a distributed version control system, created by Linus Torvalds, that lets you manage and keep track of your source code history.

* GitHub is a cloud-based Git repository hosting service. GitHub makes a lot easier for individuals and teams to use Git for version control and collaboration

## Software design

### Clean code

#### What does clean code mean?

* Code is clean if it can be understood easily – by everyone on the team. Clean code can be read and enhanced by a developer other than its original author. With understandability comes readability, changeability, extensibility and maintainability. Or how Martin Fowler (a British software engineer) said it: “Any fool can write code that a computer can understand. Good programmers write code that humans can understand”.

	

#### What steps do we usually do during a clean code refactoring?

* Refactoring tips

	- Read through the code and understand what it is doing.
	- Summarize in one sentence the purpose of the script.
	- Run the code to see what is the end result.
	- The code should keep runnable and have the same results after you finish the refactoring.
	- Run the code frequently to see if the expected results are maintained.

* Refactoring process
	- Remove the 3 C’s, clutter, complexity and cleverness. 
		- Clutter is anything in your code that does not add value. Unused pieces of code, unnecessary comments.
		- Some examples of complexity: bad naming, long methods, deep conditionals, improper variable scopes(global, local)
		- Cleverness: If it’s simple and elegant, you wouldn’t refer to it as ‘clever’
	- Remove the 3 D’s: duplication, duplication, duplication
		- this can be applied by extracting the duplicated code parts into functions

	
	

### Error handling

#### What is exception handling?

* An exception can be defined as an abnormal condition in a program resulting in disruption in the flow of the program. Whenever an exception occurs, the program halts the execution, and thus the further code is not executed. 
* Instead of letting the exception crash our program, we can intercept it and do something about it to allow the program to continue.


#### What are the basics of exception handling in Python?

* If the python program contains suspicious code that may throw an exception, we must place that code in the try block. The try block must be followed with the except statement which contains a block of code that will be executed if there is some exception in the try block.


#### In which case should we catch an exception? Why?

* We should catch an exception when we want to protect small blocks of code against specific errors. We catch exceptions in order to take measures which will avoid the program crashing or displaying unwanted results.

#### What can/should we do with an exception in the ‘except’ block?

* In the `except` block we should write code that the program will execute when there is an exception. 

#### What does the else and finally statement do in a try-except block in Python?

* The else statement will be executed only if the try clause doesn’t raise an exception.

* The finally block will always be executed, no matter if the try block raises an error or not. 


## Software Development Methodologies

#### What is the main goal of a retrospective meeting?

* The purpose of the retrospective meeting is for the development team to discuss what went well during the just completed development cycle and what did not. Then, the development team must think of actions that they can take in order to improve the development process.

## Programming environment

### Unix

#### What is UNIX and what is Linux?

* UNIX is an operating system that was born in the late 1960s, when AT&T bell Labs released an operating system called Unix written in C, which allows quicker modification, acceptance, and portability. 

* Linux is the best-known and most-used open source operating system. As an operating system, Linux is software that sits underneath all of the other software on a computer, receiving request from those programs and relaying these requests to the computer’s hardware.


#### What do we call the shell in Linux?

* The shell in Linux is the command line interpreter, that executes other programs. It provides a computer user an interface to the Linux system, so that the user can run different commands or utilities/tools with some input data.

#### What does root means in a Linux environment?

* Root is the user name or account that by default has access to all commands and files on a Linux or other UNIX-like operating system. 


#### How do you access your personal files in Linux?

* In Linux, the personal data is stored in /home/username folder.

#### How can you install an application in Linux?
* Open a Terminal window and run the following command:

	`sudo apt install <name_of_the_application>`

#### What is package management in Linux, what are repositories?

* Package management systems allows users to install, update, remove and get information about software installed.

* Repositories are storage locations where the packages are downloaded from

#### How do you navigate in the filesystem with the command line?

	pwd : prints the current working directory
	ls : displays the content of the current working directory
	cd followed by path : used to access a certain folder
	cd.. : used to go up a level in your directories tree


#### What does the following commands do: mkdir, rm, cat, cp, touch?

* `mkdir` - creates a new folder
* `rm` - used to delete a file specified on the command line
* `cat` - used to display the content of a text file
* `cp` - used to make a copy of a file or group of files
* `touch` - creates a new file


#### How can you look up what does a command do in Linux if you have no internet connection?

* You can use the following commands: `--help` or `man`


#### What does the following commands do: head, tail, more, less?

* `head` - outputs the first 10 lines of a file.
* `tail` - outputs the last 10 lines of a file.
* `more` - output the contents of a file, one screen at a time.
* `less` - similar with `more`, but has more advanced features and allows you to navigate forward and backward through the file.

#### How do you download a file from internet using the terminal?

* `wget <link-to-file>`
