# Enterprise module (C# branch)

### ASP.NET Core, WCF

#### What Is the difference between .NET Core and .NET Standard? How do them relate to “classic” .NET?

.NET Core is an open-source cross-platform implementation of .NET. It shares many of its characteristics with .NET Framework.

All aspects of .NET Core are open-source including libraries, runtime, compilers, languages as well as application frameworks. .NET core also supports
 C#, Visual Basic and F#. It can run the application code with the same behavior on multiple architectures, including x64, x86, and ARM. It has a flexible
  deployment model in which it can be included in the application or installed side-by-side (user-wide or system-wide).

  .NET Core can also be used with Docker. It also includes command-lines tools that can be used during local development and most importantly in continous integration.

  .NET Standard is a specification (not an implementation of .NET) which defines the set of APIs that all .NET implementations must provide. It addresses the code 
  sharing problem for .NET developers across all platforms by bringing APIs across diferent environments.

  We can think of it as another .NET Framework, except that we use it to develop class libraries only. .NET Standard is a success of the portable class 
  library.


#### What is ASP.NET MVC?

ASP.NET MVC is an open-source software from Microsoft. Its web development framework combines the features of MVC (Model-View-Controller) 
architecture, the most up-to-date ideas and techniques from Agile development and the best parts of the existing ASP.NET platform.


#### Can you explain Model, Controller and View in MVC?

Model

The model component corresponds to all the data-related logic that the user works with. This can represent either the data that is being 
transferred between the View and Controller or any other business-logic related data.

View

The View component is used for all the UI logi of the application. For example, the Customer view will include all the UI components 
such as text boxes, dropdowns, etc. that the final user interact with.

Controller

Controllers act as an interface between Model and View components to process all the business logic and incoming requests, 
manipulate data using the model component and interact with the Views to render the final output.


#### Explain the page lifecycle of MVC.

#### What is Razor View Engine?

Razor View engine is a markup syntax which helps us to write HTML and server-side code in web pages using C# or VB.NET. It is server-side
 markup language hower it is not at all a programming language.

Razor is a templating engine and ASP.NET MVC has implemented a view engine which allows us to user Razor inside of an MVC application
 to produce HTML. However, Razor does not have any ties with ASP.NET MVC.


#### What you mean by Routing in MVC?

Routing is a pattern maching system that monitor the incoming request and figures out what to do with that request. At runtime, 
Routing enging is using the Route table for matching the incoming request's URL pattern agains the URL patterns defined in the 
Route table. You can register one or more URL patterns to the Route table at Application_Start event.

#### What is Layout in MVC?

An application may contain common parts in the UI which remains the same throughout the application, such as the logo, header, 
left navigation bar, right bar or footer section. ASP.NET MVC introduced a Layout view which contains these common UI parts, so 
that we don't have to write the same code in every page.


#### What ConfigureServices() method does in Startup.cs?

This method is used to configure services that are used by the application. When the application is requested for the first time, 
it calls ConfigureServices method. This method must be declared with a public access modifier, so that environment will be able to 
read the content from metadata.


#### What Configure() method does in Startup.cs?

This method is used to define how the application will respond on each HTTP request i.e. we can control the ASP.NET pipeline. This 
method is also used to configure middleware in HTTP pipeline. This method accept IApplicationBuilder as a 
parameter.

#### What is wwwroot folder in ASP.NET Core?

By default, the wwwroot folder in the ASP.NET Core project is treated as a web root folder. Static files can be stored in any folder 
under the web root and access with a relative path to that root.

#### What’s the usage of [InternalsVisibleTo] attribute? What are pros and cons of it?

The InternalsVisibleTo attribute is a well-known attribute for testing assemblies. The internal methods of an assembly become visible 
to the test project. This allows you to test the internal methods without using reflections, so your tests are more 
maintainable.


#### Explain what is WCF?

WCF stands for Windows Communication Foundation. It is basically used to create a distributed and interoperable Application. 
This is a framework, which is used for creating Service oriented Applications. You can send data asynchronously from 
one end point to another.


#### Mention what is the endpoint in WCF and what are the three major points in WCF?

WCF offers its services to its client using an endpoint. An endpoint comprises of three key elements, the address, binding and 
contract. WCF endpoints provide the necessary resources and directions, which help clients to communicate with the various 
services WCF offers.

#### Object Relational Mapping, Entity Framework

#### What is an ORM? What are benefits, when to use?

Object Relational Mapping is a technique that lets you query and manipulate data from a database using an object-oriented paradigm. 
Benefits of using an ORM:

* DRY code
* Database handling is done automatically
* Abstracts the DB system so you can bring changes


#### What is Entity Framework? What are the advantages, limitations?

Entity Framework is an open-source ORM framework for .NET applications, supported by Microsoft. It enables developers to work with 
data using objects of domain specific classes without focusing on the underlying database tables and columns where this data is stored. 

The advantages of EF are:

* It provides auto generated code
* It reduces development time
* It reduces development cost
* It enables developers to visually design model and mapping of database
* It provides capability of programming a conceptual model


#### What is lazy loading?

Lazy loading (also called on-demand loading) is an optimization technique for the online content, be it a website or a web app. 
Instead of loading the entire we page and rendering it to the user in one go as in bulk loading, the concept of lazy loading 
assists in loading only the required section and delays the remaining, until it is needed by the user.


#### What is the difference between code first and DB first approach?

In code first approach we will first create entity classes with properties defined in it. Entity framework will create the database and 
tables based on the entity classes defined. So database is generated from the code. When the .NET code is run, the database will be created.

In database first approach, Database and tables are created first. Then you create entity Data Model using the created database.


#### What is a migration script?

Whereas a build script creates a database, a migration script, or 'change' script, alters a database. It is called a migration script because 
it changes all or part of a database from one version to another. It 'migrates' it between versions. This alteration can be as simple as 
as adding or removing a column or a table, or a complex refactoring task such as splitting tables or changing column properties in a way 
that could affect the data it stores.


#### What is a navigation property?

A navigation property is an optional property of an entity type that allows for navigation from one end of an association to the 
other end. Unlike other properties, navigation properties do not carry data.


#### Name 3 different attributes used in EF Core, what can they do for you?

[Required] - property's value is required
[Table] - override the naming convention of a table
[MinLength] - set minimum length allowed for a property value