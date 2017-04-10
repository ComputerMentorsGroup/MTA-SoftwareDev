# Lesson 3

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

## Details

* `Console.Title = "Input";`
    * This names the Console Application "Input"
* `Console.Write("Please Enter Your Name");`
    * Prints the statement between "s to the Console Window
* `string name = Console.ReadLine();`
    * Whatever the user inputs is read by the console as a **string** with the variable **name**
    
    
Now let's add a few lines to this!


    
```C#
Console.Title = "Input";

Console.Write("Please Enter Your Name: ");
string name = Console.ReadLine();

Console.WriteLine("Welcome " + name + "!");
Console.ReadKey();

```
## Details
* `Console.WriteLine("Welcome " + name + "!");`
  * The console will print whatever is stored in the variable **name**
* `Console.ReadKey();`
  * This statement calls upon the ReadKey method of the Console class to wait for any key to be pressed (Press Any Key to Continue)
    https://www.youtube.com/watch?v=st6-DgWeuos
    
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
## Details
* `Console.WriteLine("What year were you born?");`
  * First the computer asks us for the year born. The Chinese Zodiac is based off the year you were born.
* `int birthYr = Convert.ToInt32(Console.ReadLine());`
  * We must establish a variable name of **birthYr** with the data type **integer** or int.  In this line we convert anything the user types into the console as an integer.  
* `int findZodiac = (birthYr - 3) % 12;`
   * Remaining with the integer datatype, we have another variable that stores the result of two mathematical operations: subtraction and modulus.  Modulus stores or displays the REMAINDER after division is done.  For example, 5/2 is 2 remainder 1.  You could say 5/2 is 2.5, however, we only want to use integers to determine the chinese zodiac (no decimals or fractions!).  You will see why in a following code snippet.
* `string zodiac;`
   * We must define the variable which will display your zodiac name.  We call this a string because it outputs text.
   
`switch (findZodiac)`
`            `{`
`               `case 1: zodiac = "rat"; break;`
                `case 2: zodiac = "ox"; break;`
                `case 3: zodiac = "tiger"; break;`
                `case 4: zodiac = "rabbit"; break;`
                `case 5: zodiac = "dragon"; break;`
                `case 6: zodiac = "snake"; break;`
                `case 7: zodiac = "horse"; break;`
                `case 8: zodiac = "goat"; break;`
                `case 9: zodiac = "monkey"; break;`
                `case 10: zodiac = "rooster"; break;`
                `case 11: zodiac = "dog"; break;`
                `case 12: zodiac = "pig"; break;`
                `default: zodiac = "I don't know!"; break;`
            `}`
```

Here's the meat of our program.  The REMAINDER (or modulus) will be checked against each INTEGER next to **case**.  
When a match if found, the program "breaks" and stores the zodiac string where the break-out occured.
            
* `Console.WriteLine("Your Chinese Zodiac is the sign of the " + zodiac);`
   * Here we print out the zodiac string that was stored in the previous step.

   
