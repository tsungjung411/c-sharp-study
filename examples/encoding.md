## Encoding
- [[dotnet] Encoding Class](https://docs.microsoft.com/zh-tw/dotnet/api/system.text.encoding?view=netframework-4.8)
  - ```Encoding.GetEncoding("big5")```
  - ```Encoding.GetEncoding(950)```
- [Encoding.Default Property](https://docs.microsoft.com/en-us/dotnet/api/system.text.encoding.default)
  > Different computers can use different encodings as the default, and the default encoding can change on a single computer.
  
## Default Encoding
```C#
using System;
using System.Text;

namespace Main
{
    public class Test
    {
        public static void Main(string[] args)
        {
            dumpEncoding(Encoding.Default);
            
            dumpEncoding(Encoding.GetEncoding(
                Encoding.Default.HeaderName));
        }
        
        static void dumpEncoding(Encoding encoding) {
            string bodyName = Encoding.Default.BodyName;
            int codePage = Encoding.Default.CodePage;
            string encodingName = Encoding.Default.EncodingName;
            string headerName = Encoding.Default.HeaderName;
            string webName = Encoding.Default.WebName;
            Console.WriteLine("bodyName: \"{0}\"", bodyName);
            Console.WriteLine("codePage: {0}", codePage);
            Console.WriteLine("encodingName: \"{0}\"", encodingName);
            Console.WriteLine("headerName: \"{0}\"", headerName);
            Console.WriteLine("webName: \"{0}\"", webName);
            Console.WriteLine("==========================================");
        }
    }
}
```
- https://rextester.com/l/csharp_online_compiler
  執行結果：
  ```
  bodyName: "iso-8859-1"
  codePage: 1252
  encodingName: "Western European (Windows)"
  headerName: "Windows-1252"
  webName: "Windows-1252"
  ==========================================
  bodyName: "iso-8859-1"
  codePage: 1252
  encodingName: "Western European (Windows)"
  headerName: "Windows-1252"
  webName: "Windows-1252"
  ==========================================
  ```
- Windows 10
  ```
  bodyName: "big5"
  codePage: 950
  encodingName: "繁體中文 (Big5)"
  headerName: "big5"
  webName: "big5"
  ==========================================
  bodyName: "big5"
  codePage: 950
  encodingName: "繁體中文 (Big5)"
  headerName: "big5"
  webName: "big5"
  ==========================================
  ```

## 參考資料
- [How does Encoding.Default work in .NET?](https://stackoverflow.com/questions/6006422/how-does-encoding-default-work-in-net)
