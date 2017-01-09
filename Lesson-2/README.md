# Boolean Logic

Boolean Logic statements (also known as conditional logic) are any kind of logical 
statement that returns a boolean value (true or false value)


# Comparison Operators
Comparison Operators can be used to define boolean variables,
 if-else statements (described below) and while loops (also described below)


| Operator        | description                                                                           |
|-----------------|---------------------------------------------------------------------------------------|
|`==`             |a double equal is used to compare values (ex. using x from the previous example `x == 4` returns *true* if x is equal to 4)|
|`=`              |**is not a comparison operator.** a single equal sign is used to confirm a variables meaning (ex. `x = 4` means that *x is 4*)|
|`!=`             |this combination means does not equal (ex. `x != 3` because `x == 4`)|
|`>, <, >=, <=`   |these symbols act the same way as they do in math (<= is equivalent to ≤ and >= is equivalent to ≥).| 

###### Additional Resources
* https://msdn.microsoft.com/en-us/library/c8f5xwh7.aspx

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
      }
  }
}
```
