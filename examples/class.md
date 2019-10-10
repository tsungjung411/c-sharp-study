```C#
// https://rextester.com/l/csharp_online_compiler
// Rextester.Program.Main is the entry point for your code. Don't change it.
// Compiler version 4.0.30319.17929 for Microsoft (R) .NET Framework 4.5

using System;
using System.Linq;

namespace Rextester
{
    public class Person
    {
        public Person(string name, int weight)
        {
            this.Name = name;
            this.Weight = weight;
        }
        public string Name { get; set;}
        public int Weight { get; set;}
        public override string ToString()
        {
            return this.Name + ": " + this.Weight + "(kg)";
        }
    }
    
    public class Program
    {
        public static void Main(string[] args)
        {
            Person p = new Person("TJ_Tsai", 62);
            Console.WriteLine(p.ToString());
        }
    }
}
```

## 參考資料
- [[csharp] 類別 (C# 程式設計手冊)](https://docs.microsoft.com/zh-tw/dotnet/csharp/programming-guide/classes-and-structs/classes)
