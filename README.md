Stress-out note

NhanNguyen

some little note by myself to remind how much i suffered

---

## Things worth to review:

| No. | Content                                                               |
| --- | --------------------------------------------------------------------- |
|     |                                                                       |
| 0   | [Nothing](#nothing)                             |


# Difference Shadow DOM and virtual DOM ?

Shadow DOM is a technique using by Angular to enscapsulation the DOM Note - it mean every DOM element is encapsulated by ShadowDom Boundary - It help seperate DOM tree into multiple part - And we just need to updated which part should be updated
The styling or javascript code inside that shadow dom node can not effect to the parent in DOM tree - easy to naming css styling
=> Solve the enscapsulation issue
=> Solve a little performance issue

Virtual DOM is a technique using by ReactJS to increase the perforamance of Application - it create a snapshot of DOM tree - and update changes of our application to the snapshot - after that Virtual DOM will be compare to Original DOM - and just update which the different element
=> Solve the performance issue 

# Ng-container, ng-template ?

# Is it possible to apply multiple directives for an element ?

We canot use multiple structural directive in one element;

Becuase it will conflix and Angular will have no idea to do with this element - walkaround is use <ng-container> to wrap this element

# What are the differences between Angular and AngularJs ?

# What are the differences between Angular and ReactJs ?

# Angular page lifecycle ? Execution flow ?

When Angular create Component in run through couple of differnce phrases in this creation process - and it give us a change to hook into this process to execute some code.

Angular will call some method in each phrases / process.

# What is the Spread operator ?




# How long have you work with .Net Framework ?

I have some previous experience working with .Net Framework, it may around 6 months

# What is the difference between .Net Framework and .Net Core ?

Both: is a free, open-source platform to create web app, web api, mobile app, desktop app...

.Net Framework is a previous version of .Net core

.Net framework:

    Only support in Window 

.Net Core:

    Lightweight, fast.

    Support is cross-platform framework, support in Window, macOS, Linux
    
    Add more features to .Net Framework

> When .Net Framework only support for window, .Net core is new version, so it add some new features, support cross-platform ( window, macos, linux) and also lightweight and fast

# Why we have to use .Net Core ?

Because it help the development process easier

# What is the Entity Framework ?

Entity Framework is an ORM framework - allow us to work with relational database in Object-oriented programing

ORM (Object-Relational Mapping): is a technique for storing, retrieving, updating and deleting relational database by oriented program

In ORM: 

    it create relational tables based on classes/object - and it called code first

    it create classes/object based on relational table - and it called called database first

It utilizes a "data layer access" to do the translation between Oject-oriented code and relation database table

# Please describe about Asp.Net MVC architecture ?

MVC stand for Model-View-Controller architecture - it help seperate Data access logic part and presentation part of our application

M - Model: the only place responsible for handling data logic, access to database

C - Controller: act like middle man between Model and View - Responsble for taking request from client - pass the request to Model - recive respond data from Model - pass that respond data to View - recive HTML/CSS code from View and sent it back to client

V - View: the only place responsible for taking data from controller - create dynamic data template 

When client request for a web page -> controller will take that request and call the model to retrieve data -> and model will send back the data to controller -> after that controller will sent the data to view -> view will responsible for create HTML code base on the set of this data and sent the HTML code back to controller -> in the end controller will sent the respond to the browser or client

# How can we pass data from Controller to View in Asp.Net MVC?



# How can we pass data from this Controller to another Controller ?



# What is the session in Asp.Net MVC ?



# Have you worked with Unit Test ?

Yes, i have some experiences working with Unit Test

ussually i use Nunit for writing Unit Test for .NET Core, C# application

There are 3 section of Unit Testing: 

    Arrange: where we put all testing data and arrange value we going to use

    Act: where we do actual calculation

    Asert: where we assert something about actual value in Act

# What is the LinQ ?

LinQ is stand for Language Interged Query

> When we fetch data from difference type of data sources, it return multiple kind of datasources -> we need a way to query multiple type of data without knowing what kind of data and the specific syntax

> It enable us to query any type of datasources like sql server, object, list,...

> Allow us to work with difference type of datasources using a similar code style without worries about what kind of this datasources

For Example: 

When we write LinQ query for data comefrom SQL Server database, LinQ Provider will convert LinQ Query to T-SQL Query to do the query in SQL Server Database

# What is Lambda Expression ?

Lambda expression is an anonymoust funciton ( with equal and greater than symbol) - lambda expression is divide into two part left hand side is an input parameters and right hand side is an expression 

> We usually pass the lambda expression into LinQ Query to do the expression of that query

# What is Filter Action is Asp.Net MVC ? ***

`In Controller` - every method is called action method.

Filter Action is an attribute that can applied either on controller aciton method or on a controller, when they are applied in controller - they will be applied for all the aciton method in controller.

> It allow us to run custom code before executing action method

For Example: 

    ValidationInput

    Authorize

    AllowAnonymous

# What is the validation attributes in Asp.Net ?

it is an attributes allow us to specify valiation rules for our class or model properties.

For Example: 

    [Required] Attribute

    [StringLength(100)] Attribute


# What is the middleware in Asp.Net Core ?

Middleware is a pices of software that has access to incoming request and outgoing respond.

Middleware can decide to perform some work after pass the request into next middleware 

For Example:

    Middleware for authenticaiton

    Middleware for handling error

# What is the Dependency Injection in Asp.Net Core ?

It is the way we inject the dependency interface of one class in constructure parameter of other class

And we have to use the help of ASP.NET to register this dependency in ConfigureServices method of Startup.cs class

services.AddSingleton(<IDependency>, Dependency)

> Singleton: the services will be intai
# What are the Service LifeTimes in Asp.Net Core ?



# What is the asynchronous programming in .Net ?



# Code first, model fist, database first ?



# Controller Action return types in Asp.Net Core ? (https://www.c-sharpcorner.com/article/
3-ways-to-return-the-data-from-controller-action-method-in-asp-net-core/)
# There are two methods , method1 allows user1 access, method2 allows user2 access. How can we implement that feature ?



# Exception handling in Asp.Net Core ?



# How to define routing in Asp.net Core ?



# Is it possible to keep the same name of action methods ?



# How can you handle exception in .Net ?



# What is RestFul API ?



# What are the differences between methods GET/POST/PUT/DELTE/PATCH ?



# How can we protect Api ?



# Stack and Heap ?



# String is reference type or value type ?



# Can you tell about your experience in Unit Test / Integration Test ?



# What is the Model Binding in Asp.Net ?



# Model binding / Parameter binding types in Asp.Net Core ? FromBody / FromForm / FromQuery / FromRoute / FromHeader



# Difference between Ienumrable and Iqueryable ?



# How can we handle exception in Asp.Net Core ?



# Have you ever analyze and design an application from by your-self ?



# Can you explain about keyword async/await ?



# What is the difference between Task and Thread ?



# What is reflection technique in .Net ?



# What is the memory leak ?



# What tools we can monitor/diagnostic memory leak in Visual Studio ?



# How can we optimize performance for Asp.Net application ?



# Access modifiers in .Net ?



# Difference between reference type and value type ?



# Difference string and stringbuilder ?



# OOP properties ?



# What is inheritance property in OOP ?



# What is encapsulation in OOP ?



# What is abstraction property in OOP ?



# What is polymorphism property in OOP ?



# Do you know any design pattern ?



# What is Singleton design pattern ?



# What is Factory Method design pattern ?



# What is SOLID ?



# What is KISS principle ?



#  


