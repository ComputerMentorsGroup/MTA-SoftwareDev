# Comparison Opperaters
* = - a single equal sign is used to confirm a varibles meaning (ex. x = 4 means that x is 4)
* == - a double equal is used to compare values (ex. using x from the previous example x == 4)
* != - this combination means does not equal (ex. x != 3 because x == 4)
* >, <, >=, <= - these symbols act the same way as they don in math.

# If-Else Statments

An if statment allows you to check if a value is true or false. If the value is true the code in the if else statement will activate. Other wise the code wont.

```C#
class MainClass {
  public static void Main (string[] args){ 
      if(2 + 2 == 4){
         // because 2+2 = 4 the code is true and will print out the line bellow.
         System.Console.WriteLine("Hello World");
      }
      
      if(2 + 2 != 4){
         // because 2+2 = 4 the code is false and will not print
         System.Console.WriteLine("Hello World");
      }
  }
}
```
