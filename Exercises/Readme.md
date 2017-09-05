# Practical Exercises

## Use these exercises to challenge and practice what you've learned in your lessons.  These may contain features you'd like to implement into your own portfolio.  



## Table of Contents
### [FizzBuzz](#FizzBuzz)
### [HangMan](#HangMan)
### [Bubble Sort](#numbersort)
### [Username and Password](#username-and-password-1)
### [Draw an X](#drawX)
### [Recursion: Decimal to Binary](#decbin)
### [Dimensions](#dim)
### [DayofWeek](#dayweek)
### [New File](#NewFile)
### [Windows Forms 101](#winforms1)


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

<a name="drawX"></a>
# Draw an X Using Asterisks *

```C#
using System;  
public class Exercise81
{  
    public static void Main()
        {
    int row,column; 
   
    Console.Write("\n\n");
    Console.Write("Display the pattern like 'X' with an asterisk:\n");
    Console.Write("---------------------------------------------");
    Console.Write("\n\n");   
 
   for(row=0;row<=6;row++)
        {
         for (column=0; column<=6; column++)
            {
            if (((column == 1 || column == 5) && (row > 4 || row < 2)) || row == column && column > 0 && column < 6 || (column == 2 && row == 4) || (column == 4 && row == 2))
            Console.Write("*");
             else
              Console.Write(" ");
            }
            Console.Write("\n");
        }
	Console.Write("\n");
   }
}
```


***
<a name="decbin"></a>
# Recursion: Decimal to Binary

```C#
using System;

class RecExercise13
{
    public static void Main(string[] args)
    {
        int num;
        DecToBinClass pg = new DecToBinClass();
		Console.WriteLine("\n\n Recursion : Convert a decimal number to binary :");
		Console.WriteLine("------------------------------------------------------"); 
        Console.Write(" Input a decimal number : ");
        num = int.Parse(Console.ReadLine());
        Console.Write(" The binary equivalent of {0} is : ", num);
        pg.deciToBinary (num);
        Console.ReadLine();
        Console.Write("\n");
    }
}
public class DecToBinClass
{
    public int deciToBinary(int num)
    {
        int bin;
        if (num != 0)
        {
            bin = (num % 2) + 10 * deciToBinary(num / 2);
            Console.Write(bin);
            return 0;
        }
        else
        {
            return 0;
        }
 
    }
}
```


***
<a name="dim"></a>
# Dimensions

```C#
using System;

public struct sampStru
{
    private double val;
    public double Value
    {
        get { return val; }
        set { val = value; }
    }
    public double Read()
    {
        return double.Parse(Console.ReadLine());
    }
}
public struct Square
{
    sampStru ln;
    sampStru ht;

    public sampStru Length
    {
        get { return ln; }
        set { ln = value; }
    }
    public sampStru Width
    {
        get { return ht; }
        set { ht = value; }
    }
    public void newSquare()
    {
        sampStru rct = new sampStru();

        Console.WriteLine("\nInput the dimensions: ");
        ln = sqrLength();
        Console.Write("width : ");
        ht.Value = rct.Read();
    }
    public sampStru sqrLength()
    {
        sampStru rct = new sampStru();

        Console.Write("length : ");
        rct.Value = rct.Read();
        return rct;
    }
}
public class strucExer10
{
    static void Main()
    {
		Console.Write("\n\nMethod that returns a structure  :\n");
		Console.Write("--------------------------------------\n");
        var Sqre = new Square();
        Sqre.newSquare();
        Console.WriteLine();
        Console.WriteLine("Perimeter and Area:");
        Console.WriteLine("Length:    {0}", Sqre.Length.Value);
        Console.WriteLine("Width:    {0}", Sqre.Width.Value);
        Console.WriteLine("Perimeter: {0}", (Sqre.Length.Value + Sqre.Width.Value) * 2);
        Console.WriteLine("Area:      {0}\n", Sqre.Length.Value * Sqre.Width.Value);
    }
}

```


***
<a name="dayweek"></a>
# Day of the Week

```C#
using System;

class dttimeex57
{
    static void Main()
    {
        int yr,mn,dt;
        
    Console.Write("\n\n Find the day for a given date :\n");
	Console.Write("------------------------------------\n");        
        
    Console.Write(" Input the Month : ");
    mn = Convert.ToInt32(Console.ReadLine());	
	Console.Write(" Input the Day : ");
    dt = Convert.ToInt32(Console.ReadLine());	
    Console.Write(" Input the Year : ");
    yr = Convert.ToInt32(Console.ReadLine());		
	DateTime d = new DateTime(yr, mn, dt);
	Console.WriteLine(" The formatted Date is : {0}",d.ToString("MM/dd/yyyy"));	
	DateTime pp;
    pp=DayOfWeek(d);
	Console.WriteLine(" The day for the date is : {0}\n ",pp.DayOfWeek);
    }
    public static DateTime DayOfWeek(DateTime dt)
    {
        DateTime ss= new DateTime(dt.Year, dt.Month, dt.Day);
        return ss;
    }    
}
```


***
<a name="NewFile"></a>
# New File

Create as CONSOLE APPLICATION in VISUAL STUDIO
(File - New - Project - Console Application)

```C#
using System;
using System.IO;
using System.Text;

class filexercise2
{
    public static void Main()
    {
        string fileName = @"mytest.txt";

        try
        {
            // Delete the file if it exists.
            if (File.Exists(fileName))
            {
                File.Delete(fileName);
            }
			Console.Write("\n\n Create a file with content in the disk :\n");
			Console.Write("---------------------------------------------\n");            
            // Create the file.
            using (StreamWriter fileStr = File.CreateText(fileName)) 
            {
                fileStr.WriteLine(" Hello and Welcome");
                fileStr.WriteLine(" It is the first content");
                fileStr.WriteLine(" of the text file mytest.txt");
				 Console.WriteLine(" A file created with content name mytest.txt\n\n");
            }	            			
        }
        catch (Exception MyExcep)
        {
            Console.WriteLine(MyExcep.ToString());
        }
    }
}

```

Check your Visual Studio folder for the .txt file:

C:\Users\Student\Documents\Visual Studio 2015\Projects\ConsoleApplication3\ConsoleApplication3\bin\Debug

***
<a name="winforms1"></a>
# Windows Forms 101
File - New - Project -> Windows Forms

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










