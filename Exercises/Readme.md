# Practical Exercises

## Use these exercises to challenge and practice what you've learned in your lessons.  These may contain features you'd like to implement into your own portfolio.  



## Table of Contents
### [FizzBuzz](#FizzBuzz)
### [HangMan](#HangMan)
### [Bubble Sort](#numbersort)
### [Username and Password](#username-and-password-1)


***
<a name="FizzBuzz"></a>
# FizzBuzz
Below is a simple program that prints out a sequence of numbers from 0 - 100. Except every time it hits a number which is a multiple of 3 it prints out "Fizz" and if it hits a multiple of 5 it prints out "Buzz" and if its a multiple of both it prints out "FizzBuzz".

```C#
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
There are multiple ways of completing the FizzBuzz program. Take some time and experiment on the differnt ways you can complete it, such as using a While loop or a do While loop. Or you can even try using another method insted of the main method.

```C#
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

```C#
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

```C#
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
You will also want to add code to prevent the app from crashing when the player/user adds more than one character. Now would be a good time to search and research Try-Catch-Finally statements.
https://msdn.microsoft.com/en-us/library/0yd65esw(v=vs.90).aspx

```C#
try{

} catch {

}finally{

}

```

Next try adding code that allows the player to finish that word without typing out every letter individually. Try using if statements.
https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/if-else

```C#
if(){

}

```
It also wouldn't hurt to ask the player if they’d like to play again.


```
            

```
The current array is fine but let’s future proof it a bit and set the list to and word bank to expand automatically.
https://msdn.microsoft.com/en-us/library/aa288453(v=vs.71).aspx
```C#
int[] numbers = new int[] {1, 2, 3, 4, 5};
```

Bellow is a ASCII art hangman if you want to add it to your game.
```C#
public static void HangMan(int tries) {

			string hangedMan = "____\n     |";

			if (tries == 5) {
				hangedMan = "____\n     |\n     O";
			} else if (tries == 4) {
				hangedMan = "____\n     |\n     O\n     |\n     |";
			} else if (tries == 3) {
				hangedMan = "____\n     |\n     O\n    /|\n     |";
			} else if (tries == 2) {
				hangedMan = "____\n     |\n     O\n    /|\\ \n     |";
			} else if (tries == 1) {
				hangedMan = "____\n     |\n     O\n    /|\\ \n     |\n    /\n";
			} else if (tries == 0) {
				hangedMan = "____\n     |\n     O\n    /|\\ \n     |\n    / \\\n";		
			}
			Console.Write(hangedMan);

		}
```

***
<a name="numbersort"></a>
# Bubble Sorting

```C#
using System; 
public class Bubble_Sort  
{  
   public static void Main(string[] args)
         { 
            int[] a = { 3, 0, 2, 5, -1, 4, 1 }; 
			int t; 
			Console.WriteLine("Original array :");
            foreach (int aa in a)                       
            Console.Write(aa + " ");                     
            for (int p = 0; p <= a.Length - 2; p++)
            {
                for (int i = 0; i <= a.Length - 2; i++)
                {
                    if (a[i] > a[i + 1])
                    {
                        t = a[i + 1];
                        a[i + 1] = a[i];
                        a[i] = t;
                    }
                } 
            }
            Console.WriteLine("\n"+"Sorted array :");
            foreach (int aa in a)                       
            Console.Write(aa + " ");
			Console.Write("\n"); 
            
        }
}

```


***


<a name="username-and-password"></a>
# Username and Password

```C#
using System;
public class Exercise16
{
    public static void Main()
    {
       string username, password;
       int ctr = 0;
       Console.Write("\n\nCheck username and password :\n");
	   Console.Write("Note: Default user name and password is :abcd and 1234\n");
       Console.Write("------------------------------------------------------\n"); 
         
        do
        {
			Console.Write("Input a username: ");
			username = Console.ReadLine();
 
			Console.Write("Input a password: ");
			password = Console.ReadLine();
			
             if(username != "abcd" || password != "1234")
             ctr++;
             else
             ctr=1;
     
        }
        while((username != "abcd" || password != "1234")  && (ctr != 3));
	 
        if (ctr == 3)
            Console.Write("\nLogin attemp three or more times. Try later!\n\n");
        else   
            Console.Write("\nThe password entered successfully!\n\n");		
    }
}
```


***

<a name="linkname"></a>
# Title

```C#

```


***
<a name="linkname"></a>
# Title

```C#

```


***
<a name="linkname"></a>
# Title

```C#

```


***
<a name="linkname"></a>
# Title

```C#

```


***
<a name="linkname"></a>
# Title

```C#

```


***
<a name="linkname"></a>
# Title

```C#

```


***
<a name="linkname"></a>
# Title

```C#

```


***
<a name="linkname"></a>
# Title

```C#

```


***










