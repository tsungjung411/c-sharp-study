## 學習資源
- [TutorialPoint](https://www.tutorialspoint.com/csharp)
- [Microsoft C# 指南](https://docs.microsoft.com/zh-tw/dotnet/csharp/index)
- [TQC+ C# 認證教學手冊](https://tqcplus-csharp-ebook.readbook.tw/)

## 安裝軟體
- [Ubuntu - Mono](https://www.mono-project.com/download/stable/#download-lin-ubuntu)
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
- 跟 java 的差別
  - 匯入套件：import(java) v.s. using(C#)
  - 入口點：main(java) v.s. Main(C#)
  - 字串：String(java) v.s. string(C#)
  - 輸出：System.out.println(java) v.s. Console.WriteLine(C#)
  - 函數：以小寫開頭(java) v.s. 大寫開頭(C#)
    - [駝峰式大小寫](https://zh.wikipedia.org/wiki/%E9%A7%9D%E5%B3%B0%E5%BC%8F%E5%A4%A7%E5%B0%8F%E5%AF%AB)
      - 小駝峰式命名法 (lower camel case)
      - 大駝峰式命名法 (upper camel case)
