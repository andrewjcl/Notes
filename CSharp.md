# C#

```
https://programmingbydoing.com/
https://www.caveofprogramming.com/c-sharp-tutorial/basic-c-programming-test-your-knowledge-2.html
15 : The Forgetful machine
```

### Basic Program Outline

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
#### Data

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




#### Console

*Writing*
```c#
Console.WriteLine();
```

*Reading*
```c#
Console.ReadLine();
Convert.ToInt32(Console.ReadLine());     // Casting from String to Int
Convert.ToDouble(Console.ReadLine());    // Casting from String to Double
```


#### Flow

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
