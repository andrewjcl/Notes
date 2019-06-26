# C Sharp

```
https://programmingbydoing.com/
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

#### Console

*Writing*
```c#
Console.WriteLine();
```

*Reading*
```c#
Console.ReadLine();
Convert.ToInt32(Console.ReadLine()); // Casting from String to Int
Convert.ToDouble(Console.ReadLine()); // Casting from String to Double
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
