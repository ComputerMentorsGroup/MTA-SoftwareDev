# Boolean Logic

Boolean Logic expressions (also known as conditional expressions or statements) are any kind of logical 
statement that returns a boolean value (true or false value)


# Comparison Operators
Comparison Operators can be used to define boolean variables by comparing any two numbers (or strings in some cases),
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

# Exercise

### Truth Table

given the statement `(A < B)` fill out the answer column for this table

| A value | B value | result (true or false) |
|---------|---------|------------------------|
| 1       | 2       |                        |
| 2       | 1       |                        |
| 10      | 30      |                        |




# Switch Statements

In this lesson you will create a console application that can receive input and respond with information.

Writing your first program:

1. Open Microsoft Visual Studio
2. Create a New Project
3. Choose Windows - Console Application
4. Name the project Input
5. Position the cursor between the { } (curly brackets) of the Main() method and type the code below.
6. Press F5 when completed to see the results.

```C#
Console.Title = "Input";

Console.Write("Please Enter Your Name: ");
string name = Console.ReadLine();

```

* `Console.Title = "Input";`
    * This names the Console Application "Input"
* `Console.Write("Please Enter Your Name");`
    * Prints the statement between "s to the Console Window
* `string name = Console.ReadLine();`
    * Whatever the user inputs is read by the console as a **string** with the variable **name**
    
    
# Exercise

Now let's add a few lines to this!


    
```C#
Console.Title = "Input";

Console.Write("Please Enter Your Name: ");
string name = Console.ReadLine();

Console.WriteLine("Welcome " + name + "!");
Console.ReadKey();

```

* `Console.WriteLine("Welcome " + name + "!");`
  * The console will print whatever is stored in the variable **name**
* `Console.ReadKey();`
  * This statement calls upon the ReadKey method of the Console class to wait for any key to be pressed (Press Any Key to Continue)
    https://www.youtube.com/watch?v=st6-DgWeuos
    

# Exercise 

Next, we're going to modify this program to calculate our Chinese Zodiac!
    
```C#
Console.Title = "Input";
     
                        Console.Write("Please Enter Your Name: ");
            string name = Console.ReadLine();

            Console.WriteLine("Welcome " + name + "!");

            Console.WriteLine("What year were you born?");
            int birthYr = Convert.ToInt32(Console.ReadLine());
            int findZodiac = (birthYr - 3) % 12;

            string zodiac;

            switch (findZodiac)
            {
                case 1: zodiac = "rat"; break;
                case 2: zodiac = "ox"; break;
                case 3: zodiac = "tiger"; break;
                case 4: zodiac = "rabbit"; break;
                case 5: zodiac = "dragon"; break;
                case 6: zodiac = "snake"; break;
                case 7: zodiac = "horse"; break;
                case 8: zodiac = "goat"; break;
                case 9: zodiac = "monkey"; break;
                case 10: zodiac = "rooster"; break;
                case 11: zodiac = "dog"; break;
                case 12: zodiac = "pig"; break;
                default: zodiac = "I don't know!"; break;
            }

            Console.WriteLine("Your Chinese Zodiac is the sign of the " + zodiac);
            
            Console.ReadKey();

```

* `Console.WriteLine("What year were you born?");`
  * First the computer asks us for the year born. The Chinese Zodiac is based off the year you were born.
* `int birthYr = Convert.ToInt32(Console.ReadLine());`
  * We must establish a variable name of **birthYr** with the data type **integer** or int.  In this line we convert anything the user types into the console as an integer.  
* `int findZodiac = (birthYr - 3) % 12;`
   * Remaining with the integer datatype, we have another variable that stores the result of two mathematical operations: subtraction and modulus.  Modulus stores or displays the REMAINDER after division is done.  For example, 5/2 is 2 remainder 1.  You could say 5/2 is 2.5, however, we only want to use integers to determine the chinese zodiac (no decimals or fractions!).  You will see why in a following code snippet.
* `string zodiac;`
   * We must define the variable which will display your zodiac name.  We call this a string because it outputs text.

```C#
 switch (findZodiac)
            {
                case 1: zodiac = "rat"; break;
                case 2: zodiac = "ox"; break;
                case 3: zodiac = "tiger"; break;
                case 4: zodiac = "rabbit"; break;
                case 5: zodiac = "dragon"; break;
                case 6: zodiac = "snake"; break;
                case 7: zodiac = "horse"; break;
                case 8: zodiac = "goat"; break;
                case 9: zodiac = "monkey"; break;
                case 10: zodiac = "rooster"; break;
                case 11: zodiac = "dog"; break;
                case 12: zodiac = "pig"; break;
                default: zodiac = "I don't know!"; break;
            }
```

* Here's the meat of our program: The SWITCH statement.  The REMAINDER (or modulus) will be checked against each CASE INTEGER (the whole number next to **case**).  
   * When a match is found, the program "breaks" and stores the zodiac string where the break-out occured.
            
* `Console.WriteLine("Your Chinese Zodiac is the sign of the " + zodiac);`
   * Here we print out the zodiac string that was stored in the previous step.


### Research: When would you use a Switch Statement rather than an If/Else Statement?
### Challenge: Create another Switch Statement Application.  Your application should receive an integer input and correctly print a corresponding statement/answer from within a switch.
   

