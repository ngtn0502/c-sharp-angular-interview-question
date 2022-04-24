

---

# Things worth to review:

| No. | Content                                                               |
| --- | --------------------------------------------------------------------- |
|     |                                                                       |
| 1   | [Angular](#angular)                             |
| 2   | [DotNET](#dotnet)                             |
| 3   | [Database](#database)                             |

# Angular

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

# What is State Manament Angular?

State is a way we store data member in component in react or angular

There are several way to do state management in Angular

For Example:

    Service

    NgRx

# What's the difference of ASP.Net and .Net Core?

ASP.NET: is a framwork of .NET Core for building web-api

.NET Core: is a open-source platform for building many kind of allication, include web application

# What access modifiers exist in C#?

Public: mean that the type/member is available for all other code in the same assembly 

Private: mean that the type/member are only available in the same class

Protected: mean that the type/member are only available in the same class or in the class derived from this class 

Static: static class can not be instanciated ( cannot use `new operator` to create class) - we access the method of static class by calling class name itself

    ex: Console.Wriline()

# What design patterns and software principles have you worked with?

OOP principle

SOLID principle

Dependency Injection principle

Generic Repository pattern

Specificaiton pattern

Mediator patern

# What is singleton?

Singleton: our dependency will intanciated when our application start and remain/alive whole lifetime of our application

# What is a difference between string and stringbuilder? When would you use over the other?

String: string is immutable - it mean when we save a string in to variable - we save the actual value of string in memory.

> When we change string - it will create new place in memory rather than changing the actual value sit on memory

StringBuilder: is mutable

> When we change stringBuilder -  we change the actual value sit on memory

> StringBuilder helpful when we have to append or concat string, because it do not create new string in memory - do not cause memory leak.

# What memory leaks you are aware of in C#?

If we use string type, whenever we concat or append string, it will create new string variable in memory -> lead to memory leak 

Keeping database connections or result sets open when they are not used. Remember to call Dispose() on all IDisposable objects. Use the using statement.

# What's the purpose of garbage collector?

GC help us to manage memory automatically

- Allocate object on memory heap rather than stack

- Clean variable when it no longer in use -> release memory

# How do you handle errors in C#?

```
try {

}
catch {

}
```
# What is Interceptor?

in Angular, interceptor is a special services . We use to Interceptor to intercep into every HTTP Request and HTTP Respone 

Normally, we use our information into our HTTP headers of HTTP Request or modify/format HTTP Response information before returning services

# What is Reactive Programing?

Reactive Programing is asynchronous data-stream programming

In reactive programing, we use Observable to control data-stream, observable will emit the data for every changes of the state, observer will receive notification if they subscribe to an observable

# What is RxJs?

RxJs is library for reactive programming;

RxJS provide some classes and operator for 


---

---

# dotNET

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

> .NET Core support cross-platform

> Lightweight, fast, better perforamance

> Well support for cloud computing eviroment

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

> Transient: the services will be instantiate every time we request it

> Scoped: the services will be instantiate and create its scope. Within this scope, it reuses the existing services. Services will be destroy if no one using or reference to it

> Singleton: the services will be instantiate and remain with lifetime of application, and we can use it every where

# What are the Service LifeTimes in Asp.Net Core ?



# What is the asynchronous programming in .Net ?

In C#, we use async-await and Task object to perform asynchronous task - and it follow [Task-based Asynchronous Pattern](https://docs.microsoft.com/en-us/dotnet/standard/asynchronous-programming-patterns/task-based-asynchronous-pattern-tap)

We await to the method that take time or services response for calling external api, it will run in the background and does not affect main thread of out application

# Code first, model fist, database first ?

It is way of approach we use in Entity Framework

> Code frist: means we write .NET Class, entity framework will convert this class into entity of database - control database by code

> Database first: means EF will creates model and class for us based on the existing database

> Model first: means we draw the models first by EF Designer tool and EF will take care about creating database for us

# Controller Action return types in Asp.Net Core ? - [Articles](https://www.c-sharpcorner.com/article/
3-ways-to-return-the-data-from-controller-action-method-in-asp-net-core/)

Return IActionResult Type

Benefit:
> It allow to return multiple type of data along with the status code, this is very important in RESTful API

Drawback:
> Have to define type of data for swagger.

```
[Route("emplpyees/{id}")]
[ProducesResponseType(StatusCodes.Status201Created, Type = typeof(Employee))]  
[ProducesResponseType(StatusCodes.Status400BadRequest, Type = typeof(Employee))]  
public IActionResult GetEmployeeById(int id)  
{  
    if (id == 0)  
    {  
        return NotFound();  
    }  
    var employee = new Employee() { Id = 1, Name = "Nitish" }; // Get the data from db  
    return Ok(employee);  
}  
```

Return ActionResult<T>

Benefit
> It allow to return multiple type of data along with the status code, this is very important in RESTful API, does not need to defiend type of data for swagger

[Route("emplpyees/{id}")]  
[ProducesResponseType(StatusCodes.Status201Created)]  
[ProducesResponseType(StatusCodes.Status400BadRequest)]  
public ActionResult<Employee> GetEmployeeById(int id)  
{  
    if (id == 0)  
    {  
        return NotFound();  
    }  
    var employee = new Employee() { Id = 1, Name = "Nitish" }; // Get the data from db  
    return employee;  
}  

# There are two methods , method1 allows user1 access, method2 allows user2 access. How can we implement that feature ?



# Exception handling in Asp.Net Core ?

To handle exception in ASP.Net Core, we use exception middleware

It will catch the HTTP Request pipeline

If there is error in Request, middleware will return `the consist response type`.

> Consistent response type is important because it help client-side easier to handle error message.

If there is no error, middleware will let the HTTP Request continue to next middleware in the pipeline.


# How to define routing in Asp.net Core ?

In Asp.Net Core, it is provide a feature called Route Attribue: [Route="Employee/Id"]

It allow us to defined a route for controller or action method inside the controller.

# Is it possible to keep the same name of action methods ?

Yes, it is possible to have the same name of action method.

But the action method need to have difference route attribute or difference parametter.

# How can you handle exception in .Net ?



# What is RestFul API ?

RESTful API is a standart for developing web api

# What are the differences between methods GET/POST/PUT/DELTE/PATCH ?

> POST: create new set of data in 



# How can we protect Api ?



# Stack and Heap ?

Stack is where stored primitype type ( number, int, boolean, et cetera...)

Heap is where stored reference type ( object, array, class, string, et cetera...)

# String is reference type or value type ?

String is reference type. But string is immuatble.

It means, everytime we change the value of string, compiler will create a new string object in memory and point the string variable into that memory location.

We can use StringBuilder to make string muatable.

# Can you tell about your experience in Unit Test / Integration Test ?



# What is the Model Binding in Asp.Net ?

Model binding is a way ASP.NET Core bind our Routing Data ( path, query parameter,..) into the RouteAttribute of action method in the controller

# Model binding / Parameter binding types in Asp.Net Core ? FromBody / FromForm / FromQuery / FromRoute / FromHeader

Parameter binding is a way ASP.NET Core bind our Body, Header Data to the parameter of action method in the controller

# Difference between Ienumrable and Iqueryable ?

IEnumerable should ony using for storing in-memory value ( memory/data not connected to the database)

IQueryable should using for data fetching from the database.

Because:

``` 
TestingEntiies db = new TestingEntities(); //mock databse
```

> IEnumerable: fetch all table from database and apply filter in client side

```
In C#:

IEnumerable<Employee> ob = db.Employee // loading employee table
IEnumerable<Employee> b = ob.Where(x => x.id == 2).ToList();

In SQL:

SELECT * FROM [Employee]
```

> IQueryable: filter and fetch data directly in database

```
In C#:

IQueryable<Employee> ob = db.Employee // loading employee table
IQueryable<Employee> b = ob.Where(x => x.Id == 2).ToList();

In SQL:

SELECT * FROM [Employee] WHERE Id = 2;
```

> So IQueryable is better performance than IEnumerable with in-database data

# Have you ever analyze and design an application from by your-self ?



# Can you explain about keyword async/await ?

Async/await key word is use for asynchronous programing in C#

Async: we add async before the method to make this method become asynchronous, and we can be able use await keyword inside async method

Await: we add await before the task to run this task in the background ( does not block the main task) and to tell the execution should stop until the Task complete.

# What is the difference between Task and Thread ?

Task repesent some work should be done in the background ( so it does not block the main thread)

Thread is the worker - is the thing that responsible for the execution

# What is reflection technique in .Net ?


# What is the memory leak ?


# What tools we can monitor/diagnostic memory leak in Visual Studio ?


# How can we optimize performance for Asp.Net application ?

IQueryable and IEnumerable

# Access modifiers in .Net ?

Pulic / Private / Protected / Internal

Public: method/property of this class will available to all other class in the same asembly

Private: method/property of this class only available in the same class

Protected: method/property of this class will be available in the same class and derived class of protected class ( same asembly)

Internal: method/property of this class will be available in the same class and derived class of internal class same asembly and difference assembly.

# Difference between reference type and value type ?

Reference type: mean that the variable only hold the address/ hold the reference to the actual value.

Value type: mean that the variable hold the actual value sit in memory.

# Difference string and stringbuilder ?

String is immutable

StringBuilder is mutable

# OOP properties ?

Enscapsulation

Inheritance

Abstraction

Polymorphism

# What is inheritance property in OOP ?

The class can be inherit from base class, and this will have access to method and property of base class

> Make the class more flexible - increase scalability

# What is encapsulation in OOP ?

We encapsulate/protect the property and method (data) of the class ( by using access modifier).

> We protect the data of the class, to prevent accidentally modify from other class

> The data or property of the class will be hidden from any other class

> Encapsulation can be achieved by using access modifier

```
using system;  
public class Department {  
    private string departname;.......  
    // Accessor.  
    public string GetDepartname() {  
        return departname;  
    }  
    // Mutator.  
    public void SetDepartname(string a) {  
        departname = a;  
    }  
}  
```

```
public static int Main(string[] args) {  
    Department d = new Department();  
    d.SetDepartname("ELECTRONICS");  
    Console.WriteLine("The Department is :" + d.GetDepartname());  
    return 0;  
}
```

# What is abstraction property in OOP ?

Abstraction: it mean the class should show essential information and hiding detail from user

> In C#, Abstraction can be achived with abstract class.

Abstract class is a class can not be instanciated.

Abstract method is a method that do not have a body and the actual implementation is in the derived class.

> Abstract class provide a common definition of property and method that derived class can share

```
class program  
{  
    abstract class animal  
    {  
        public abstract void eat();  
        public void sound()  
        {  
            Console.WriteLine("dog can sound");  
        }  
    }  
    class dog : animal  
    {  
        public override void eat()  
        {  
            Console.WriteLine("dog can eat");  
        }  
    }  
    static void Main(string[] args)  
    {  
        dog mydog = new dog();  
        animal thePet = mydog;  
        thePet.eat();  
        mydog.sound();  
    }  
}  
```

# What is polymorphism property in OOP ?

Polymorphism mean that the derived class can overide the method in base class

> Method in derived class can overide the method in base class

Polymorphism mean that same class can have multiple functionality, multiple implementation

For example:

    Compiler will check the parameter passed and make the decision of which method to call

```
public class TestData  
{  
    public int Add(int a, int b, int c)  
    {  
        return a + b + c;  
    }  
    public int Add(int a, int b)  
    {  
        return a + b;  
    }  
}  
class Program  
{  
    static void Main(string[] args)  
    {  
        TestData dataClass = new TestData();  
        int add2 = dataClass.Add(45, 34, 67);  
        int add1 = dataClass.Add(23, 34);  
    }  
}  
```

# Database

## Store Procedure (advantage, disadvantage), how can it improve the performance?

Pros

- Good performance
- High security
- Reusable

Cons

- Hard for testing and debugging
- Hard for maintenance

Improvement

- Split SP into smaller SP, single responsibility for easy to maintenance
- SET NOCOUNT ON
- Avoid select all columns
- Avoid sub-query
- Avoid calculation in WHERE clause
- Try to avoid/limit using cursor
- Avoid prefix sp_
- Use schema name with tables
- Consider using temporary table, table variable, CTE
- Use indexing
- Use SQL Profiler and Execution Plan to analyze and turning query

## Truncate vs delete from

- DELETE: Delete row or table based on condition

```
DELETE FROM tbo.example
WHERE condition
```

- TRUNCATE: delete all row or all table in database not based on any condition

```
TRUNCATE FROM tbo.example
```

## Identity vs scope identity

@@Indentity return last id value in the same database connection 

Scope_Identity() return last id value in the same scope

## Nosql vs sql


## What kind of Database that you have been using so far ?

I mainly use mongodoDB for nosql database and sql server for relational-database

## How long have worked with MS SQL Server ?

I have little experience with sql server, it about 2-3 years

## What types of object or features that you have been using in MS SQL ?

## What types of join do you know in SQL ?

Inner join: Return records that have matching value in both table

Left join: Return all records in left table and matched record in right table

Right join: Return all records in right table and matched record in left table

Full Outer join: Return all records, even if it matched or not

## What is user-defined function in SQL ?

UDF is most likely like function in other programming languages, use to perform complex calculation or formating data.

UDF can take one or more input parameter and return single value or result set of value

## What is stored procedure in SQL ?

Store procedure is a container for reusable query, that we can execute over and over late.

## What is the view in MS SQL ?

View is a place contained saved sql query, it can be consider as a virtual table.

- Help to reduce the complexity of join query => No need to write joint query everytime we need

## What is sub-query ?

Sub-query is a nested query inside outer query.

We use returned value from sub-query to perform another outer query.

## Store Procedure (advantage, disadvantage), how can it improve the performance?

Advanages:

- Reuseable.

- Decouple business logic code from database

- High security.

Disadvantage:

- Hard to debug and maintain because error only happen in compile time.

Improvetion

- SET NOCOUNT ON

- Split sp into multiple sp with single responsibility

- Avoid select all column

- Using indexes.

## What is temporary table in MS SQL ?

Temporary table is most likely like permanent table, is useful for saved permanent data or intermadiate table.

## What is the index in database ? Any attention for using index ?

Indexing is a technique help us to improve the performance of the query.

We index the column to sort it into specific order, and when we do the searching in where clause or any other condition, it will reduce the time 
## What are the difference between clustered index and non-clustered index ?

[Clustered - Non-Clustered Indexing](https://www.youtube.com/watch?v=NGslt99VOCw&t=259s)

Clustered index is defined how records are arranged/stored physically in table

- ex: Primmary key will be set to be clustered index by default when we created table, that reason why our records displayed by ascending order in table

Non-clustered index: we indexing a column of table in another place, when we do the searching it will find data in indexing table after that sql server will do the lookup to find actual data in real table.

Difference:

- One clustered index - many non-clustered index

- Clustered index is faster and lighter than non-clusterd index

> Because non-clustered index need to create one more table and do the lookup thing

- Clusterd index determines how records sit physically in specific order 

- non-CLuster index do not affect how records is store in table

## What are the difference between User-Defined Function and Stored Procedure ?

Scalar(adj): a thing should be returned one or single value

UDF is most likely like function in programming languages: we use to convert value to another format, perform a complex calculation, help us to not repeat the code multiple time.

Store procedure is a place we saved query for reuseable purpuse.

Difference:

- UDF must return value - SP does not force

- SP can have output parameter - UDF can not

## What is the transaction in SQL Server ?

Transaction: is a way we ensure to do not accidentally modify the stored data - ensure the integrity of data

When we begin the transaction, it help us to decide to commit transaction when all query is complete - or rollbacked the database to previous staged when there is an error.

> It help to prevent the maintain the integrity of database

## Different between @@IDENITY, SCOPE_IDENTITY() and IDENT_CURRENT() ?

@@Indentity return id value of latest query which executed in same connection

Scope_Identity() return id value of latest query which executed in the same scope

 - Scope mean: in the same function, store procedure,..

## @ERROR and ERROR_NUMBER() ?

This is a old way to handle error in SQL Server

Now we using Try..Catch like another programming languages ( C#, Java) to handle error

Try...Catch block is using with Transaction to ensure the integrity of database

```
Create Store Procedure SP_Example
@ProductID int,
as
Begin

Begin Try
    Begin Transaction
        // Logic query 
        // Logic code
    Commit Transaction // Commit all query to affect database if there no error
End Try
Begin Catch
    Rollback Transaction // Rollback to previous staged of database when there is error happened
End Catch
End
```

## Primary Key and Unique Key ?

Primary key: is an identifier of records - ensure records in specific column is unique

- Primary key value is unique in column.

- Does not allow null

- Only one primary key constrain in table

- Using for clustered indexing by default 

Unique key: is a constrain to make sure data in the column is unique - not duplicated

- Allow null

- Allow multiple unique key constrain in one table

- For creating non-clusterd indexing

## Primary Key and Foreign Key ?

Foreign key in one table is primary key in another table

Foreign key is a column that reference to another columns ( usually primarykey) in another table

- It display the relationship between two table

- One records allow to be have multiple foreign key.

- Can have more than one foreign key in table

- Can contain null value

## What is the self-join in SQL and when should we use it ?

We rarely using self-join in SQL

ex: Using it when table references data in itself

## What types of backup do you know in SQL Server ?

Full Backup: foundation of any backup - need to be done first in every kind of backup

Differential Backup: backup the difference between latest full-backup and recent file

Transaction Backup

Log Backup

## What is cross join and full join in SQL ?

Cross join: combine all comlumn and all record from two table into one - no on clause are made

Full join: is combine of right join and left join - it try to join two table, if any column does not sactify the on clause it will return null in this

## What tool we can use for tracing query in MS SQL Server ?

Sql server profiler

## Do you know any best practice when working with stored procedures ?

Drop store before creating new store procedures

Split store procedure into multiple-small-onepurpose-singleResponsibility store procedure => easy to maintain and debug

Using indexing to increase performance 

Carefully when using where clause and subquery - because sub-query in where clause will be executed in every records in outer table

Avoild calculation in where clause

SET NOCOUNT ON -> We do not need to see *how manny row effected* in every completed query in store procedure -> increate performance

Using schema name for table

Carefully, consider when using temporary table, temporary variable

## Do you know how to optimize query performance ?

Avoid select all column - avoid select *

Avoid subquery in where clause - avoid calculation in where clause

> Because where clause will be executed in every records in table

Avoid/Consider when using temporary table, temporary varible

## Do you know how to optimize performance of the database ?

Propering indexing

Retreive needed data - relevant data only - need to analyze the requrement/business carafully

Consider when using subquery in every query


