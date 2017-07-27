# Practical Exercises

## Use these exercises to challenge and practice what you've learned in your lessons.  These may contain features you'd like to implement into your own portfolio.  



## Table of Contents
### [FizzBuzz](#FizzBuzz)
### [HangMan](#HangMan)
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
<a name="HangMan"></a>
# HangMan

```Code
Open your web browser and go to:
repl.it/languages/csharp

/*
 *  C# Program to Create a HangMan Game
 */
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
 
namespace Hangman
{
    class Program
    {
        static void Main(string[] args)
        {
 
            Console.WriteLine("Welcome to Hangman!!!!!!!!!!");
            string[] listwords = new string[10];
            listwords[0] = "sheep";
            listwords[1] = "goat";
            listwords[2] = "computer";
            listwords[3] = "america";
            listwords[4] = "watermelon";
            listwords[5] = "icecream";
            listwords[6] = "jasmine";
            listwords[7] = "pineapple";
            listwords[8] = "orange";
            listwords[9] = "mango";
            Random randGen = new Random();
            var idx = randGen.Next(0, 9);
            string mysteryWord = listwords[idx];
            char[] guess = new char[mysteryWord.Length];
            Console.Write("Please enter your guess: ");
 
            for (int p = 0; p < mysteryWord.Length; p++)
                guess[p] = '*';
 
            while (true)
            {
                char playerGuess = char.Parse(Console.ReadLine());
                for (int j = 0; j < mysteryWord.Length; j++)
                {
                    if (playerGuess == mysteryWord[j])
                        guess[j] = playerGuess;
                }
                Console.WriteLine(guess);
            }
        }
    }
}

```
If you'd like to add a "You Win!" line at the end, use:

```
            while (true)
            {
                char playerGuess = char.Parse(Console.ReadLine());
                for (int j = 0; j < mysteryWord.Length; j++)
                {
                    if (playerGuess == mysteryWord[j])
                        guess[j] = playerGuess;
                }
              Console.WriteLine(guess);
              
              string s = new string(guess);
                
                if (s == mysteryWord) {
                  Console.WriteLine("You win!");
            } 
            }                        
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








