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



When the code executes, an object of Rectangle type is created in **HEAP** memory.  A reference to this memory is stored inside the variable rect, and the variable rect is stored in **STACK** memory - a fast memory that resides in the computer's RAM.
