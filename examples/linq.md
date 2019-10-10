### sum([2, 4, 6, 8, 10]) = 30
```C#
//https://rextester.com/l/csharp_online_compiler
//Rextester.Program.Main is the entry point for your code. Don't change it.
//Compiler version 4.0.30319.17929 for Microsoft (R) .NET Framework 4.5

using System;
using System.Linq;

namespace Rextester
{
    public class Program
    {
        public static void Main(string[] args)
        {
            int[] nums = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
            
            // sum event numbers
            nums = nums.Where(x => x % 2 == 0).ToArray(); // Where(): in Linq
            Console.Write(String.Join(" + ", nums));
            Console.WriteLine(" = " + nums.Sum()); // Sum(): in Linq
            Console.WriteLine("average = " + nums.Average()); // Average(): in Linq
        }
    }
}
```

### 參考資料
- [How to delete an element from an array in C#](https://stackoverflow.com/questions/496896/how-to-delete-an-element-from-an-array-in-c-sharp)
- [How to sum up an array of integers in C#](https://stackoverflow.com/questions/2419343/how-to-sum-up-an-array-of-integers-in-c-sharp)
- [filter an array in C#](https://stackoverflow.com/questions/1912128/filter-an-array-in-c-sharp)
