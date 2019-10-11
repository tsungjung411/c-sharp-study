```C#
//https://rextester.com/l/csharp_online_compiler
//Rextester.Program.Main is the entry point for your code. Don't change it.
//Compiler version 4.0.30319.17929 for Microsoft (R) .NET Framework 4.5

using System;

namespace Rextester
{
    class Multiplier {
        double Factor;
        public Multiplier(double factor) {
            this.Factor = factor;
        }
        public double Multiply(double x) {
            return x * this.Factor;
        }
    }
    
    public class Program
    {
        delegate double Function(double a);
        
        public static double Square(double a) {
            return a * a;
        }
        static double[] Apply(double[] a, Function f) {
            double[] results = new double[a.Length];
            for (int i = 0; i < a.Length; i++) {
                results[i] = f(a[i]);
            }
            return results;
        }
        
        public static void Main(string[] args)
        {
            double[] a = {0, 0.5, 1.0};
            Console.WriteLine("a: " + String.Join(" ", a));
            
            
            double[] squares = Apply(a, Square);
            Console.WriteLine("squares: " + String.Join(" ", squares));
            
            double[] sins = Apply(a, Math.Sin);
            Console.WriteLine("sins: " + String.Join(" ", sins));
            
            Multiplier m = new Multiplier(2);
            double[] ms = Apply(a, m.Multiply);
            Console.WriteLine("ms: " + String.Join(" ", ms));
        }
    }
}
```

## 參考資料
- [[csharp] 委派](https://docs.microsoft.com/zh-tw/dotnet/csharp/tour-of-csharp/delegates)
