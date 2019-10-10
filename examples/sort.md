## Primitive types
```C#
// https://rextester.com/l/csharp_online_compiler
// Rextester.Program.Main is the entry point for your code. Don't change it.
// Compiler version 4.0.30319.17929 for Microsoft (R) .NET Framework 4.5

using System;
using System.Linq;

namespace Rextester
{
    public class Program
    {
        public static void Main(string[] args)
        {
            int[] nums = {8,4,5,1,7,2,9,6,3,0};
            Array.Sort(nums);
            
            foreach (int num in nums)
            {
                Console.WriteLine("num: " + num);
            }
            
            // the extension is from Linq
            nums.ToList().ForEach(Print);
            nums.ToList().ForEach(Console.WriteLine);
            nums.ToList().ForEach(delegate(int x) {
                Console.WriteLine("delegate: x: " + x);
            });
        }
        
        private static void Print(int x)
        {
            Console.WriteLine("Print: x: " + x);
        }
    }
}
```

## Class types
```C#
// https://rextester.com/l/csharp_online_compiler
// Rextester.Program.Main is the entry point for your code. Don't change it.
// Compiler version 4.0.30319.17929 for Microsoft (R) .NET Framework 4.5

using System;
using System.Collections.Generic;

namespace Rextester
{
    public class Person: IComparable
    {
        public Person()
        {
        }
        public Person(string name, int weight)
        {
            this.Name = name;
            this.Weight = weight;
        }
        public string Name { get; set;}
        public int Weight { get; set;}
        public int CompareTo(object another)
        {
            if (another is Person)
            {
                return this.Weight.CompareTo((another as Person).Weight);
            }
            else
            {
                throw new ArgumentException("object is not Person");
            }
        }
        public override string ToString()
        {
            return this.Name + ": " + this.Weight + "(kg)";
        }
    }
    
    public class Program
    {
        public static void Main(string[] args)
        {
            // defined in System.Collections.Generic
            List<Person> list = new List<Person>();
            Person p;
            
            list.Add(new Person("TJ_Tsai", 62));
            list.Add(new Person("John", 65));
            list.Add(new Person("David", 61));
            list.Add(new Person("TV", 100));
            list.Sort();
            list.ForEach(Console.WriteLine);
            
            Person[] persons = new Person[] {
                new Person() {Name = "TJ_Tsai", Weight = 62},
                new Person() {Name = "John", Weight = 65},
                new Person() {Name = "David", Weight = 61},
                new Person() {Name = "TV", Weight = 100},
            };
            Array.Sort(persons);
            list.ForEach(Console.WriteLine);
        }
    }
}
```

## 參考資料
- [C# 陣列排序](https://e8859487.pixnet.net/blog/post/391833046)
- [[dotnet] List<T>.ForEach(Action<T>) Method](https://docs.microsoft.com/zh-tw/dotnet/api/system.collections.generic.list-1.foreach?view=netframework-4.8)
