## hashset
```C#
//https://rextester.com/l/csharp_online_compiler
//Rextester.Program.Main is the entry point for your code. Don't change it.
//Compiler version 4.0.30319.17929 for Microsoft (R) .NET Framework 4.5

using System;
using System.Collections.Generic;
using System.Linq;

namespace Rextester
{
    public class Program
    {
        public static void Main(string[] args)
        {
            HashSet<int> set = new HashSet<int>();
            set.Add(5);
            set.Add(2);
            set.Add(5);
            set.Add(3);
            set.Add(5);
            
            Console.Write("set: ");
            // ToList(): defined in Linq
            set.ToList().ForEach(x => Console.Write("{0},", x));
            
            Console.WriteLine();
            Console.WriteLine("set: " + String.Join(",", set));
            
            Console.WriteLine();
            Console.WriteLine("set.Count: " + set.Count);
            Console.WriteLine("set.Count(): " + set.Count());
            Console.WriteLine("set.Contains(2): " + set.Contains(2));
            Console.WriteLine("set.Contains(2): " + set.Contains(2));
        }
    }
}
```
- [C# HashSet 用法、Hashtable用法](https://www.itread01.com/p/1420575.html)

執行結果：
```
set: 5,2,3,
set: 5,2,3

set.Count: 3
set.Count(): 3
set.Contains(2): True
set.Contains(2): True
```
