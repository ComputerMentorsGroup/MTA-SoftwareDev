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

# While loops

A while loop is like an if statement except that the code within the while loop 
will execute over and over again 
until the statement within the parentheses is false

```C#
class MainClass {
  public static void Main (string[] args){ 
      //define and integer called x
      int x = 0;
      while(x < 10){ // Loop through the next 2 lines until x is no longer less than 10
            System.Console.WriteLine("x is equal to " + x);
            x++; //shorthand code equivelent to x = x + 1
      }
  }
}
```
the output of this program if run should be 
```
X is 0
X is 1
X is 2
X is 3
X is 4
X is 5
X is 6
X is 7
X is 8
X is 9
```
Notice how `X is 10` is never displayed. This is because when x is equal to 10, x is no longer less than 10, 
if you change the statement within the while loop from `while(x<10)` to `while(x <= 10)` then `X is 10` should be the last statement displayed