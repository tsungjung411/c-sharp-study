
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

## 參考資料
- [C# 陣列排序](https://e8859487.pixnet.net/blog/post/391833046)
- [[dotnet] List<T>.ForEach(Action<T>) Method](https://docs.microsoft.com/zh-tw/dotnet/api/system.collections.generic.list-1.foreach?view=netframework-4.8)
