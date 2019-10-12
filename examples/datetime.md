## Now to string
```
//https://rextester.com/l/csharp_online_compiler
//Rextester.Program.Main is the entry point for your code. Don't change it.
//Compiler version 4.0.30319.17929 for Microsoft (R) .NET Framework 4.5

using System;

namespace Rextester
{
    public class Program
    {
        public static void Main(string[] args)
        {
            Console.WriteLine("Now: " + DateTime.Now);
            Console.WriteLine("GetType: " + DateTime.Now.GetType());
            Console.WriteLine("yyyy-MM-dd HH:mm: "
                              + DateTime.Now.ToString("yyyy-MM-dd HH:mm"));
            Console.WriteLine("week(ddd / dddd): "
                              + DateTime.Now.ToString("ddd (dddd)"));
        }
    }
}
```
- [how can i get the current time in C#? ](https://stackoverflow.com/questions/10374089/how-can-i-get-the-current-time-in-c)

執行結果：
```
Now: 12.10.2019 08:08:11
GetType: System.DateTime
yyyy-MM-dd HH:mm: 2019-10-12 08:59
week(ddd / dddd): Sa (Samstag)
```

<br>

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

執行結果：
```
year: 2019
month: 10
day: 12
week: Saturday
```

<br>

## Week
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
            Console.WriteLine();
            Console.WriteLine("week: " + dt.DayOfWeek);
            Console.WriteLine("week(type): " + dt.DayOfWeek.GetType());
            Console.WriteLine("week(current): " + CultureInfo.CurrentCulture.DateTimeFormat.GetDayName(dt.DayOfWeek));
            Console.WriteLine("week(current): ddd(dddd): " + dt.ToString("ddd (dddd)"));
            Console.WriteLine("week(zh-tw): " + new CultureInfo("zh-tw").DateTimeFormat.GetDayName(dt.DayOfWeek));
            Console.WriteLine("week(ja-jp): " + new CultureInfo("ja-jp").DateTimeFormat.GetDayName(dt.DayOfWeek));
        }
    }
}
```
 - [【.NET】利用 CultureInfo 取得各語系星期顯示名稱](https://dotblogs.com.tw/echo/2016/10/16/dotnet_dayofweek_displaybycultureinfo)
 - [Table of Language Culture Names, Codes, and ISO Values (PIA)](https://docs.microsoft.com/en-us/previous-versions/commerce-server/ee796272(v=cs.20)?redirectedfrom=MSDN)

執行結果：
```
year: 2019
month: 10
day: 12

week: Saturday
week(type): System.DayOfWeek
week(current): Samstag
week(zh-tw): 星期六
week(ja-jp): 土曜日
```

<br>

## 參考資料
- [how can i get the current time in C#? ](https://stackoverflow.com/questions/10374089/how-can-i-get-the-current-time-in-c)
- [Parse string to DateTime in C#](https://stackoverflow.com/questions/5366285/parse-string-to-datetime-in-c-sharp)
- [[dotnet] CultureInfo.InvariantCulture Property](https://docs.microsoft.com/zh-tw/dotnet/api/system.globalization.cultureinfo.invariantculture?view=netframework-4.8)
 - [【.NET】利用 CultureInfo 取得各語系星期顯示名稱](https://dotblogs.com.tw/echo/2016/10/16/dotnet_dayofweek_displaybycultureinfo)
 - [Table of Language Culture Names, Codes, and ISO Values (PIA)](https://docs.microsoft.com/en-us/previous-versions/commerce-server/ee796272(v=cs.20)?redirectedfrom=MSDN)
