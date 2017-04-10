# While loops

A while loop is like an if statement except that the code within the while loop 
will execute over and over again 
until the statement within the parentheses is false.
```C#
class MainClass {
  public static void Main (string[] args){ 
      //define an integer called i
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

You can learn more about conditional expressions [here](https://github.com/ComputerMentorsGroup/MTA-SoftwareDev/tree/master/Lesson-2#comparison-operators). 


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

# Details



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

## More lines!
Modify the program below to output 100 lines instead of 10
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

## One more line
How could you modify the program above to output just one more line without changing any of the integers already in the program?

## For loops

Modify the example below to use a for loop instead of a while loop

```C#
class MainClass {
  public static void Main (string[] args){ 
      //define an integer called i
      int i = 0;
      while(i < 10){ // Loop through the next 2 lines until i is no longer less than 10
            System.Console.WriteLine("x is equal to " + i);
            i++; //shorthand code equivelent to x = x + 1
      }
  }
}
```
