# C#

[Structure](#structure)\
[Data](#data)\
[Console](#console)\
[Flow](#flow)

```
https://programmingbydoing.com/
https://www.caveofprogramming.com/c-sharp-tutorial/basic-c-programming-test-your-knowledge-2.html
15 : The Forgetful machine
```
## Structure

*Basic Program Outline*

```c#
using System;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World");
        }
    }
}
```

*Class in other file*
```c#
using System;

namespace ConsoleApp1
{
    class Car
    {
        private String name;             // Private class method
        
        public Car(String name)          // Class Constructor with parameter
        {         
            this.name = name;
        }
    
        public void Start()              // Class function
        {
            Console.WriteLine("Car started!");
        }
    }
}
```


## Data

*Simple Array*
```c#
int[] numberArray = new int[5] {1, 2, 3, 4, 5};    // Initializing array
Console.WriteLine(numberArray[2]);                 // Accessing array at given index
```

*2d Array*
```c#
int[,] numberArray = new int[,] {{1,1}, {1,1}, {1,1}, {1,1}, {1,1}};    // Initializing array
Console.WriteLine(numberArray[0,1]);                                    // Accessing array at given index
```

*Casting*
```c#
Convert.ToInt32(Console.ReadLine());     // Casting from String to Int
Convert.ToDouble(Console.ReadLine());    // Casting from String to Double
```

## Console

*Writing*
```c#
Console.WriteLine();
```

*Reading*
```c#
Console.ReadLine();

```


## Flow

*If Else*
```c#
if (x < y)
{
    // Do this
}
else
{
    // Do this
}
```

*For*
```c#
for (int i = 0; i < 5; i++)
{
    // Do this
}
```

*While*
```c#
while( x == y)
{
    // Do this
}
```

*Switch*
```c#
switch (value)
{
    case 1:
        // Execute code
        break;
    case 2:
        // Execute code
        break;
    default:
        // Execute code
        break;
}
```
