# Getting Started

C# Is a programming language based on C, Java, and a few other common languages. 
The most basic C# Application will look like this:


```C#
class MainClass {
  public static void Main (string[] args){ 
      // code that you want to run goes here
      // Each line between these two curly brackets is executed (run) one at a time from top to bottom
      
      //The line below will print (display) hello world on the console that appears when you run this program
      System.Console.WriteLine("Hello World");
  }
}
```
## Details
This is whats known as a Console Application. Lets break this program down a lot. 
it looks like a lot of code, but all this program does is
display the words "Hello World" in the console that shows up when you run this program.

* `class MainClass {`
    * This line defines a Class, we will explain later what classes are about. 
    For now, just know that every program must start with something like this
    * The Curly Bracket at the end of this line defines the beginning of a block of code
    that will describe what this class does
* `public static void Main(string[] args){`
    * This is the Main function. A function is a named block of code that can be called upon at
    any time while the program is running. The Main function is the starting point for the
    entire program. 
* Any line starting with `//` is known as a comment.
    * Comments are ignored by the computer, but can be used to
        * document code
        * disable code without deleting it (just add `//` to the beginning of any line to disable it)
        * keep notes about what needs to be done next (begin comment with TODO: )
* `System.Console.WriteLine("Hello World");`
    * This line writes a *string* of text to the system console
    * `System` is the Namespace that the console is defined in 
    (we will explain more about what namespaces are later)
    * `Console` is the class that defines the functionality of the Console that is displayed
    when this program starts 
    * `WriteLine` is the *function (also sometimes known as a method)* that tells the program how to write to the console
    * Never forget the Semicolon: `;`
        * A semicolon defines the end of a line of code. If the line does not end with a curly bracket,
        it should always end with a semicolon. 
        * **This is a very important rule in C#**
* The next two `}` Curly brackets end the Main function code block and then the MainClass code block
    * **Any Every opening curly bracket `{` must end with a closing bracket `}`. This is a rule in C# with no exceptions!**
    
# Exercise

Using https://repl.it/languages/csharp or Visual Studio Community,
Change the program above to print "Goodbye world" to the console instead of Hello World.


# Variables

In programming, variables are used to hold values. 
The value of a variable can be a number or an object such as a String of text or something else that you define.
Variable can be used for:
* Organizing code
* Storing user input
* Managing the current state of the program (more details later)

# Most Common Types

* int - holds interger values (i.e. whole numbers)
* float - holds floating point values (i.e. decimal values) 4 bytes sized.
* double - holds larger decimal values (twice as large as float)
* bool - holds either true or false (boolean values)
* char - holds only one character
* string - holds a series of characters (text)
An `=` symbol sets the value of the variable to the value specified on the right hand side of the symbol. For example:
```C#
int y = 100 / 2; // y will equal 50 because math
string name = "Alex"; // Double quotes for string
char first = 'A'; // Single quotes for char
bool v = true; // can only be true or false
long x = 2;
long l = x * 2; //will equal 4 because x was set to 2
float f = 3.55555f; // You must put the f in front of the number or the program will assume its a double (causing an error).
double d = 4.9999999; // Double is the defualt floating type varible so it doesn't need a clarification lice decimal and float.
```
# Variable naming
* Can contain uppercase and lowercase letters, numbers, and underscores.
* CANNOT start with a number or contain spaces
* Names are case sensitive.
* Should start with a lowercase letter but is not mandatory.
    * It is common practice to define variables with lowerCamelCaseNames meaning the first word is lower case and all proceeding 
words are upperCase
```C#
string firstName = "Alex"; // is allowed
string LastName = "Jones"; // is allowed but not a recommended naming standard
string 1stName = "Barbra"; // this name is not allowed
string iAmNumber1 = "Ann"; // this is allowed
```

# Other Types
* double - holds floating point values. 8 bytes sized
* decimal - holds floating point values. 16 bytes sized. Optimal for financial and monateray calculations as it has higher precision.
* byte - holds small interger values from 0 - 255.
* sbyte - signed byte, holds interger values from -128 to 127.
* unit - holds only positive interger values.
* long - Same as an interger but is bigger.
* ulong - unsigned long, same as long but only holds positive values.
* short - holds small interger values from -32,768 to 32,767.
* ushort - unsigned short, same as short but only holds positive numbers

# Exercise 

Using https://repl.it/languages/csharp or Visual Studio Community,
Write a program that calculates the area of a rectangle with a height of 13 and a width of 48.2

