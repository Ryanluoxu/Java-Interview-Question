# Java Interview Question

Feel free to send me pull requests when you have better answer or I make any mistake.

## Mock Test 1

### 1-10

#### 1.	What is the difference between JDK and JRE ?
- JDK is Java Development Kit including JRE and developer tools, like compiler and debugger 
- JRE is Java Runtime Environment where Java programs run on. Inside JRE basically it's JVM ( including class loader, Execution engine..) 
- For example, if we just want to run a Java program, JRE is enough. If we want to create a Java program, then we need JDK.
 
#### 2.	What is the basic flow of execution once you write a Java program ?
- The program we write is Java Source Code. Once we write a source code, Java compiler will compile it to Java Byte Code. Then Class Loader verifies this Byte Code and passes to JVM where byte codes will be executed. 
- For example, we have a source code program called Hello.java. Compiler will compile it to Hello.class which is Byte Code. Then class loader will load it and verify it, and pass to JVM where Hello.class will be executed.
 
#### 3.	Why we need `main()` method ?
- Main method is the entry point that Class Loader looks for. We need main method as starting point so that our program can start executing.
 
#### 4.	Why `main()` is `static` ?
- For non static method, we need to create an object so that we can access the method. But Class Loader is not able to create an object and it has to access main method in the beginning of the program. So main method must be static so that Class Loader can access it without creating an object.

#### 5.	What do you mean by `static` ?
- Static means the variables or methods are available at class level. We don’t have to create an instance of the class to access it. 
- For example, we have a public class called 'Company', and there are two methods which are static method showCompany and non-static method showCompanyAddress. So we can access showCompany directly. But we have to create an object of class Company to access showCompanyAddress.

#### 6.	What is class ? Give me an example.
- Class is something in general. It is to provide templates to create objects. This template can define variables and methods so that the member of this class can access those variables as state and methods as its behavior.
- The purpose of writing class is to protect our data members which are attributes and methods.
- For example, we have a class called 'Bank' which contains variable bankCode and method showBankCode. Then we create a member called DBS of this class so that DBS will have variable of bankCode and method of showBankCode.
 
#### 7.	What is object ? Give me an example. 
- Object is a specified item. Like this book is an object. 
- Or we can say object is an instance of the class. To call non static method from a static method, object has to be created first.  For example, we have a class called Customer, and Jason is the one of customer. So Jason is an object of this Customer class. 

#### 8.	What statement we write to create object ?
- We use 'new' operator to create an object. 
- Statement is : `Class object = new Class();`.
- For example, `University NUS = new University();`
- Once we creates an object, it goes in Heap. And find the reference in Stack. Finally it will be cleared by GC.

#### 9.	What is OOPs ?
- OOPs is Object Oriented Programs.
- Object Oriented means we organize our software as a combination of objects.
- Basic concepts of OOPs is Object, Class, Inheritance, Polymorphism, Abstraction and Encapsulation.
 
#### 10.	Is it possible to write more than one `main()` method in a class ?
- Yes. It's possible as long as the method parameter is different. This is called method overloading. 

### 11-20
#### 11.	What is Encapsulation ?
- Encapsulation is a mechanism of wrapping the data and code so that the variables of this class can be only accessed through certain methods. The purpose is to protect our variable or attributes.
- To achieve encapsulation, we declare the variables as private. And provide public setter and getter methods to modify and view the values.
- For example, we have a class called Account which has an attribute: password.
```
public class Account {
   private String password;
   // setter and getter
   ..
}
```

#### 12.	What is method overloading ?
- Method overloading is a feature that allows a class to have two or more methods with same name but different parameters.
- For example, we have a class called Bank. Inside the class, we have a method called showCustomerNumber with no parameter. Then we can use method overloading to create another method called showCustomerNumber with a parameter of customerNumber. 
- Method overloading is one type of polymorphism.

Polymorphism:
1.	Polymorphism means many forms. 
2.	It is the ability to present the same interface by using different forms of data.
3.	And it is an important feature for programmers to add more into the existing program

#### 13.	What is method overriding ? 
- Method overriding is a feature for child class to override the method of parent class.
- The benefit is to define a behavior that's specific to the child class based on its own requirements.
- For example, we have a parent class called Vegetable and a child class called Potato. Inside Vegetable, we have a show method showing that "This is a vegetable." and we can use method overriding to create same method for Potato showing that "This is a potato."
- Method overriding is one type of polymorphism.

#### 14.	What is constructor ?
- Constructor is a special type of method to initialize the object.
- There are 2 basic rules: constructor name must be the same as class name; and constructor must have no explicit return type.
- Types: Default constructor (by JVM) and parameterized constructor (by programmer) 
 
#### 15.	What is association ?
- Association is a relationship between two classes. 
- It can be either composition or aggregation.
- Composition means must have. Like animal has body.
- Aggregation means optional. Like animal has legs, but not every animal has legs. So legs are optional for animal.
 
#### 16.	What is the purpose of `toString()` ? 
- The purpose of toString() is return a string representation of the object or tell something about the object instance. 
- For example, a Person class may override its toString method to return "I am a person." so that we can just print an abject itself to get this information.
 
#### 17.	What is Type Casting ? Types of type casting in Java ?
- Means temporary conversion of a variable to another data type.
- Implicit casting: `int` -> `double`; explicit casting: `double` -> `int`
-	Up casting: `String` -> `Object`; Down casting: `Object` -> `String`
- Auto boxing: `int` -> `Integer`; Un boxing: `Interger` -> `int`.

#### 18.	What is inheritance ? What type of inheritance Java supports ?
- Classes can be derived from other classes, so that inheriting fields and methods from those classes. Called inheritance. The class that inherites is called child class or sub class. The class that is inherited is called parent class or super class.
- Java support multi level inheritance. 
- For example, I am a son. And I can have a father and my father can has his father. And so on.
 
#### 19.	What is advantages of inheritance ?
- For method overriding. A child class can override the method that inherites from its parent class to perform its own functionality.
- To reuse the code. So that we don't have to write codes which already exist in parent class.
- We don't have to create objects when using inheritance so that we can save momery.
 
#### 20.	What is `super` keyword ? Where we use ?
- `super` comes from superclass which is also called parent class. So `super` refers to parent class. 
- We use `super` to call parent constructor, call overridden methods or access hidden fields.
- For example, if parent class has a show method saying "I am parent." and child class override it by "I am child". Then we can use super.show method to show "I am parent".

### 21-30
#### 21.	What is abstraction ? What is the purpose of abstraction ?
- Abstraction is a process to hide the implementation and only provide the functionality.
- In other words, the user can know what the object does instead of how it does.
- The purpose of abstraction is to hide details and only show the essential features of the object. 
- In Java, abstraction is achieved by using interface and abstract class.
 
#### 22.	What is abstract class ? Benefits of writing an abstract class ?
- Abstract class is the class that contains abstract methods.  Abstract method is a method that has been declared but without implementation. 
- For example, we have an abstract class called Country, and we have an abstract method inside called showCountry but we don’t create the method body. If we want to implement this method, we have to created a subclass and give the method body for it saying, "I am a country."
- The benefit is to provide a template so that those well-defined class can follow it and implement those methods which have been declared.
 
#### 23.	What is interface ? Benefits of writing an interface ?
- Abstract class is the class that contains abstract methods.  Abstract method is a method that has been declared but without implementation. 
- For example, we have an abstract class called Country, and we have an abstract method inside called showCountry but we don’t create the method body. If we want to implement this method, we have to created a subclass and give the method body for it saying, "I am a country."
- The benefit is to provide a template so that those well-defined class can follow it and implement those methods which have been declared.
 
#### 24.	What is the difference between abstraction and encapsulation ?
- Abstraction and encapsulation are both important features of OOPs and they are different to each other. Abstraction occurs during design phase. And encapsulation occurs during development phase.
- Abstraction is used to hide details and only show the essential features of the object. One example is interface. 
- Encapsulation is the process of binding the data. One example is the class with private variable and public method.
- In simple words, we do abstraction when deciding what to implement. We do encapsulation when hiding something that we have implemented.
 
#### 25.	What is the difference between abstract class and interface ?
- Interface is a fully abstract class
- Abstract class can have variables and both abstract method and concrete method. While interface can only have abstract method and the constant. 
- A class can only extend one abstract class while can implement more than one interfaces.
 
#### 26.	What is final keyword ?
- Final keyword is to restrict the users.
- The class with final cannot have child class. 
- The variable with final can't be change.
- The method with final can't be override.
 
#### 27.	What is anonymous inner class ?
- Final keyword is to restrict the users.
- The class with final cannot have child class. 
- The variable with final can't be change.
- The method with final can't be override.
 
#### 28.	What is singleton class ? What is the purpose of writing singleton class ?
- It's the class that we make its constructor as private
- The purpose is to allow users to create object only one time.
 
#### 29.	What is factory design pattern ? What is factory method ?

#### 30.	Can we write a constructor inside abstract class or interface ?
- Constructor is a special method to initialize the object with method body.
- For interface, it cannot have any concrete method. So constructor is not allowed in interface.
- For abstract class, we can have a constructor since it can have both abstract and concrete method.
- The situations: you want to initialize the object of abstract class before instantiation by subclass.


## Mock Test 2

### 1-10
#### 1.	How many data types we have in Java ?
- Primitive : int, short, long, byte, float, double, char, boolean
- Non primitive: String, Arrays, user defined classes

#### 2.	What are access modifiers ?
They are attributes that determine whether a class can be accessed.
Types:
- Public: outside class and package
- Private: only within the class
- Protected: within the package; outside the package with inheritance only
- Default: only within the package

#### 3.	What is array ? benefits and limitation.
- Array is a fixed sized data structure to store similar data type.
- Benefits:
    - Optimize the codes, so that we can store, retrieve or sort the data easily
- Limitation:
    - The size of array is fixed. We can’t change the size at runtime.
    - We need the decide the data type when we create array.
 
#### 4.	Importance of .equals() and hashCode().
- By generating hashCode() and equals(), we can compare the values of two objects.
- hassCode() is used to create a temperate memory location for an object so that we can use .equal() to compare the values of objects.

#### 5.	Why we need to handle exception ?
- It is a process that converts system error into user friendly error message.
- So that we can handle run time error and maintain normal flow of java application.
- The purpose is to prevent data lost.

#### 6.	How we handle exception ?
- Try – catch : 
    - Try: where we put our codes which may causes problem
    - Catch: to provide the user friendly error message when exception happens 
- Throw:
    - For user defined exception
    - To provide error message when user defined exception happens
    - For those situation are wrong for us but right for JVM.
- Throws: 
    - throws keyword is within the method signature to indicate this method may cause exception. 
    - For checked exception.

#### 7.	Difference between checked and unchecked exception.
- Checked exceptions:  the classes that extend Throwable class except RuntimeException and Error. They are being **checked at compile time**.
- Unchecked exceptions: the classes that extend RuntimeException. They are being **checked at runtime**.


#### 8.	What is the purpose of throw keyword?
- The purpose is to handle those exceptions we need to handle manually

#### 9.	Why we need Thread? Different way to create thread.
- Threads allow us to do multiple tasks at the same time.
- Two ways
    - Extends Thread class
    - Implements Runnable interface


#### 10.	What is synchronization in thread?
- It’s the capability to control the access of multiple threads to any shared resource.
- We can use it to allow only one thread to access the shared resource at the time.


### 11-21
#### 11.	What is the need of Producer and Consumer class in threading?
- They are commonly used in multi-threaded program.
- We can code Producer and Consumer independently, they just need to know shared object.
- Producer and Consumer don’t have to know each other. 
- Separate functionalities to producer and consumer, so that our codes are more clean, readable and manageable.  


#### 12.	What is Thread Pool ?
- It’s a group of threads that are waiting for the job.
- The threads there can be reuse many times so that we avoid overhead of creating threads.


#### 13.	What is volatile keyword ?
- It’s used to mark a variable as “being stored in main memory”.
- Means for these variables, we read it from main memory and write it to main memory.


#### 14.	What is wrapper class ?
- They’re used to create objects for eight primitive data types. Because sometimes only objects are acceptable. Like map and list.

#### 15.	What is purpose of Generics ?
- With the help of Generics, we can write a single generic method or class. And use the method or class with different type of arguments. ( wrapper class for primitive )
- Like arraylist and map


#### 16.	Tell me some interface name and classes in collection framework.
- Set: HashSet, TreeSet and LinkedHashSet
- List: ArrayList and LinkedList
- Queue: LinkedList


#### 17.	Collection is a class or interface ?
- Collection is interface. It’s the parent interface of all collections in Java.
- Collections is a utility class to implement the Collection interface.


#### 18.	What is Comparable and Comparator interfaces ?
- Comparable: It’s the interface that makes classes comparable. The object of those classes is capable to compare itself with other objects.
- Comparator: It’s the interface that let classes become a comparator. The object of those classes is capable to compare two different objects.


#### 19.	What is serialization in Java ?
- It’s a mechanism that an object can be represented as a sequence of bytes.
- The bytes includes: object’s data, object’s type and types of data.


#### 20.	What is Marker interface ? What is the purpose ?
- It's the interface without any fields or methods. It’s empty interface.
- rializable, Clonnable and Remote
- The purpose: it indicate signal or command to Complier.


#### 21.	What is transient keyword ?
- It’s the keyword to make variable unable to be serialized.
- So JVM knows that variable is not part of the persistent state of the object.


### Database

#### 1.	What is DBMS and RDMBS ?
- The database management system is a collection of programs that enables user to store, retrieve, update and delete information from a database.
- Relational Database Management system (RDBMS) 
    - It is a database management system (DBMS) that is based on the relational model. 
    - Data can be accessed in many different ways without having to reorganize the database tables. 
    - Data can be accessed using an API , Structured Query Language (SQL).


#### 2.	What is SQL ?
- Structured Query Language is a language specially for communicating with databases. So that we can store, retrieve and manipulate the data in database.

#### 3.	Different type of SQL’s statements ?
- DDL: Data Definition Language
    - To define the structure that holds the data.
    - E.g. Create, Alter, Drop and Truncate table.
- DML: Data Manipulation Language
    - To manipulate the data.
    - Insert, Update, delete
- DCL: Data Control Language
    - To control the visibility of data
    - Grant, Revoke
- DQL: Data Query Language
    - Select
- TCL: transaction Control Language
    - Commit
    - Rollback


#### 4.	What are properties of a transaction ?	(ACID)
- A transaction is a sequential group of DB manipulation operations as one single work unit.
- Atomicity: A transaction must be treated as a unit. Transaction finishes if all the steps completes, otherwise the transaction will be rolled back.
- Consistency: The database must remain in a consistent state after any transaction.
- Isolation: Make sure each transaction operates independently. They don’t affect each other.
- Durability: The database should be durable enough to hold all the updates even if the system fails or restarts. 


#### 5.	What are the different type of normalization ?
- The process of removing the redundant data and make table well defined.
Types:
- First Normal Form (1NF)
    - In 1NF, each column just hold one value.
    - productID, color, price
- 2NF
    - It’s 1NF
    - All non-key attributes are fully functional dependent on the primary key.
- 3NF
    - It’s 2NF
    - There is no columns transitively dependent on PK.
    - ProducdID-Google-US


#### 6.	What is a primary and Foreign key ?
Primary key:
- PK works as an index of the data in a table.
- It’s a column. Its values are unique in every row.
- Every row must have a primary key value.
- If it’s referred by foreign key, we can’t change its key value
Foreign key:
- FK works as a reference index to access the data of other table.
- If we have a relational table C of table A. There is one column in table C that refers PK of table A. So that the data of table A can be accessed by table C.
- This column is called foreign key.


#### 7.	Define Join and explain different type of joins ?
Join:
- To avoid data duplication, data is stored in some related tables.
- Join is used to get data from these tables to create a new table which meets our requirement.
Types:
- Inner join: returns records at the intersection
- Left join: returns all records from table A and matching records from B
- Right join: returns all from B and matching from A
- Full join: all records from A and B
- natural join: remove the duplicate columns from the result
- Self join: it is a join of a table to itself.


#### 8.	What is the advantage of stored procedure ?
- It is a function that contains a collection of SQL queries.
- They are pre-compiled and stored in the database. So execution is much faster.
- It is portable. The stored procedures in SQL can be run on every platform that MySQL runs on. We don’t have to install additional package or program for that


#### 9.	What is JDBC ?
- Java Database Connectivity. It’s an API to access DB.
- Including 3 activities: 	
    - Connect to a DB
    - Send queries and update statements to DB
    - Retrieve and process the results received from DB

#### 10.	Types of JDBC Driver ?
1. JDBC – ODBC bridge driver
    - In this type, JDBC-ODBC bridge driver converts JDBC calls into ODBC calls. And uses ODBC driver to connect to DB.
    - It’s no recommended, because ODBC driver needs to be installed in client machine and it is slow. 
2. Native – API driver ( partially)
    - In this driver, JDBC API calls are converted into native API calls. And uses vendor database library to connect to DB.
    - Causes portability issue. Native driver and vendor library have to be installed in client machine.
    ![2](http://pic/2.emf)
 3. Network Protocol driver ( fully)
    - Uses middleware to connect to DB. JDBC calls are converted into vendor-specific database protocol. 
    - No client side library is required but it is costly because of maintenance. 
    ![3](http://pic/3.emf)
4. Thin driver ( fully)
    - The thin driver converts JDBC calls directly into vendor-specific database protocol.
    - Better performance and no software is required on both client and server.
    ![4](https://github.com/Ryanluoxu/Java-Interview-Question/blob/master/pic/4.emf)
    
     ![4](https://github.com/Ryanluoxu/Java-Interview-Question/blob/master/pic/mmexport1500263471803.jpg)
    
    



#### 11.	What are the steps to connect with the database in Java ?

#### 12.	Tell me some interfaces and classes that we use from java.sql package.

#### 13.	Different type of JDBC statements

#### 14.	Difference between Statement and PreparedStatement interface ?

#### 15.	How to execute a stored procedure ?

## Mock Test 3

#### 1.	What is MVC? What is DAO?

#### 2.	What is Web Container? Role of Web Container?

#### 3.	Difference between doGet() and doPost()

#### 4.	Difference between RequestDispatcher and SendRedirect

#### 5.	How many different ways we can handle session and servlet?

#### 6.	JSP life cycle

#### 7.	How many directives we have in JSP?

#### 8.	What is JSTL? What is Custom Tags?

#### 9.	How to handle exception in JSP?

#### 10.	What is expression language in JSP?

#### 11.	What is the difference between JNDI and JDBC?

#### 12.	What is the difference between servlet, JSP and JSF?

#### 13.	Difference between Web server and Application server?

