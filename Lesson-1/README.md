#Getting Started

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

Change the program above to print "Goodbye world" to the console instead of Hello World.