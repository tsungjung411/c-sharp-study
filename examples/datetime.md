## "19840411" to DateTime
```
//Rextester.Program.Main is the entry point for your code. Don't change it.
//Compiler version 4.0.30319.17929 for Microsoft (R) .NET Framework 4.5

using System;
using System.Globalization;

namespace Rextester
{
    public class Program
    {
        public static void Main(string[] args)
        {
            DateTime dt = DateTime.ParseExact(
                "20191012", "yyyyMMdd", 
                CultureInfo.InvariantCulture);
            
            Console.WriteLine("year: " + dt.Year);
            Console.WriteLine("month: " + dt.Month);
            Console.WriteLine("day: " + dt.Day);
            Console.WriteLine("week: " + dt.DayOfWeek);
            
        }
    }
}
```
 - [Parse string to DateTime in C#](https://stackoverflow.com/questions/5366285/parse-string-to-datetime-in-c-sharp)

## 參考資料
- [[dotnet] CultureInfo.InvariantCulture Property](https://docs.microsoft.com/zh-tw/dotnet/api/system.globalization.cultureinfo.invariantculture?view=netframework-4.8)
- [Parse string to DateTime in C#](https://stackoverflow.com/questions/5366285/parse-string-to-datetime-in-c-sharp)
