# Practical Exercises

## Use these exercises to challenge and practice what you've learned in your lessons.  These may contain features you'd like to implement into your own portfolio.  



## Table of Contents
### [FizzBuzz](#FizzBuzz)
### [Name](#shortname)
### [Name](#shortname)
### [Name](#shortname)


***
<a name="FizzBuzz"></a>
# FizzBuzz
Bellow is a simple program that prints out a sequence of numbers from 0 - 100. Except every time it hits a number which is a multiple of 3 it prints out "Fizz" and if it hits a multiple of 5 it prints out "Buzz" and if its a multiple of both it prints out "FizzBuzz".
```Code
using System;
class MainClass {
  public static void Main (string[] args) {
    for(int i = 0; i <= 100; i++){
      if(i % 15 == 0){
        Console.WriteLine ("FizzBuzz");
      } else if (i % 5 == 0){
        Console.WriteLine ("Buzz");
      } else if(i % 3 == 0){
        Console.WriteLine ("Fizz");
      } else{
        Console.WriteLine (i);
      }
    }
    
  }
}
```
There are multiple ways of completing the FizzBuzz program. Take some time and experiment on the differnt ways you can complete it, such as using a While loop or a do While loop. Or you can even try using another method insted of the main methode.

```Code
using System;
class MainClass {
  public static void FizzBuzz(){
    for(int i = 0; i <= 100; i++){
      if(i % 15 == 0){
        Console.WriteLine ("FizzBuzz");
      } else if (i % 5 == 0){
        Console.WriteLine ("Buzz");
      } else if(i % 3 == 0){
        Console.WriteLine ("Fizz");
      } else{
        Console.WriteLine (i);
      }
    }
  }
  
  public static void Main (string[] args) {
    FizzBuzz();
    }
    
  }
}
```

***
<a name="shortname"></a>
# Name

```Code
code goes here
```


***
<a name="shortname"></a>
# Name

```Code
code goes here
```


***








