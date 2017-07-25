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


