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
