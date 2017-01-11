# If-Else Statements

An if statement allows you to check if a value is true or false. If the value is true the code in the if else statement will execute (run). Other wise the code will be skipped.

```C#
class MainClass {
  public static void Main (string[] args){ 
      if(2 + 2 == 4){
         // because 2+2 = 4 the code is true and will print out the line bellow.
         System.Console.WriteLine("2 plus 2 is equal to 4");
      }
      
      if(2 + 2 != 4){
         // because 2+2 = 4 the code is false the line below will not be run
         System.Console.WriteLine("2 plus 2 is not equal to 4");
      } else { //else is an optional addition to if statements
         // Code between these brackets will only be run if the above statement is false
         System.Console.WriteLine("2 plus 2 is equal to 4");
      }
  }
}
```