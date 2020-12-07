# OOP questions

## Software design

### Error handling

#### What does 'fail fast' mean in terms of exception handling? Why is it a good practice?

The fail fast principle stands for stopping the current operation as soon as any unexpected operation occurs.
Adhering to this principle generally results in a more stable solution.

##### Why Fail-Fast?

Fail-fast makes bugs and failures appear sooner, thus:

+ Bugs are earlier to detect, easier to reproduce and faster to fix.

+ It's faster to stabilize softwares.

+ Fewer bugs and defects will go into prodduction, thus leading to higher-quality ad more production-ready software.

+ The cost of failures and bugs are reduced.
 
##### Application of Fail-Fast

Fail-fast is the principle behind many Agile practices:

+ Test-driven development: Writing tests to cover all the cases in which it would fail and all the requirements
it has to meet, before even implementing it.

+ Continuous integration: An agile practice in software development, where developers are required to
integrate their current works into shared repository/branch several times a day. Each integration is
verified by automated builds, thus helping team to find and fix problems early.


## Computer Science

### Data structures

#### How to find the middle element of singly linked list in O(n)?
#### Given an array of integers going from 1 to 100 (both inclusive) there is a duplicated entry. How to find it?
#### What is a linked list? How to find if a linked list has a loop?
#### What is the Big O time complexity of the common operations in an ArrayList, LinkedList, HashMap? And of a bubble sort, quicksort, finding items in a Binary Search tree?
#### How does HashMap work?
#### Why is it important for keys in a map to have an immutable type? (Consider String for example.)

String, Integer and other wrapper classes are natural candidates for HashMap key. String is most frequently used key
because String is immutable, final and overrides equals() and hashCode() methods. Other wrapper classes also
share similar properties. 

Immutability is required in order to prevent changes on fields used to calculate hashCode because
if the key object returns different hashCode during insertion and retrieval, then it won't be possible to get the object from the HashMap.
Immutability is required as it offers other advantages, like thread-safety; if you can keep your hashCode the same
by only making certains fields final, then you go for that as well. Since equals() and hashCode() method are used during
retrieval of value object from HashMap, it's important that the key object correctly overrides these methods.

### Other

#### What is a garbage collector, in a nutshell?

**Garbage Collection** in Java is a process by which the programs perform memory management automatically.
The Garbage Collector(GC) finds the unused objects and deletes them to reclaim the memory. In Java, dynamic memory
allocation of objects is achieved using the new operator that uses some memory and the memory remains allocated until there
are references for the use of the object.

When there are no references to an object, it is assumed to be no longer needed, and the memory occupied by the
object can be reclaimed. There is no explicit need to destroy an object as Java handles the de-allocation automatically.

## Programming paradigms

### Procedural

#### What is casting? What is the difference between up vs downcasting?

Casting is taking and Object of one particular type and "turning it into" another Object type.
Up-casting is casting to a supertype, while downcasting is casting to a subtype. Upcasting and downcasting gives us
advantages, like Polymorphipsm or grouping by different objects. We can treat an object of a child class type to be as an object
of its parent class type. This is called upcasting. Now, anytime an object of parent class type is type cast into a child
class type, it is called downcast.


#### Which order should we catch the exceptions? Why?

When catching exceptions, you want to always catch the most specific first and then the most generic. If the first
catch matches the exception, it executes, if it doesn't, the next one is tried ad so on until one is matched or none are.


### Object-oriented

#### What is a class?

A class is a blueprint to create an object.

#### What is an object?

An object is an instance of a class, each object has its own set of properties.

#### What is a constructor?

Constructors are special methods in Java/C# that have the same name as the class. Everytime we create an object, a default constructor is created.

#### Do we require parameter for constructors?

We can create constructors with or without parameters. The default constructor doesn't have any parameters, so no, it's not required to use parameters for constructors.

#### What is an interface?

An interface is just a class, the difference is that it has only method signatures, so no code written in the method body. Using interface-based design concepts provides loose coupling, component-based programming, easier maintainability, makes your code more scalable and makes code reuse much more accessible because the implementations is separated from the interface.


#### What are access modifiers?

Access modifiers are keywords used to specify the declared accessibility of a member or a type. There are 4 access modifiers in Java: public, private, protected and default.


#### What is data hiding?

Data hiding is a software development technique specifically used in OPP to hide internal object details (data members). Data hiding ensures exclusive data access to class members and protects object integrity by preventing unintended or intended changes.
Data hiding also reduces system complexity for increased robustness by limiting the interdependencies between software components. Data hiding is also known as data encapsulation or information hiding.

#### Can a static method use non-static members?

Yes, non-static members are allowed in a static method.


#### What is the difference between hiding a static method and overriding an instance method?

Hiding a static method or any method uses the OOPs principle of Encapsulation compared to overriding, an instance method that uses OOPs prince of Polymorphism.

#### Define the following terms: Instantiation, Attribute, Method

Instantiation: the process of creating a new object; Attribute: it's another word for field, member. An object can have multiple attributes of different types, such as int, float, boolean, String and so on. ; Method: is a block of code which onl runs when it is called. Methods are used to perform certain actions and they are also known as functions.

#### Could we access a static variable (or method) from a non-static method? Why?

Yes, a non-static method can acess a static variable or call a static method in Java. There is no problem with that because of static members i.e. both static variable and static methods belong to a class and can be called from anywhere, depending upon their access modifiers. 

#### Could we access a non-static variable (or method) from a static method? Why?

No, because that non-static variable belongs to an instance. We need to create an object to use those fields and methods.

#### How many instances you have of a static variable of a given class?

Only one.

#### Why is it not a good practice to write a lot of static methods?

Static methods cause tight coupling, which is a violation of good Object Oriented Design.  

#### What are the features of static attributes and static methods of a class? What are the benefits, when to use them?
#### What is the ‘this’ reference?

Using 'this' keyword you reference the object of the current class.

#### What are base class, subclass and superclass?

When we use inheritance, a subclass extends superclass. This means the subclass has all properties of a superclass, such as methods, fields, inner classes or block of codes. A base class is a class that will be extended and is only used as a base for all clases to receive its properties.

#### Draw an object oriented family (as entities, with relations) on the whiteboard.

#### Difference between overloading and overriding?

Method overloading is the example of compile time polymorphism, while method overriding is the example of run time polymorphism.
In the case of method overloading, parameter must be different. In case of method overriding, parameter must be the same.


#### What are the Object Oriented Principles? Explain the concepts with realistic examples!

Inheritance - Polymorphism - Encapsulation - Abstraction

#### What is method overloading?

Overloading: is a feature that allows a class to have more than one method having the same name, if their arguments lists are different. Three ways to achieve overloading - number of parameters, data type of parameters and sequence of Data type parameters.

#### What is method overriding?

If a subclass provides a different implementation for the method that has been declared by one of its parent class, it is known as method overriding.


#### Explain how object oriented languages attempt to simplify memory management for Programmers.

#### Explain the “Single Responsibility” principle!

The single-responsibility principle (SRP) is a computer-programming principle that states that every module or class should have reponsibility over a single part of the functionality provided by the software, and that responsibility should be entirely encapsulated by the class, module or function.

#### What is an object oriented program? Explain, show.

In an object oriented program, the programmers define the data type of a data structure and also the types of operations(functions) that can be applied to the data structure. In this way, the data structure becomes an object that includes both data and functions. In addition, programmers can create relationships between one object and another. For example, objects can inherit characteristics of other objects.


#### How do you make a class immutable? What do you need to watch out for?

You can make a class immutable in few ways:

1. Declare class final
2. Declare class members final
3. Create getter methods and no set methods.


#### How many instances can be created for an abstract class?

You can't create an instance from an abstract class because it's incomplete, has methods without body.


## Programming languages

### Java

#### What is autoboxing and unboxing?

Autoboxing is the automatic conversion that the Java compiler makes between the primitive types and their corresponding object wrapper classes. Unboxing means converting an object of a wrapper type to its corresponding primitive value.


#### If you have a variable, that shall store a positive whole number between 0 and 200, what primitive type would you use to store it?

Use an unsigned integer.


#### What is the "golden rule" of variable scoping in Java? What is the lifetime of variables?

A variable is available only in the scope it was defined (curly brackets). The lifetime of an Instance variable is until the object stays in memory. The lifetime of a Class variable is until the end of the program or as long as the class is loaded in memory. The lifetime of a local variable is until the control leaves the block in which it's declared.


#### What is the purpose of the ‘equals()’ method?

.equals() evaluates to the comparison of values in the objects

#### What is the difference between '==' and 'equals()'?

== checks if both objects point to the same memory location whereas .equals() evalutes to the comparison of values in the objects.


#### What does the ‘static’ keyword mean?

The keyword static indicates that the particular member belongs to a type itself, rather than to an instance of that type. This means that only one instance of that static member is created which is shared across all instances of the class.


#### Why is the main() method declared as static? Explain.

Java main() method is always static, so that the compiler can call it without the creation of an object or before the creation of an object of the class.


#### What is the default access modifier in a class?

Default - No keyword required: When no access modifier is specified for a class, method or data member, it is said to be having the default access modified by default.
Default access modifier called 'Package private' since classed having efault access modifier are accessible only with the same package.


#### What is the JVM?

Java Virtual Machine: It is an abstract virtual computer which runs by specification. One of its main features is that enables a computer to run Java programs as well as
programs writtern in other language that are converted by the compiler to byte-code. It is a software layer that secures wll protected environment to run the program and provides
good mobility("Write once, Run anywhere"). Any Java application can be run only inside some concrete implementation of the abstract specification of the Java Virtual Machine.


#### What is the difference between the JRE and the JDK?

JRE (Java Runtime Environment): It is a software layer that runs on top of a computer's operating system software and provides the class libraries and other resources(JVM) that a
specific Java program needs to run. JDK(Java Developer Kit): It provides tool for developers to create Java programs that can be executed and run by the JVM and JRE.


#### What is the difference between long and Long?

long is a primitive type, while Long is a wrapper class around the primitive long.


#### Can a long store bigger numbers than a Long?

No, because long has the same maximum value like Long, 2^63 - 1. If you want to store a bigger number, you should use BigInteger.


#### What kind of packages do you know under java.util.* ? Bring at least 3 examples.

* java.util.ArrayList
* java.util.Collections
* java.util.List


#### What are the access modifiers in Java? Which one could we use for class?

Access modifiers in Java: public, private, protected and default. For classes we can use public and default.


#### Can an “enum” contain methods in Java? Explain.

Enums can contain constructors, methods and fields. 


#### When would you use a private/protected/public attribute? What is the difference?

Private is used when you want to limit access only inside the class, protected inside the class, the package, but can be accessed if that class
is inherited. Using public you can access the class from anywhere.


#### How do you prevent developers from subclassing a class?

Declare the class with final keyword so it can't be extended(inherited).


#### How do you prevent developers from overriding a method in a subclass?

You use the final keyword in a method declaration to indicate that the method cannot be overrided by subclasses.

#### How do you prevent developers from changing the value of a variable?

Once a **final variable has been assigned, it always contains the same value. If a final variable holds a reference to an object, the the state of the object
may be changed by operations on the object, but the variable will always refer to the same object (this property of **final is called non-transitivity).

#### Think about money ;) How would you store a currency value, that shall support decimal parts? Think it through again, and try to think outside of the box!

Use Currency class.


#### What happens if you try to call something, that you have no access to, because of data hiding?

You get an error that Java compiler can't find that member.


#### What happens if you try to delete/drop an item from an array, while you are iterating over it?

The length of an array is fixed on creation, therefore it is not possible to remove any elements while iterating, or just picked by value or index.
However there is a method removeElement() in class ArrayUtils. This creates a new array without the element we want to remove. This works via iterating.

#### What happens if you try to delete/drop/add an item from a List, while you are iterating over it?

If you want to delete the item you are currently at while iterating, it will cause a ConcurrentModificationException, unless you are using an iterator and say
iterator.remove(). Esentially, the ConcurrentModificationException is used to fail-fast when something we are iterating on is modified.


#### What happens if you try to add an item to the end of an array, while you are iterating over it?

It's not possible, because arrays have a fixed size after they are created. If you want to add an element to the end of an array, you have to create a new array
with length n + 1 (if the originl list's length was n), copy the original list elements to the new one and add your element to the end of the new list.


#### If you need to access the iterator variable after a for loop, how would you do it?

We define the iterator variable before the loop, so after the loop ends, we can still retrieve the value from the iterator.

#### Which interfaces extend the Collection interface in Java. Which classes?

Set, List, Queue 

#### What is the connection between equals() and hashCode()? How are they used in HashMap?

**equals(Object obj): a method provided by java.lang.Object that indicates whether some other object passed as an argument is "equal to" the current instance.
The default implementation provided by the JDK is based on memory location - two objects are equal if and only if they are stored in the same memory address. If two
objects are equal, they MUST have the same hash code.

**hascode(): a method provided by java.lang.Object that returns an integer representation of the object memory address.


#### What is the difference between checked exceptions and unchecked exceptions? Could you bring example for each?

There are two exception types, checked and unchecked (also called runtime). The main difference is that checked 
exceptions are checked when compiled, while unchecked exceptions are checked at runtime. Checked exception (ClassNotFoundException), unchecked exception(Arithmetic Exception).


#### What is Error in Java and how does it relate to Exception?

Both error and exception are subclasses of throwable class. Exceptions are related to the application itself while the errors are related to the environment (JVM) in which
 the application is running. Errors cannot and should not be handled or caught. They signal severe problems during runtime that should stop execution. Two most common examples
 are stack overflow and out-of-memory errors.


#### When does 'finally' block run? What it is used for? Could you give an example from your projects when you would use 'finally'?

The code we defined in the finally block runs whether there was a caught exception or not. We usually use finally block to clean up the resources - e.g. we are reading from a file
 in the try block and we want to close the file no matter what.


#### What is the largest number you can work with in Java?

Built-in Java primitive type, Double MAX_VALUE `public static final double MAX_VALUE` . A constant holding the largest positive value of type double.


#### When you use method overriding, can you change the access level of the method, from protected to public? Why?When you use method overriding, can you change the access level of the method, from public to protected? Why?

A sub-class can always wided the access modifier, because it is still a valid substitution for the super-class. The access modifier of an overriding or hiding method must provide at least as much access as the overriden
 pr hidden method.


#### Can the main method be overridden? Explain your answer!

No, because the main method is a static method. A static method cannot be overridded since they are not dispatched on the object instance at runtime.


#### When you use method overriding, can you throw fewer exceptions in the subclass than in the parent class? Why?

The overriding method must NOT throw checked exceptions that are new or broader than those declared by the overriden method. For example, 
a method that declares a FileNotFoundException cannot be overidded by a method that declares a SQLException, or any other non-runtime exception, unless it's a sublcass of 
FileNotFoundException.

It means that if a method declares to throw a given exception, the overriding method in a subclass can only declare to throw that exception or its subclass.

#### When you use method overriding, can you throw more exceptions in the subclass than in the parent class? Why?

The overriding method must NOT throw checked exceptions that are new or broader than those declared by the overrided method.


#### What does "final" mean in case of a variable, method or a class?

In variable using final, you create a constant, for methods - prevent method overriding, while for classes prevent inheritance.


#### What is the super keyword?
.
The super keyword in Java is a referene variable which is used to refer immediate parent class object. Whenever you create the instance of subclass, an instance of parent class 
is created implicitly which is referred by super reference variable. We can use super keyword to access the data member or field of parent class. It is used if parent class and child have same fields.
 The super keyword can also be used to invoke parent clas method. It should be used if subclass contains the same method as parent class. In other words, it is used if method is overriden. **Usage:

 * super can be used to refer immediate parent class instance variable.
 * super can be used to invoke immediate parent class method.
 * super() can be used to invoke immediate parent class constructor: default constructor is provided by compiler automatically if there is no constructor. But, it also add super() as the first
 statement.

#### What are “generics”? When to use? Show examples.

Using java generics, programmers are able to write more general methods. It means that it is not necessary to specify the input type of a method, therefore it can handle Strings, Integers, Doubles and so on.
 It is very useful when for example we want to implement a sorting method. If we use generics, our method will handle more types of Lists. Generics also provide compile-time safety that allows programmers to
 catch invalid types at compile time.


#### What is the benefit of having “generic” containers?


#### Given two Java programs on two different machines. How can you communicate between the two? What are the possible ways?

#### What is an annotation? What can be annotated and how? Show examples.

Annotations help to associate metadata (information) to the program elements i.e instance, variables, constructors, methods, classes, etc.


### C&#35;

#### Explain the purpose of IL and how does it relate to CLR?
#### What does “managed code” mean?
#### What is an assembly?
#### What is the difference between an EXE and a DLL?
#### What is strong-typing versus weak-typing? Which is preferred? Why?
#### What is a namespace?
#### Explain sealed class in C#?
#### What is explicit vs. implicit conversion? Give examples of both of them.
#### Is a struct stored on the heap or stack?
#### Can a struct have methods?
#### Can DateTimes be null?
#### List out the differences between Array and ArrayList in C#?
#### How is the using() pattern useful? What is IDisposable? How does it support deterministic finalization?
#### How can you make sure that objects using dedicated resources (database connection, files, hardware, OS handle, etc.) are released as early as possible?
#### Why to use keyword “const” in C#? Give an example.
#### What is the difference between “const” and “readonly” variables in C#?
#### What is a property in C#?
#### List out two different types of errors in C#?
#### What is the difference between “out” and “ref” parameters in C#?
#### Can we override private virtual method in C#?
#### What's the difference between IEquatable and just overriding Object.Equals()?
#### Explain the differences between public, protected, private and internal. Explain access modifier – “protected internal” in C#!
#### What’s the difference between using `override` and `new` keywords when defining method in child class?
#### Explain StringBuilder class in C#!
#### How we can sort the array elements in descending order in C#?
#### Can you use a value type as a generic type argument in C#? For example when implementing an interface like (IEquatable).
#### What are Nullable Types in C#?
#### Conceptually, what is the difference between early-binding and late-binding?
#### What is delegate, event, callback, multicast delegate?
#### What is enum in C#?
#### What is null-conditional operator?
#### What is null-coalescing operator?
#### What is serialization?
#### What is the difference between Finalize() and Dispose() methods?
#### How do you inherit a class from another class in C#?
#### What is difference between “is” and “as” operators in C#?
#### What are indexers in C# .NET?
#### What is the difference between returning IQueryable<T> vs. IEnumerable<T>?
#### What is LINQ? Explain the idea of extension methods.
#### What are the advantages and disadvantages of lazy loading?
#### How to use of “yield” keyword? Mention at least one practical scenario where it can be used?
#### What are attributes in C#? Give some examples of usage of them.
#### By what mechanism does NUnit know what methods to test?
#### What is the GAC? What problem does it solve?
#### What is the largest number you can work with in C#?

### Database

#### How can you connect your application to a database server? What are the possible ways?
#### What do you know about database normalization?
