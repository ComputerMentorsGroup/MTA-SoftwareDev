# Lesson 3: Object Oriented Programming (OOP)

**Make sure you have finished the SWITCH STATEMENT EXERCISE (New!!) at the end of Lesson 2 before proceeding!**

### Important Terms:
Pay close attention to these terms throughout the lesson:
* Class
* Constructor
* Encapsulation
* Inheritance
* Method
* Objects
* Polymorphism


# Exercise
1. Open Microsoft Visural Studion
2. Begin a New Console Application Project
3. Add a new Visual C# **CLASS** named Rectangle to the project.
4. Replace the code for the Rectangle class as follows.
5. Build (F5) to ensure there are no errors.
6. Keep the project open.
```C#
class Rectangle
{
   private double length;
   private double width;
   
   public Rectangle(double l, double w)
   {
   length = l;
   width = w;
   }
   
   public double GetArea()
   {
      return length * width;
   }
}
```

### A **CLASS** is a template that can be reused over and over again to create objects.

* The class you created is named Rectangle.
* The Rectangle class has two data fields: length and width
* This class also defines a **METHOD** named GetArea --> Read on!

### A **METHOD** defines actions and operations supported by a class. 
* The Method is defined like so: access level, data type to "return", and the name of the method
`public double GetArea()`
* With our example, GetArea method has a *public* **access level**, a *double* data type, the method name is GetArea, the parameters are empty (there's nothing in the parenthesis!), and the block of code which executes is a single return statement.
* If the method does not intend to return a value it may say **void** instead of specifying a data type.
* The method must use a **return** statement, which executes the method and terminates right after it is done.



# Exercise

Modify the code of your Program class from the previous exercise using the code below.
**The code below creates a rect object with given dimensions (5.0 and 10.0), then uses the method you previously defined to find the area of the object (rectangle).  It then prints the area to the console.**

```C#
class Program
{
static void Main(string[] args)
   {
   Rectangle rect = new Rectangle(5.0, 10.0);
   double area = rect.GetArea();
   Console.WriteLine("area of Rectangle: {0}", area);
   }
}
```
**Press F5 and Save your project. Keep the project open.**




In this line you've created an object:


`Rectangle rect = new Rectangle(5.0, 10.0);`



| Class | Object Name | New Object | Constructor |
| --- | --- | ---  | --- |
| Rectangle | rect | new | Rectangle(5.0, 10.0); |



Here we are calling a **CONSTRUCTOR** with two arguments:
(5.0 and 10.0); 
Which are using the *double* data type (they are decimals!)


We create the **OBJECT** by using the *new* keyword followed by the class **CONSTRUCTOR**:
**new Rectangle(5.0, 10.0);**



**OBJECTS** are created from templates defined by classes.

A **CONSTRUCTOR** is a class method that is executed when a new instance of a class is created.  It initializes the data within an object (5.0 and 10.0 in the example).
* Constructors always have the same exact name as the class.
* Constructors do not need to have a return data type
* Multiple constructors can be defined for a class


***

### More Concepts: 

When the code executes, an object of Rectangle type is created in **HEAP** memory (like a heap of laundry!).  A reference to this memory is stored inside the variable rect, and the variable rect is stored in **STACK** memory - a fast memory that is queued in the computer's RAM.


More on this concept here:


*"The Stack is self-maintaining, meaning that it basically takes care of its own memory management.  When the top box is no longer used, it's thrown out.  The Heap, on the other hand, must worry about Garbage collection (GC), which deals with how to keep the Heap clean (no one wants dirty laundry laying around, it stinks!)."
Source: http://www.c-sharpcorner.com/article/C-Sharp-heaping-vs-stacking-in-net-part-i/*


***

# Exercise

1. Use the project you saved in the previous task.
2. Modify the code of the Rectangle class:


```C#
class Rectangle {
   private double length;
   private double width;
   private double Length;
}

   get
     { 
     return length;
     }
     set
     {
     if (value > 0.0)
     length = value;
     }
 }
 public double Width
 {
   get
   {
      return width;
   }
   set
   {
   if (value > 0.0)
   width = value;
   }
}

   public double GetArea()
   {
   return length * width
   }
}
```


3. Now modify the code within the Program class:


```C#
class Program
{
static void Main(string[] args)
{
   Rectangle rect = new Rectangle();
   rect.Length = 5.0;
   rect.Width = 10.0;
   double area = rect.GetArea();
   Console.WriteLine(
      "Area of Rectangle: {0}", area);
   }
}

```

4. Save your project.



**In this exercise you modified the Rectangle class to have Length and Width properties.**  Properties are defined using a public access modifier.  Notice in your code the values for length and width cannot be negative.



**PROPERTIES** are class members that can be accessed like data, but contain code like a method.  Properties expose the data of a class in a more controlled manner.  For example, private data can be exposed using a public property.

A property has two **accessors**: *GET* and *SET*

**GET** is used to return the property value.  If you do not include a GET accessor then the property will have a write-only property.

**SET** is used to assign a new value to a property.  If you do not include a SET accessor then the property will be read-only.

Properties are usually *public* and should begin with a capital letter (Length, Width).  *Private fields are always lower-case.*



***


### Research:  Let's say you have a class named Widget.  Chances are, another company will also ship code that contains a class named Widget.  How do you handle the ambiguity in names?

Answer:  Organize your code into a **NAMESPACE**  for example:
 
`` namespace NewCompany
 {
   public class Widget { 
   ... 
   }
}

and

namespace YourCompany 
   {
   public class Widget {
   ...
   }
}
``

***
