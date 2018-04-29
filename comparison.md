# This should be in markdown
## This should be in markdown
### This should be in markdown

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
import graphics.Rectangle;
```
+ Packages are used to easily and logically determine which function are needed for a proper use. Naming is very import in regards to     packages
### C# 
+ Similar to Java namespaces are used to organize classes and to control the scope of classes and methods used in larger programming projects
```csharp
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
class Student(){
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
+ Java's garbage collector handles decontructing. There isn't a way to manually deconstruct an object in Java
### C#
