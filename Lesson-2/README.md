# Boolean Logic

Boolean Logic statements (also known as conditional logic) are any kind of logical 
statement that returns a boolean value (true or false value)


# Comparison Operators
Comparison Operators can be used to define boolean variables,
 if-else statements (described below) and while loops (also described below)
 

| Operator              | description                                                                           |
|-----------------------|---------------------------------------------------------------------------------------|
|`==`                   |a double equal is used to compare values (ex. using x from the previous example `x == 4` returns *true* if x is equal to 4)|
|`=`                    |**is not a comparison operator.** a single equal sign is used to **set** a variable to a value (ex. `x = 4` means that *x is 4*)|
|`!=`                   |this combination means does not equal (ex. `x != 3` because `x == 4`)|
|`>`, `<`, `>=`, `<=`   |these symbols act the same way as they do in math (<= is equivalent to ≤ and >= is equivalent to ≥).| 

###### Additional Resources
* https://msdn.microsoft.com/en-us/library/c8f5xwh7.aspx
* https://www.tutorialspoint.com/csharp/csharp_relational_operators.htm

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
###### Additional Resources
* https://msdn.microsoft.com/en-us/library/5011f09h.aspx
* https://www.tutorialspoint.com/csharp/csharp_decision_making.htm

# While loops

A while loop is like an if statement except that the code within the while loop 
will execute over and over again 
until the statement within the parentheses is false

```C#
class MainClass {
  public static void Main (string[] args){ 
      //define an integer called x
      int i = 0;
      while(i < 10){ // Loop through the next 2 lines until i is no longer less than 10
            System.Console.WriteLine("x is equal to " + i);
            i++; //shorthand code equivelent to x = x + 1
      }
      
      while(1==1){ //1 is always equal to 1, tharefore:
            //This creates an infinite loop, the computer will run whatever is in here
            //over and over again until the program is stopped or the computer is shut down
            System.Console.WriteLine("Help i'm stuck in an infinite loop!");
      }
      //Any code below an infinite loop will never be run
      System.Console.WriteLine("This line will never be printed");
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
Notice how `X is 10` is never displayed. 
This is because when x is equal to 10, x is no longer less than 10.
 
if you change the statement within the while loop from 
`while(x<10)` to `while(x <= 10)` then `X is 10` should be 
the last statement displayed

# For Loops
A for loop is a shorthand version of a while loop the example while loop above could be rewritten as:
```C#
class MainClass {
  public static void Main (string[] args){ 
      //define an integer called x
      for(int i=0; i < 10; i++){ // Loop through the next 2 lines until i is no longer less than 10
            System.Console.WriteLine("x is equal to " + i);
      }
  }
}
```
* For loops are usually used for iterating through lists, or for iterating a specific number of times

# Exercises

### Truth Table

given the statement `(A < B)` fill out the answer column for this table

| A value | B value | result (true or false) |
|---------|---------|------------------------|
| 1       | 2       |                        |
| 2       | 1       |                        |
| 10      | 30      |                        |
