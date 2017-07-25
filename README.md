# Java Interview Question

Feel free to give me pull requests when you have better answer or I make any mistake.

## Mock Test 1

### 1-10

#### 1.	What is the difference between JDK and JRE ?
- JDK is Java Development Kit including JRE and developer tools, like compiler and debugger 
- JRE is Java Runtime Environment where Java programs run on. Inside JRE basically it's JVM ( including class loader, Execution engine..) 
- For example, if we just want to run a Java program, JRE is enough. If we want to create a Java program, then we need JDK.
 
#### 2.	What is the basic flow of execution once you write a Java program ?
- The program we write is Java Source Code. Once we write a source code, Java compiler will compile it to Java Byte Code. Then Class Loader verifies this Byte Code and passes to JVM where byte codes will be executed. 
- For example, we have a source code program called Hello.java. Compiler will compile it to Hello.class which is Byte Code. Then class loader will load it and verify it, and pass to JVM where Hello.class will be executed.
 
#### 3.	Why we need main() method ?
- Main method is the entry point that Class Loader looks for. We need main method as starting point so that our program can start executing.
 
#### 4.	Why main() is static ?
- For non static method, we need to create an object so that we can access the method. But Class Loader is not able to create an object and it has to access main method in the beginning of the program. So main method must be static so that Class Loader can access it without creating an object.

#### 5.	What do you mean by static ?
- Static means the variables or methods are available at class level. We don’t have to create an instance of the class to access it. 
- For example, we have a public class called 'Company', and there are two methods which are static method showCompany and non-static method showCompanyAddress. So we can access showCompany directly. But we have to create an object of class Company to access showCompanyAddress.

#### 6.	What is Class ? Give me an example.
- Class is something in general. It is to provide templates to create objects. This template can define variables and methods so that the member of this class can access those variables as state and methods as its behavior.
- The purpose of writing class is to protect our data members which are attributes and methods.
- For example, we have a class called 'Bank' which contains variable bankCode and method showBankCode. Then we create a member called DBS of this class so that DBS will have variable of bankCode and method of showBankCode.
 
#### 7.	What is Object ? Give me an example. 
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
 
#### 10.	Is it possible to write more than one main() method in a class ?
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
 
#### 13.	What is method overriding ? (Polymorphism)
 
#### 14.	What is constructor ?
 
#### 15.	What is association ?
 
#### 16.	What is the purpose of toString() ? 
 
#### 17.	What is Type Casting ? Types of type casting in Java ?

#### 18.	What is inheritance ? What type of inheritance Java supports ?
 
#### 19.	What is advantages of inheritance ?
 
#### 20.	What is super keyword ? Where we use ?

### 21-30
#### 21.	What is abstraction ? What is the purpose of abstraction ?
 
#### 22.	What is abstract class ? Benefits of writing an abstract class ?
 
#### 23.	What is interface ? Benefits of writing an interface ?
 
#### 24.	What is the difference between abstraction and encapsulation ?
 
#### 25.	What is the difference between abstract class and interface ?
 
#### 26.	What is final keyword ?
 
#### 27.	What is anonymous inner class ?
 
#### 28.	What is singleton class ? What is the purpose of writing singleton class ?
 
#### 29.	What is factory design pattern ? What is factory method ?

#### 30.	Can we write a constructor inside abstract class or interface ?

## Mock Test 2

### 1-10
#### 1.	How many data types we have in Java ?

#### 2.	What are access modifiers ?

#### 3.	What is array ? benefits and limitation.

#### 4.	Importance of .equals() and hashCode().

#### 5.	Why we need to handle exception ?

#### 6.	How we handle exception ?

#### 7.	Difference between checked and unchecked exception.

#### 8.	What is the purpose of throw keyword?

#### 9.	Why we need Thread? Different way to create thread.

#### 10.	What is synchronization in thread?

### 11-21
#### 11.	What is the need of Producer and Consumer class in threading?

#### 12.	What is Thread Pool ?

#### 13.	What is volatile keyword ?

#### 14.	What is wrapper class ?

#### 15.	What is purpose of Generics ?

#### 16.	Tell me some interface name and classes in collection framework.

#### 17.	Collection is a class or interface ?

#### 18.	What is Comparable and Comparator interfaces ?

#### 19.	What is serialization in Java ?

#### 20.	What is Marker interface ? What is the purpose ?

#### 21.	What is transient keyword ?

### Database

#### 1.	What is DBMS and RDMBS ?

#### 2.	What is SQL ?

#### 3.	Different type of SQL’s statements ?

#### 4.	What are properties of a transaction ?	(ACID)

#### 5.	What are the different type of normalization ?

#### 6.	What is a primary and Foreign key ?

#### 7.	Define Join and explain different type of joins ?

#### 8.	What is the advantage of stored procedure ?

#### 9.	What is JDBC ?

#### 10.	Types of JDBC Driver ?

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




* auto-gen TOC:
{:toc}
