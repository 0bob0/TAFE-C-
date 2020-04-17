# C# Tafe Course
Written by Brook Jeynes and Robert MacKenzie
<br>

<h1>Table of Contents</h1>
<ul>
  <li><a href="#first-project">First Project - getting started</a></li>
  <ul>
    <li><a href="#creating-first-project">Creating your first project</a></li>
    <li><a href="#namespaces">Namespaces</a></li>
    <li><a href="#classes">Classes intro</a></li>
    <li><a href="#methods">Methods intro</a></li>
    <li><a href="#printing">Printing to the command line</a></li>
    <li><a href="#project1">Project 1</a></li>
  </ul>
<li><a href="#second-project">Data Types, variables and sequence</a></li>
<ul>
    <li><a href="#datatypes">Data types</a></li>
    <li><a href="#typeconversion">Type conversion</a></li>
    <li><a href="#variables">Variables</a></li>
    <li><a href="#operators">Operators</a></li>
    <li><a href="#sequence">Sequence</a></li>
    <li><a href="#comments">Comments</a></li>
    <li><a href="#PseudoCode">Pseudo Code</a></li>
    <li><a href="#project2">TASK - Project 2</a></li>
  </ul>
<li><a href="#third-project">Decisions</a></li>
<ul>
    <li><a href="#if">if</a></li>
    <li><a href="#ifelse">If Else</a></li>
    <li><a href="#switch">Switch</a></li>
    <li><a href="#project3">TASK - Project 3</a></li>
  </ul>
<li><a href="#fourth-project">Loops</a></li>
<ul>
    <li><a href="#While">While</a></li>
    <li><a href="#doWhile">Do while</a></li>
    <li><a href="#for">For</a></li>
    <li><a href="#foreach">ForEach</a></li>
    <li><a href="#project4">TASK - Project 4</a></li>
  </ul>

<li><a href="#fifth-project">Arrays</a></li>
<ul>
    <li><a href="#oneDimension">One Dimension</a></li>
    <li><a href="#extrafunction">extra function</a></li>
    <li><a href="#multiDimension">Multi Dimension</a></li>
    <li><a href="#project5">TASK - Project 5</a></li>
  </ul>

<li><a href="#sixth-project">File Reading and Writing</a></li>
<ul>
    <li><a href="#readFile">Read a text file</a></li>
    <li><a href="#writeFile">Write a text file</a></li>
    <li><a href="#project6">TASK - Project 6</a></li>
  </ul>
<li><a href="#seventh-project">Methods - functions</a></li>
<ul>
    <li><a href="#Methods">What is it</a></li>
    <li><a href="#exmethod">example methods</a></li>
    <li><a href="#project7">TASK - Project 7</a></li>
  </ul>

<li><a href="#resources-content">Resources</a></li>
</ul>

<hr> <br>

<h1>Getting Started</h1>
<h2>The IDE</h2>
We'll start off by installing <a href="https://visualstudio.microsoft.com/vs/community/">Visual Studio</a> however, feel free to use any IDE you feel comfortable with. It's important to know your way around the IDE of use so make sure to read documentation and at least know the basics of it.
<br>
<h2>Resources</h2>
This tutorial follows on from these online recources and gives some practice examples to complete to test your progress, it's not required but recommended you at least check out these <a href="#resources-content">resources</a> for a better understand of basics

<h6 style="font-size:11px;"><i>*note: Many examples found in this document are taken and modified from various sites. A complete resource list can be found <a href="#resources-content">here</a></i></h6>

<hr> <br>

<h1 id="first-project">Running your first project</h1>
In this section you will learn to
<ul>
  <li>Run a basic program</li>
  <li>Debug your program</li>
  <li>Understand coding terms and code pieces</li>
    <ul>
      <li>Using</li>
      <li>Namespaces</li>
      <li>Classes</li>
      <li>Content</li>
    </ul>
</ul>
<br>
<h2 id="creating-first-project">Creating your first C# application</h2>
It is advised that you create a new folder with each project and lesson as to make sure everything is easy to find and organised. <br>

```cmd
~$ mkdir "csharp tafe course"
~$ cd "csharp tafe course"
```

```cmd
~$ mkdir "examples"
~$ mkdir "projects"
~$ cd "examples"
```

<br>

For this example project we will create a new folder with the name "Hello World Example". <br>

```cmd
~$ mkdir "1 hello world"
~$ cd "1 hello world"
```

<br>

Now it's time to create a `C# console app` and call it `main.cs`. Once created open it up in visual studio, or your IDE of choice, and make sure that you can connect to that project through the IDE editor. Now you have set everything up, write out the example code below. Try think about what it does before running it. <br><br>

```csharp
using System;

namespace HelloWorld
{
  class Program
  {
    static void Main(string[] args)
    {
      Console.WriteLine("Hello World!");    
    }
  }
}
```

<h6 style="font-size:11px;"><i>*note: 
  <ul>
    <li>// will comment out a line</li> 
    <li>/* will comment out a section */</li>
  </ul></i>
</h6>

<br>

So what does this program actually do? This application will output the phrase "Hello World!" into the commandline. This project is the starting point of every programmers langauge learning journey. Lets now delve into what each line in this program does for a better understanding of C#. 
<br><br>
It's important to note that the topics discussed below will be later discussed in more detail, this is just a simple overview as so you get a basic idea of C# and to not overload your brain with information.

<br>

<h3 id="namespaces">Namespaces</h3>

```csharp
using System;
```

<br>

This first line of code is called a `Namespace`. A Namespace is an element in C# code used to organise your programs and, once created, allow you to reference parts of code from that namespace for later functions in the code. 

So what is the `System` namespace and what does it include? <br>

> "The System namespace contains fundamental classes and base classes that define commonly-used value and reference data types, events and event handlers, interfaces, attributes, and processing exceptions." - <a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/namespaces/">A Guide to Namespaces</a>

<br>

The `using` keyword is equivalent to the `import` keyword. It allows you to import, or "use", that particular namespace (i.e. function)
<br><br>

```csharp
namespace HelloWorld {
...
}
```

<br>

This line of code should be easy to interpret considering the previous analysis of the `System` namespace. In this line of code we create our own namespace labeled `HelloWorld`.

<h6 style="font-size:11px;"><i>*note: for more information on namespaces and System check out these resources
  <ul>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/language-specification/namespaces">What is a  Namespace?</a></li>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/namespaces/">A Guide to Namespaces</a></li> 
    <li><a href="https://docs.microsoft.com/en-us/dotnet/api/system?view=netframework-4.8">What the System Namespace does</a></li>
  </ul></i>
</h6>

<br>

<h3 id="classes">Classes</h3>

```csharp
class Program {
...
}
```

<br>

Here we create a `class` and label it `Program`. A class is a <br>

> "...basic concept of Object-Oriented Programming which revolve around... real-life entities" - <a href="https://www.geeksforgeeks.org/c-sharp-class-and-object/">Geeks for Geeks - Class and Object</a>

<br>

It's essentially a user-defined blueprint which the interpretor uses to create an `Object`. 
In that quote you saw the phrase `Object-Oriented Programming` and `Object`, don't worry about these terms just yet because they will be discussed later. {add link to where they are discussed}

<h6 style="font-size:11px;"><i>*note: for more information on OOP, Objects and Classes check out these resources
  <ul>
    <li><a href="https://www.geeksforgeeks.org/c-sharp-class-and-object/">Classes and Objects</a></li>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/classes">A Guide to Classes</a></li> 
    <li><a href="https://en.wikipedia.org/wiki/Object-oriented_programming">What Object-Oriented Programming (OOP)</a></li>
  </ul></i>
</h6>

<br>

<h3 id="methods">Methods</h3>

```csharp
static void Main(string[] args) {
...
}
```

<br>

This is what we call a `Method`. A method is similar to a `Function` in other programming languages. The `Main` method is called in the above code. The main method is the first method (function) to be called when initially running the program. This means that nearly all the code you write will be inside the `Main()` method. 

For now we won't talk about what `static void` and `(string[] args)` means just yet, they will be discussed later however, if you want to read about them now some links to more information will be located just below.

<h6 style="font-size:11px;"><i>*note: It is important to note that throughout this document `method` and `function` are interchangeably used, they both mean the same thing. a method is a function and a function is a method</i></h6>

<h6 style="font-size:11px;"><i>*note: for more information on Methods check out these resources
  <ul>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/main-and-command-args/">Main Method</a></li>
    <li><a href="https://www.quora.com/Why-do-we-use-static-void-main-string-args-in-C">breakdown of a method</a></li> 
  </ul></i>
</h6>

<br>

<h3 id="printing">Printing to the console</h3>

```csharp
Console.WriteLine("Hello World!");
```

<br>

Finally onto the last line of this small program, if any of these concepts haven't made much sense don't worry too much as they will be covered later in the document. This was just a small rundown on basic concepts from a beginner application for people who don't have very much knowledge on C#. It is recommended however that further research into misunderstood topics to be done as all the example applications will build upon these basic concepts with the addition of more concepts.

In this line we have a couple things to talk about and we'll start with `Console.`. What is this? This is actually a `namespace`, remember from above how we used a namespace by importing it? (`using System;`). Here we use the namespace `Console` but you may be thinking, why didn't we import it? dont we have to import it to use it? Well, kind of. 

If we imported it the application would look like this instead: <br><br>

```csharp
using System;
using Console;

...{
  ...{
    ...{
      WriteLine("Hello World!");
    }
  }
}
```

<br>

If we import `Console` we can use any function inside of the namespace without needing to declare it. `WriteLine` is a function inside the `Console` namespace however, because we didn't reference (import) it at the start of the application we declared it as we used the functuion. Thats why in the line `Console.WriteLine(...);` we declare it.

So we've now declared the `Console.` namespace, what does the `WriteLine();` function do? It does exactly what it looks like it does, it prints out to the command line whatever is inside the function (inside the () brackets). 

We will talk about data types in the next section of this document but as of currently just remember:
<ul>
  <li>  
    A `String` is a series of characters and are declared by surrounding them in quotation marks (single '' or double "" work the same way). Example: "This is a string", "A string can include numbers aswell, 1 or 4 or maybe even 7"
  </li>
  <li>   
    An int (short for integer) is a series of numbers and are <b>not</b> contained in quotation marks, these are numbers that don't include decimal points
  </li>
</ul>

<h6 style="font-size:11px;"><i>*note: for more information on Methods check out these resources
  <ul>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/api/system.console.writeline?view=netframework-4.8">WriteLine() method</a></li>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/strings/">What are Strings</a></li> 
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types">What are Integers</a></li> 
  </ul></i>
</h6>

<br>

<h1 id="project1">main.cs: A Project About Structuring Your Programs</h1>
Now that you've learnt the structure of a C# program it's your time to have a go at creating one. Throughout this document there will be examples and mini projects for you to test your knowledge and to allow a hands on learning experience. <br>

The goal of this project is to, using the .cs file we just created, code a program which outputs the text `"C# is fun"` to the command line. Goodluck.

<h6 style="font-size:11px;"><i>*note: Underneath is an answer to this project, it is highly advised you take an attempt at the project before viewing the answer. Also note that there is never 1 single way to create a projects answer, everyone codes different and therefore there are many solutions to a single question. For this reason it is important to realise your answer may not match the one provided below, it is just a basic guide of our interpretation of the answer. As long as your program does what the question asks, you have succeeded.</i></h6>

<br>
<h3>Project 1 Answer</h3> <br>

```csharp
using System;

namespace Project1
{
    class Program
    {
        static void Main(string[] args) 
        {
            Console.WriteLine("C# is fun")
        }
    }
}
```

<br>

Once you have finished the above program you are ready to move onto the next section

<hr> <br>

<h1 id="second-project">Data Types, variables and sequence</h1>
In this section you will learn to
<ul>
    <li>Data types</li>
    <li>Type conversion</li>
    <li>Variables</li>
    <li>Operators</li>
    <li>Sequence</li>
    <li>Comments</li>
    <li>Pseudo Code</li>
  </ul>

<br>
<h2>Variables</h2>
Variables are declarations which allow you to store a certain value to a certain name. Variables can hold many types of data but that data type should always be declared when creating it.
<br><br>

```csharp
int bobAge = 100;
string bobAddress = "200 Old Man Street"
```

<br>

In this small piece of code we declare that the variable `bobAge` is an integer and that it contains the value `100`. Now whenever we want to reference the value 100 instead we can reference "bobAge". The same is done with `bobAddress`, we decalre it as a string and assign it the value `"200 Old Man Street"`. So why is this useful? Why not just reference "100" or "200 Old Man Street". Well what if we want a value to change but have it in the same section of a function? We can't just change the code everytime we want a value to change. By assigning it a name we can reference that variable in the code and assign it a new value whenever.

<br>
Here is a short list of the most common variable types
<ul>
  <li>int: 4 Bytes : Stores whole numbers from -2,147,483,648 to 2,147,483,647</li>
  <li>long: 8 Bytes: Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807</li>
  <li>float: 4 Bytes: Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits</li>
  <li>double: 8 Bytes:  Stores fractional numbers. Sufficient for storing 15 decimal digits</li>
  <li>Bool: 1 bit: Stores values with two states: true or false</li>
  <li>Char: 2 Bytes: Stores single characters, such as 'a' or 'B'. Char values are surrounded by single quotes</li>
  <li>String: 2 Bytes per character: Stores text, such as "Hello World". String values are surrounded by double quotes</li>
</ul>
<hr>
<br>

<h1>Data Types and Type Casting</h1>
<h2>User Input</h2>
Here is an example of a program that uses users input, try read through the code and think about what it does. Once you think you know what happens, create a new example and add the code into it, run it, and see if you were correct.
<br><br>

```csharp
/*
 * c# program - check wheteher the number entered is odd or even
*/

// pseudo code
// user enters a number
//if the value is even print out "even number"
//if the value is odd print out "odd number"
//end program

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
 
namespace check1
{
    class Program
    {
        static void Main(string[] args)
        {
            int i;
            Console.Write("Enter a Number : ");
            i = int.Parse(Console.ReadLine());
            if (i % 2 == 0)
            {
                Console.Write("Entered Number is an Even Number");
                Console.Read();
            }
            else
            {
                Console.Write("Entered Number is an Odd Number");
                Console.Read();
            }
        }
    }
}
```

<br>

Now that you've run the code you would have seen that the program allows you to determine whether a value is odd or even. Let's do a quick run down of how this program works. 

<h3>Imports</h3>

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

<br>

Here we import a variety of things which allow use certain functions. All these functions are taken from the `System` import, thats why we use `System.nameofpackage`.

<br>

<h3>Variables and User Input</h3>

```csharp
... {
  ... {
    ... {
      int i;
      Console.Write("Enter a Number : ");
      i = int.Parse(Console.ReadLine());
    }
  } 
}
```

<br>

Here we see that we start off by declaring the variable `i` as an `integer`, however we dont assign it a value just yet. In the next line we use a new function called `Console.Write();`, what does this do? It's the same as `Console.WriteLine();` however instead of outputting the text on a serparate line it creates it on the current line. This will make more sense when you compare the two in action. `i = int.Parse(Console.ReadLine());` is essentially 2 lines of code combined into 1 single line, the first bit being `int.Parse();` and the second being `Console.ReadLine();`. `Console.ReadLine();` allows the user to type into the terminal window and by assigning the function a value allows you to take what the user writes and assign it to that said variable. (eg, `i = Console.ReadLine();`). The other part of the code takes what the user inputs and turns it into an integer, by default anything a user enters is counted as a string. So in order to do any math with it we must first convert it to an integer, this is done by the `int.Parse()` function. So by incorperating both these functions into a single line of code `i = int.Parse(Console.ReadLine));` we take the users intput, turn it into a string, and assign it to the variable `i`. 

<br>

So now the number the user enters is assigned to `i` what are we going to do with it?

<br>

<h3>If else</h3>

```csharp
... {
  ... {
    ... {  
      if (i % 2 == 0) {
        Console.Write("Entered Number is an Even Number");
        Console.Read();
      }
      else {
        Console.Write("Entered Number is an Odd Number");
        Console.Read();
			}
		}
		}
	}
```

<br>

This is what's called an `if else` statement, it does pretty much what it sounds like, it tries something and if that doesn't work it moves onto the next bit. In the example above it checks `if (i % 2 == 0)` which means if `i` is divisible with by 2 with no remainders, indicated by the `%` sign, then activate the section of code `Console.Write("Entered Number is an Even Number");` which writes `"Entered Number is an Even Number"` to the console. However, if `i` wasn't divisible by 2 with no remainders it would then activate the `else` section of the coad outputing to the console `"Entered Number is an Odd Number"`.

<br>

<h3>Recap</h3>

<ul>
  <li>Console.Write(); / Console.WriteLine(); || Functions that output text to the terminal window</li>
  <li>Console.ReadLine(); || Allows you to capture the users input</li>
  <li>if... else || Allows you to have a set True or False query to decide what part of the code is run</li>
  <li>% || Allows you to check if a number is divisible by another without remainders</li>
  <li>int.Parse(); || Allows you to convert a data type to an integer</li>
</ul>

<h2>Decisions</h2>
<p>C# provides many decision making statements that help the flow of the C# program based on certain logical conditions. C# includes the following decision making statements.</p>
<ul>
<li>if statement</li>
<li>if-else statement</li>
<li>if-elseif-else statement</li>
<li>switch statement</li>

<h3>If</h3>

if(boolean expression == true or false)
{
    // execute all this code if expression evalutes to true
}

```csharp
if(true)
{
    Console.WriteLine("This will be displayed.");
}
Console.ReadLine();
```


or you can have multiple if statements

```csharp
int i = 10, j = 20;

if (i > j)
{
    Console.WriteLine("i is greater than j");
}

if (i < j)
{
    Console.WriteLine("i is less than j");
}        

if (i == j)
{
    Console.WriteLine("i is equal to j");
}   
```


<h3>If Else</h3>

if(boolean expression == true or false)
{
    // execute all this code if expression evalutes to true
}
else
{
    // execute all this code if expression evalutes to false
}


```csharp
int i = 10, j = 20;

if (i > j)
{
    Console.WriteLine("i is greater than j");
}
else
{
    Console.WriteLine("i is either equal to or less than j");
}
```


<h3>If elseif else</h3>

TASK - write pseudo code for the following program - also add comments to the code 
```csharp
using System;

namespace Game1
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("find the number");
            Console.Write("choose a number: 1, 2 or 3: ");
            string userValue = Console.ReadLine();
            if (userValue == "1") 
            {
                string message = "you won a lot of stuff!"; 
                Console.WriteLine(message);
            }
            else if (userValue == "2")
            {
                string message = "you won a bit of stuff!"; 
                Console.WriteLine(message);
            }
            else if (userValue == "3")
            {
                string message = "you won some stuff! - but not much"; 
                Console.WriteLine(message);
            }
            else             {
                string message = "you cannot read! - try again...... sigh";
                Console.WriteLine(message);
            }
            Console.ReadLine();
        }
    }
}
```


<h3>Switch</h3>
statements – use them if you have a range of known inputs that require a particular output. Or you don’t want to write down a massive list of If else statements.
Note - to get out of a Case we need to 'break' this allows the program to flow into the next section (after the switch)

```csharp
int day = 4;
switch (day) 
{
  case 1:
    Console.WriteLine("Monday");
    break;
  case 2:
    Console.WriteLine("Tuesday");
    break;
  case 3:
    Console.WriteLine("Wednesday");
    break;
  case 4:
    Console.WriteLine("Thursday");
    break;
  case 5:
    Console.WriteLine("Friday");
    break;
  case 6:
    Console.WriteLine("Saturday");
    break;
  case 7:
    Console.WriteLine("Sunday");
    break;
}
```

<h3>Recap</h3>
<ul>
  <li>decisions provide branches for your data flow</li>
  <li>If this is true then do the code block</li>
  <li>if... else - if this is true then do this code else do the other code code</li>
<li>switch statement - define certain cases which can be tested for a match - when matched do the code block then exit the switch</li>
</ul>

<h3>TASK - Project 2</H3>
<hr> <br>
Create a small program (using decisions) to achieve the following
A Teacher is to enter a grade and write a standard output for the student.
<ul>
<li>Grade < 50%  Fail  can try harder</li>
<li>Grade 51-60%  Pass  works hard</li>
<li>Grade 61-75%  Pass  Quiet achiever</li>
<li>Grade 76-90%  Pass  Unexpected result a joy to behold</li>
<li>Grade 91-100%  Fail  an obvious cheat no evidence of intellect shown previously</li>
</ul>

Compare your solution with other students' answers to see if there are better ways to produce your program
<hr> <br>

<h2>Loops</h2>
<h3>While</h3>
<br>
<img src="https://user-images.githubusercontent.com/33891852/77504632-9dda9680-6eac-11ea-98e2-da2c64006c3d.PNG"/>
<br>

```csharp
int i = 0;

while (i < 2)
{
    Console.WriteLine("Value of i: {0}", i);
    int j = 1;

    i++;

    while (j < 2)
    {
        Console.WriteLine("Value of j: {0}", j);
        j++;
    }
}
```

<h3>Do While</h3>
<br>
<img src="https://user-images.githubusercontent.com/33891852/79522178-5e176100-809e-11ea-8ca8-bdf3c40dd58f.PNG"/>
<br>

```csharp
	int i = 0;

	do
		{
		Console.WriteLine("Value of i: {0}", i);
		int j = i;
		i++;     
    do
		{
        Console.WriteLine("Value of j: {0}", j);
        j++;
		} while (j < 2);

	} while (i < 2);
```

<h3>For - or iteration</h3>
<br>
<img src="https://user-images.githubusercontent.com/33891852/79521876-99fdf680-809d-11ea-9caa-19d0461cdf42.PNG"/>
<br>

```csharp
	using System;

	namespace Itteration1
		{
		class Program
		{
			static void Main(string[] args)
			{
				for (int i = 0; i < 10; i++) //loop through while == True
					{
					//Console.WriteLine(i);
					if (i == 7)
					{
						continue;
					}
                Console.WriteLine("Found the number 7");
                break;
            }

            for (int i = 0; i < 12; i++)
				{
                Console.WriteLine(i);
				}
            Console.ReadLine();
			}
		}
	}
```

<h3>ForEach</h3>

```csharp
	public class Foreach
		{
			public static void Main()
			{
				// Span is a way of managing memory in .net 
				Span<int> storage = stackalloc int[10];
				int num = 0;
				foreach (ref int item in storage)
				{
					item = num++;
				}

				foreach (ref readonly var item in storage)
				{
					Console.Write($"{item} ");
				}
				// Output:
				// 0 1 2 3 4 5 6 7 8 9
			}
		}
```
<h3>Recap</h3>
<ul>
  <li>loops provide recuring tasks to be performed - go through your data to extract something</li>
  <li>types: while - do while, for, foreach</li>
</ul>

<h3>TASK - Project 3</H3>
<hr> <br>
Create a small program 
Compare your solution with other students' answers to see if there are better ways to produce your program
<hr> <br>




<h2>Arrays</h2>
<h3>One dimension</h3>
<br>
<img src="https://user-images.githubusercontent.com/33891852/79522348-cc5c2380-809e-11ea-8da3-b2eeb0f36215.png"/>
<br>

```csharp
	using System;

	namespace Array_1
	{
		class Program
		{
			static void Main(string[] args)
			{
				int[] numbers = new int[5];

				numbers[0] = 4;
				numbers[1] = 5;
				numbers[2] = 15;
				numbers[3] = 16;
				numbers[4] = 23;

				Console.WriteLine(numbers[2]); //access third element
				Console.WriteLine(numbers.Length); //how many elements in the array
				Console.ReadLine(); // pause - wait for key input
			}
		}
	}
```
<h3>Extra functions</h3>

```csharp
	using System;

	namespace Array_2
	{
		class Program
		{
			static void Main(string[] args)
			{
				int[] numbers = new int[] { 4, 8, 15, 16, 23, 42 }; //array length defined by number of elements in {}
				Console.WriteLine(numbers[2]);
				Console.ReadLine();

				string[] words = new string[] {"bob", "stan", "bill"};
				for (int i = 0; i < words.Length; i++)
				{
					Console.WriteLine(words[i]);

				}
				Console.ReadLine();
				
				words[1] = "fred";
				Console.WriteLine(words[1]);
				Console.ReadLine();

				foreach (string name in words)
				{
					Console.WriteLine(name);
				}
				Console.ReadLine();

				//reverse the string
				string str = "if you have something to do - do it";
				char[] charArray = str.ToCharArray();
				Array.Reverse(charArray);

				foreach (char char1 in charArray)
				{
					Console.Write(char1);
				}
				Console.ReadLine();
			}
		}
	}
```
<h3>Multi Dimension - in this case a 2 dimensional array</h3>
<br>
<img src="https://user-images.githubusercontent.com/33891852/79523088-b6e7f900-80a0-11ea-81e6-ea625160f218.png"/>
<br>

```csharp
	int[,] arr2d = new int[3,2]{ 
                                {1, 2}, 
                                {3, 4}, 
                                {5, 6} 
                            };

	arr2d[0, 0]; //returns 1
	arr2d[0, 1]; //returns 2
	arr2d[1, 0]; //returns 3
	arr2d[1, 1]; //returns 4
	arr2d[2, 0]; //returns 5
	arr2d[2, 1]; //returns 6
	//arr2d[3, 0]; //throws run-time error as there is no 4th row
```
<h3>Recap</h3>
For multidimensional arrays - the first number used in the declaration of the array equates to the number of rows, the second number equates to the number of columns
<ul>
  <li>arrays hold multiple buckets of data - accessed by refgerencing the elemnet number of the array</li>
  <li>can have 1 line arrays (like a string) 2 dimensions - even arrays of arrays (makes my head hurt thinking of these)</li>
</ul>
<h3>TASK - Project 4</H3>
<hr> <br>
Create a small program 
Compare your solution with other students' answers to see if there are better ways to produce your program
<hr> <br>


<h2>Working with files</h2>
<h3>read and write text to and from a file stored locally</h3>

```csharp
	using System;
	using System.IO;  // include the System.IO namespace

	namespace Files
		{
			class Program
			{
				static void Main(string[] args)
				{
				string writeText = "Hello World!";  // Create a text string
				File.WriteAllText(@"f:\file1.txt", writeText);  // Create a file and write the content of writeText to it

				string readText = File.ReadAllText(@"f:\file1.txt");  // Read the contents of the file
				Console.WriteLine(readText);  // Output the content

            // Example #2: Write one string to a text file.
				string text = "A class is the most powerful data type in C#. Like a structure, " +
                           "a class defines the data and behavior of the data type. ";
            // WriteAllText creates a file, writes the specified string to the file,
            // and then closes the file.    You do NOT need to call Flush() or Close().
				File.WriteAllText(@"f:\file2.txt", text);

				string readText2 = File.ReadAllText(@"f:\file2.txt");  // Read the contents of the file
				Console.WriteLine(readText2);  // Output the content

            // Create a string array with the lines of text
				string[] lines = { "First line", "Second line", "Third line" };

            // Set a variable to the Documents path.
				string docPath = Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments);

            // Write the string array to a new file named "WriteLines.txt".
				using (StreamWriter outputFile = new StreamWriter(Path.Combine(docPath, "WriteLines.txt")))
					{
                foreach (string line in lines)
                    outputFile.WriteLine(line);
					}

				}
			}
		}
```

<h3>Recap</h3>
<ul>
  <li>the ability to store data for retrieval later is handy</li>
  <li>be careful where you write this data to - can get lost</li>
</ul>
<h3>TASK - Project 5</H3>
<hr> <br>
Create a small program 
Compare your solution with other students' answers to see if there are better ways to produce your program
<hr> <br>

<h2>Methods</h2>
<h3>What are they</h3>
<h3>Examples</h3>

```csharp
  hello
```
<ul>
  <li>Methods (or Functions) are a good way to start dividing your code up</li>
  <li>Each method should have 1 function - i.e. add 2 numbers together - it will make your code easier to read, t'shoot and manage later on when your programs become a lot bigger</li>
</ul>
<h3>TASK - Project 6</H3>
<hr> <br>
Create a small program that uses a function or 2
Compare your solution with other students' answers to see if there are better ways to produce your program
<hr> <br>



<br><br>

<h1 id="resources-content">Complete Resource List</h1>

<h2>C# Code/Project Examples</h2>
<ul>
  <li><a href="https://channel9.msdn.com/Series/CSharp-Fundamentals-for-Absolute-Beginners?l=Lvld4EQIC_2706218949">C# Fundamentals for Absolute Beginners</a></li>
  <li><a href="https://www.csharp-examples.net/">C# Code Examples</a></li>
  <li><a href="https://www.codeproject.com/KB/cs/">C# Project Examples</a></li>
<li><a href="https://www.w3resource.com/csharp-exercises/">Online with sample exercises with flowcharts and solutions </a>
</li>

</ul>

<h2>Namespaces</h2>
<ul>
  <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/language-specification/namespaces">What is a  Namespace?</a></li>
  <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/namespaces/">A Guide to Namespaces</a></li> 
  <li><a href="https://docs.microsoft.com/en-us/dotnet/api/system?view=netframework-4.8">What the System Namespace does</a></li>
</ul>

<h2>Classes, Objects and Object-Oriented Programming</h2>
<ul>
  <li><a href="https://www.geeksforgeeks.org/c-sharp-class-and-object/">Classes and Objects</a></li>
  <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/classes">A Guide to Classes</a></li> 
  <li><a href="https://en.wikipedia.org/wiki/Object-oriented_programming">What Object-Oriented Programming (OOP)</a></li>
</ul></i>

<h2>Methods</h2>
<ul>
  <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/main-and-command-args/">Main Method</a></li>
  <li><a href="https://www.quora.com/Why-do-we-use-static-void-main-string-args-in-C">breakdown of a method</a></li> 
</ul></i>

<h2>WriteLine Methods and Strings/Integers</h2>
<ul>
  <li><a href="https://docs.microsoft.com/en-us/dotnet/api/system.console.writeline?view=netframework-4.8">WriteLine() method</a></li>
  <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/strings/">What are Strings</a></li> 
  <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types">What are Integers</a></li> 
</ul></i>

