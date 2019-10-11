## 學習資源
- [TutorialPoint](https://www.tutorialspoint.com/csharp)
- [Microsoft C# 指南](https://docs.microsoft.com/zh-tw/dotnet/csharp/index)
- [TQC+ C# 認證教學手冊](https://tqcplus-csharp-ebook.readbook.tw/)

## 安裝軟體
- ### [C# 語言版本控制](https://docs.microsoft.com/zh-tw/dotnet/csharp/language-reference/configure-language-version)
- ### [Ubuntu - Mono](https://www.mono-project.com/download/stable/#download-lin-ubuntu)
  - 測試環境
    ```bash
    $ mono-csc --version
    Mono C# compiler version 4.2.1.0
    ```
  - [Hello World](https://www.mono-project.com/docs/getting-started/mono-basics/)
    ```csharp
    using System;

    public class HelloWorld
    {
        public static void Main(string[] args)
        {
            Console.WriteLine ("Hello Mono World");
        }
    }
    ```
- ### [Windows] .Net Framework 環境
  - csc.exe 預設是在C:\Windows\Microsoft.NET\Framework\v3.5 (3.5 表示版本資訊)
  - [C#編譯](https://dotblogs.com.tw/eternaltung/2010/01/07/12890)
  - [利用指令工具編譯及執行 C# 程式](https://tqcplus-csharp-ebook.readbook.tw/csharp-and-tools.html)
- ### [使用 Visual Studio Code](https://visualstudio.microsoft.com/downloads/)
- ### 線上寫程式
  - [rextester](https://rextester.com/l/csharp_online_compiler)

## 語法學習
- [[官網] C# 語言教學課程](https://docs.microsoft.com/zh-tw/dotnet/csharp/tour-of-csharp/) - 導覽(簡介)
   - [型別與變數](https://docs.microsoft.com/zh-tw/dotnet/csharp/tour-of-csharp/types-and-variables)
- [[官網] C# 語言教學課程](https://docs.microsoft.com/zh-tw/dotnet/csharp/programming-guide/) - 程式設計手冊(詳細)
   - [類型](https://docs.microsoft.com/zh-tw/dotnet/csharp/programming-guide/types/)
     - [作法：將字串轉換為數值 (C# 程式設計指南)](https://docs.microsoft.com/zh-tw/dotnet/csharp/programming-guide/types/how-to-convert-a-string-to-a-number)

## 主題學習
- C# 編碼慣例
  - [[dotnet] C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/coding-conventions)
  - [[dotnet]C# 編碼慣例](https://docs.microsoft.com/zh-tw/dotnet/csharp/programming-guide/inside-a-program/coding-conventions)
- 標準輸入
  - [How to read Two numbers in c#](https://stackoverflow.com/questions/27589159/how-to-read-two-numbers-in-c-sharp)
    - ['System.Array' does not contain a definition for 'Select' and no extension method 'Select'](https://social.msdn.microsoft.com/Forums/vstudio/en-US/f62a3690-702a-4e92-a076-9d50d4a334c0)
      ```C#
      import Sytem.Linq;
      ```
- 標準輸出
  - [[dotnet] String.Format Method](https://docs.microsoft.com/zh-tw/dotnet/api/system.string.format?view=netframework-4.8#Starting)
  - [[dotnet] 複合格式](https://docs.microsoft.com/zh-tw/dotnet/standard/base-types/composite-formatting)
  - 字串插補
    - 功能同 String.Format()，但改用運算式表達
      - 原因：[What's with the dollar sign ($“string”) ](https://stackoverflow.com/questions/32878549/whats-with-the-dollar-sign-string)
    - [[dotnet] $-字串插補C#](https://docs.microsoft.com/zh-tw/dotnet/csharp/language-reference/tokens/interpolated?view=netframework-4.8)
  - 數值處理
    - [[dotnet] 標準數值格式字串](https://docs.microsoft.com/zh-tw/dotnet/standard/base-types/standard-numeric-format-strings)
    - [[dotnet] 作法：以前置字元零來填補數字](https://docs.microsoft.com/zh-tw/dotnet/standard/base-types/how-to-pad-a-number-with-leading-zeros)
    - 範例
      ```c#
      var pi = 3.14159265;
      Console.WriteLine("pi = {0}", pi);
      Console.WriteLine("pi = {0:0.000}", pi);
      Console.WriteLine("pi = {0,-10:0.000}", pi);
      Console.WriteLine("pi = {0,10:0.000}", pi);
      Console.WriteLine("pi = {0:F3}", pi);
      Console.WriteLine("pi = {0,10:F3}", pi);
      Console.WriteLine("pi = {0,-10:F3}", pi);
      Console.WriteLine("pi = " + pi.ToString("F3"));
      Console.WriteLine("pi = " + pi.ToString("0.000"));
      Console.WriteLine("pi = " + pi.ToString("#0.000"));
      Console.WriteLine("leading zero: " + 123.ToString("D8")); // width:8
      Console.WriteLine("{0:#,###}", 123456789);
      ```
- 字串
  - [Add, Remove, Replace String In C#](https://www.c-sharpcorner.com/UploadFile/mahesh/add-remove-replace-strings-in-C-Sharp/)
  - [@ -- 逐字識別項](https://docs.microsoft.com/zh-tw/dotnet/csharp/language-reference/tokens/verbatim?view=netframework-4.8)
  - [如何：在 C# 比較字串](https://docs.microsoft.com/zh-tw/dotnet/csharp/how-to/compare-strings)
  - 字元
    - [C# String Chars (Get Char at Index)](https://www.dotnetperls.com/string-char)
- 擴充方法
  - [[C#]擴充方法 – 介紹](https://kw0006667.wordpress.com/2013/05/29/c%E6%93%B4%E5%85%85%E6%96%B9%E6%B3%95-%E4%BB%8B%E7%B4%B9/)
- 數學(Math)
  - [Is there an exponent operator in C#?](https://stackoverflow.com/questions/3034604/is-there-an-exponent-operator-in-c)
- 語言整合查詢(LINQ)
  - [[wiki] 語言整合查詢(LINQ)](https://zh.wikipedia.org/wiki/%E8%AF%AD%E8%A8%80%E9%9B%86%E6%88%90%E6%9F%A5%E8%AF%A2)
- 例外處理
  - [[dotnet] 例外狀況的最佳做法](https://docs.microsoft.com/zh-tw/dotnet/standard/exceptions/best-practices-for-exceptions)
- 多維度陣列
  - [[csharp] 多維陣列 (C# 程式設計手冊)](https://docs.microsoft.com/zh-tw/dotnet/csharp/programming-guide/arrays/multidimensional-arrays)

## 比較差異
- 跟 java 的差別
  - 匯入套件：import(java) v.s. using(C#)
  - 入口點：main(java) v.s. Main(C#)
  - 字串：String(java) v.s. string(C#)
  - 輸出：System.out.println(java) v.s. Console.WriteLine(C#)
  - 函數：以小寫開頭(java) v.s. 大寫開頭(C#)
    - [駝峰式大小寫](https://zh.wikipedia.org/wiki/%E9%A7%9D%E5%B3%B0%E5%BC%8F%E5%A4%A7%E5%B0%8F%E5%AF%AB)
      - 小駝峰式命名法 (lower camel case)
      - 大駝峰式命名法 (upper camel case)
