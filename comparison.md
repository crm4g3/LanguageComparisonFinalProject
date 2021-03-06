# Cody McIlvaine


# Comparing Java and C#



## Language purpose/genesis

### Java
#### Why was the language created?
+ Java was created to control a variety of day-to-day electronic products.
#### What problems was the language trying to address
+ They were trying to create a more reliable programming language compared to c++ which emphasized speed.
#### Is the language a reaction to a previous language or a replacement for another language?
+ Somewhat of a replacement. Java derives much of its syntax from C and C++
    
### C#
#### Why was the language created?
+ It was developed as a rival to Java. Microsoft didn't want Sun(Oracle) to make changes to Java so they created their own language.
#### What problems was the language trying to address
+ It seems as though C# was created by microsoft to compete against Sun(Oracle)
#### Is the language a reaction to a previous language or a replacement for another language?
+ It was a reaction to the creation of Java.

## Unique features

### Java
+ Java is one of the most used languages for devices around the world.
### C#
+ Properties, Supports interoperability between languages.
    
## Name spaces

### Java
+ In Java namespaces are called packages. Here is and example of importing a package. 
```java
package harding.compsci.graphics;

import graphics.Rectangle;
```
+ Packages are used to easily and logically determine which function are needed for a proper use. Naming is very import in regards to     packages
### C# 
+ Similar to Java namespaces are used to organize classes and to control the scope of classes and methods used in larger programming projects
```csharp
namespace Harding.Compsci.Graphics {
}

using System;
```

## Types

### Java
+ Primitive data types: byte, short, int, long ,float, double, char, boolean
+ Both reference and value types are supported by Java
+ New value types can be created by Java
### C#
+ Primitive data types: bool, byte, sbyte, char, decimal, double, float, int, uint, long, ulong, object, short, ushort, string
+ Both reference and value types are support by C#
+ New value types can be created by C#
    
## Classes
 
### Java
+ Defining a class
 ```java
class Student{
    String Name;
    //Contructor
    public Student(String name){
        this.name = name
    }
}
```
+ Creating a new instance
 ```java
Student newStudent = new Student("John");
```
+ Java's garbage collector handles decontructing, but you can override the finalize function to make your own deconstructor.
 ```java
 protected void finalize() throws Throwable { 
    super.finalize();   // Always call parent's finalizer   
}
```
### C#
+ Defining a class
```csharp
public class Person
{
    private string name;

    // Constructor
    public Person()
    {
        name = "unknown";
    }
    // destructor
    ~Car()
    {
        name = null;
    }
}
```
+ Creating a new instance
```csharp
Person person = new Person();
```
+ C# has a Finalize function used to cleanup unused objects ad as seen above a destructor can be defined within a class.

## Instance reference name in data type (class)
### Java
+ Uses the keyword "this" to reference instance variables.
### C#
+ Also uses the "this" keyword to reference instance variables.

## Properties
### Java
+ Java requires building your own geters and setters and does not have computed properties or backing variables.
### C#
+ C# has built in getters and setters, backing variables, and COmputed properties.
```csharp
public double Hours
   {
       get { return seconds / 3600; }//getter
       set { //setter and computed property
          if (value < 0 || value > 24)
             throw new ArgumentOutOfRangeException(
                   $"{nameof(value)} must be between 0 and 24.");

          seconds = value * 3600; 
       }
   }
```

## Interfaces/Protocols
### Java
+ Java doesnt use protocols.
+ An interface allows a class to become more formal about the behavior it promises to provide.
```java
interface Bicycle {
    void doSomething();
}

class FunBike Implements Bicycle{
    void doSomething();//Must be implemented as that is the point in an interface
}
```
### C#
+ C# doesnt use protocols
+ Can be used to simulate inheritance for structs since they can inherit from other classes or structs.
+ Used to contain definition for a group of related functionalities.
```csharp
interface ISampleInterface
{
    void SampleMethod();
}

class ImplementationClass : ISampleInterface
{
    void ISampleInterface.SampleMethod(){}
}
```

## Inheritance / Extension
### Java
+ Java uses the "extends" keyword for inheritance
 ```java
public class A{}
public class B extends A{}
```
### C#
+ C# uses a ":" for inheritance as shownn below
```csharp
public class A{}
public class B : A{}
```

## Reflection
### Java

### C#

## Memory management
### Java
+ Java memory is divided into two parts. Young generation and Old generation. Young generation is where all new object are created. When young generation is filled garbage collection is performed. This is called minor GC which divides Young Generation into three parts Eden Memory and Survior Memory spaces. Old Generation memory contains objects that are long lived and have survived after many rounds of Minor GC. Similar to the Young Generation, Old Generation performs Major GC.
+ During GC all application threads are stopped.
+ Java does not use automatic reference counting.
### C#
+ Memory is held in an address space called the managed heap. All reference types are allocated here. 
+ Memory is released when the GC determins the best time to perform a collection. It determines which object are no longer being used by examinging the applications roots. Each root either refers to an object on the managed heap or is null. Using this list, it examines an application's roots, and in the process creates a graph that contains all the objects that are reachable from the roots. bjects that are not in the graph are unreachable from the application's roots. The garbage collector considers unreachable objects garbage and will release the memory allocated for them.
+ C# does not use automatic reference counting.

## Comparing values
### Java
 ```java
String name = "john";
if (name == "john")  //Will not work

if (name.equals("john"))   // true
```
### C#
```csharp
string name = "john"; 
if (name == "john")    // true

if (name.Equals("john"))   // true
```

## Null/nil references
+ Both languages use NULL
+ Niether language has special features relating to NULL values

### Errors and exception handling
### Java
 ```java
try {
  y = 0; 
  x = 10 / y;
} catch (Exception ex) {
  System.out.println(ex.getMessage()); 
} finally {

}
```
### C#
```csharp
try {
  y = 0; 
  x = 10 / y;
} catch (Exception ex) {
  Console.WriteLine(ex.Message); 
} finally {

}
```

## Lambda expressions, closures, or functions as types
### Java
+ Java uses Lambda expression to create anonymous methods which are used to implement a method defined by the functional interface.
```java
interface MyGreeting {
	String processName(String str);
}

public static void main(String args[]) {
	MyGreeting morningGreeting = (str) -> "Good Morning " + str + "!";
	MyGreeting eveningGreeting = (str) -> "Good Evening " + str + "!";
  
	System.out.println(morningGreeting.processName("Luis"));
	// Output: Good Morning Luis! 
    
	System.out.println(eveningGreeting.processName("Jessica"));	
    // Output: Good Evening Jessica!
}
```
### C#
+ C# refers to funtion types at delegates.
+ There's also two generic types of delegate types defined in the base class library, one for methods that return a value, and one for those who doesn't, and they come with variations over how many arguments you have.
```csharp
public delegate void DoSomethingDelegate();
DoSomethingDelegate f = DoSomething;
f();
```

## Implementation of listeners
### Java
+ Java has many ways of creating listeners.
+ 1. class must implement ActionListener
+ 2. Register an instance of the class 
+ 3. Include code that implements the methods in listener interface.
```java
public class Beeper ... implements ActionListener {
    ...
    //where initialization occurs:
        button.addActionListener(this);
    ...
    public void actionPerformed(ActionEvent e) {
        ...//Make a beep sound...
    }
}

```
### C#
+ Listeners are available to the Debug, Trace, and TraceSource classes, each of which can send its output to a variety of listener objects.
+ You can define your own listeners by inheriting from the TraceListener base class and overriding its methods with your customized methods. 
## Implementation of event handlers
### Java
+ Javas event handlers and listeners are the same.
### C#
+ Declare the event in your class and then invoke it in the appropriate areas.
```csharp
namespace ImplementInterfaceEvents  
{  
    public interface IDrawingObject  
    {  
        event EventHandler ShapeChanged;  
    }  
    public class MyEventArgs : EventArgs   
    {  
        // class members  
    }  
    public class Shape : IDrawingObject  
    {  
        public event EventHandler ShapeChanged;  
        void ChangeShape()  
        {  
            // Do something here before the event…  

            OnShapeChanged(new MyEventArgs(/*arguments*/));  

            // or do something here after the event.   
        }  
        protected virtual void OnShapeChanged(MyEventArgs e)  
        {  
            if(ShapeChanged != null)  
            {  
               ShapeChanged(this, e);  
            }  
        }  
    }  

}  
```

## Singleton
### Java

### C#





















