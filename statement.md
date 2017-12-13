# Welcome!

This C# template lets you get started quickly with a simple one-page playground.

```C# runnable
// { autofold
using System;
using System.Collections;

class Program
{
    static void Main(string[] args)
    {
        // Pass reference type by value
        ArrayList arrayList = new ArrayList() { 0, 1, 2, 3 };
         Console.WriteLine("Pass by Value");
 
        PassByValue(arrayList); 
        // What should be the output of below line ??
        Console.WriteLine(arrayList[1]);
                arrayList = new ArrayList() { 0, 1, 2, 3 }; 
             Console.WriteLine("Pass by Reference"); 
        PassByReference(ref arrayList); 
        // What should be the output of below line ??
        Console.WriteLine(arrayList[1]); 
       
    } 
    private static void PassByValue(ArrayList arrayList)
    { 
        Console.WriteLine(arrayList[1]);
        // Now Change the first position value
        arrayList[1] = 90;
        arrayList = new ArrayList() { 101, 102, 103, 104 }; 
        Console.WriteLine(arrayList[1]);
    } 
    private static void PassByReference(ref ArrayList arrayList)
    { 
        Console.WriteLine(arrayList[1]); 
        // Now Change the first position value
        arrayList[1] = 90;
             arrayList = new ArrayList() { 101, 102, 103, 104 }; 
        Console.WriteLine(arrayList[1]);
    }
}
```

# Advanced usage

If you want a more complex example (external libraries, viewers...), use the [Advanced C# template](https://tech.io/select-repo/386)
