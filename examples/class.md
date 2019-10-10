## 建立基本類別
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
        public Person()
        {
            Console.WriteLine("Person() is called");
        }
        public Person(string name, int weight)
        {
            this.Name = name;
            this.Weight = weight;
            Console.WriteLine("Person(string, int) is called");
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
            Person p1 = new Person("TJ_Tsai", 62);
            Console.WriteLine(p1.ToString());
            
            // the constructor takes 0 arguments
            Person p2 = new Person {Name = "TJ_Tsai", Weight = 62};
            Console.WriteLine(p2.ToString());
        }
    }
}
```

## 比較物件和類別的關係
- java: ```object instanceof Person```
- C#: ```object is Person```

## 物件轉型
- java: ```((Person) object).xxx```
- C#: ```(object as Person).Xxx```

## 參考資料
- [[csharp] 類別 (C# 程式設計手冊)](https://docs.microsoft.com/zh-tw/dotnet/csharp/programming-guide/classes-and-structs/classes)
