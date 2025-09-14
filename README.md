<p align="center">
  <img src="https://media.discordapp.net/attachments/1416655767104393330/1416661590304096368/unnamed-Photoroom_1.png?ex=68c7a86b&is=68c656eb&hm=73bada98bbfc5a63967bced7b3a9a9b08519fb71088a281f1ffc5afeec7535e3&=&format=webp&quality=lossless" width="500" alt="Logo"/>
</p>
<h1 align="center">หลักการเขียนโปรแกรมคอมพิวเตอร์ C#.NET</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Language-C%23-178600?style=for-the-badge&logo=csharp&logoColor=white"/>
  <img src="https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white"/>
  <img src="https://img.shields.io/badge/IDE-Visual%20Studio-5C2D91?style=for-the-badge&logo=visualstudio&logoColor=white"/>
</p>

---

## 🚀 ส่งงาน8 -  เขียนโปรแกรมใช้ for loop


```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        // ข้อ 1
        Console.WriteLine("1 - Program for display number");
        Console.Write("What is last number? ");
        int lastNumber = int.Parse(Console.ReadLine());

        Console.WriteLine("Output :");
        for (int i = 1; i <= lastNumber; i++)
        {
            Console.Write(i + " ");
        }
        Console.WriteLine();

        // ข้อ 2
        Console.WriteLine("\n2 - Program for display number (5 numbers per line)");
        Console.Write("What is last number? ");
        int lastNumber2 = int.Parse(Console.ReadLine());

        Console.WriteLine("Output :");
        for (int i = 1; i <= lastNumber2; i++)
        {
            Console.Write(i + " ");
            if (i % 5 == 0)
            {
                Console.WriteLine();
            }
        }
        Console.WriteLine();

        // ข้อ 3
        
        int countGreaterOrEqual50 = 0;
        int countLess50 = 0;
        string inputNumbers = "";

        for (int i = 0; i < 6; i++)
        {
            Console.Write("Input your number? ");
            int number = int.Parse(Console.ReadLine());
            
            if (i > 0)
            {
                inputNumbers += " ";
            }
            inputNumbers += number;

            if (number >= 50)
            {
                countGreaterOrEqual50++;
            }
            else
            {
                countLess50++;
            }
        }

        Console.WriteLine("\nOutput");
        Console.WriteLine("Your input number is " + inputNumbers);
        Console.WriteLine("Count of Number is greater or equal than 50 = " + countGreaterOrEqual50);
        Console.WriteLine("Count of Number is less than 50 = " + countLess50);

        // ข้อ 4
        
        int sum = 0;
        string formula = "";

        for (int i = 1; i <= 49; i += 4)
        {
            sum += i;
            if (formula.Length > 0)
            {
                formula += " + ";
            }
            formula += i;
            Console.WriteLine(formula + " = " + sum);
        }

        // ข้อ 5
        
        Console.Write("NUMBER FOR FIND FACTORIAL : ");
        int factorialNumber = int.Parse(Console.ReadLine());

        long factorial = 1;
        string formulaFactorial = "";

        for (int i = factorialNumber; i >= 1; i--)
        {
            factorial *= i;
            if (i < factorialNumber)
            {
                formulaFactorial += " x ";
            }
            formulaFactorial += i;
        }

        Console.WriteLine("OUTPUT :");
        Console.WriteLine("\t" + factorialNumber + "! = " + formulaFactorial + " = " + factorial);

        Console.ReadKey();
    }
}
```

## 🚀 ส่งงาน9 -  เขียนโปรแกรม loop หลายชั้น
```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
    	//ข้อ1
        Console.Write("Start number : ");
        int startNumber = int.Parse(Console.ReadLine());

        Console.Write("Last number : ");
        int lastNumber = int.Parse(Console.ReadLine());
        
        for (int i = startNumber; i <= lastNumber; i++)
        {
            Console.WriteLine("\tMultiply " + i);
            for (int j = 1; j <= 12; j++)
            {
                Console.WriteLine("\t"+i + " x " + j + " = " + (i * j));
            }
            Console.WriteLine("---------------------------");
        }
        //ข้อ2
        Console.Write("Row : ");
        int rows = int.Parse(Console.ReadLine());
        Console.ForegroundColor = ConsoleColor.Green;
        
        string[] symbols = { "&", "#", "@" };

        for (int i = 1; i <= rows; i++)
        {
            if (i % 5 == 0)
            {
                
                Console.WriteLine("C o m p u t e r S c i e n c e");
                
            }
            else
            {
                for (int j = 0; j < i; j++)
                {
                    Console.Write(symbols[j % symbols.Length] + " ");
                }
                Console.WriteLine();
            }
        }
        Console.ResetColor();
        //ข้อ3
        Console.Write("Christmas bush: ");
        int bushCount = int.Parse(Console.ReadLine());

        if (bushCount <= 2)
        {
            Console.WriteLine("\terror christmas bush!!!");
        }
        else
        {
            for (int b = 1; b <= bushCount; b++)
            {
                for (int i = 1; i <= bushCount; i++)
                {
                    for (int space = bushCount + bushCount - i - b; space > 0; space--)
                    {
                        Console.Write(" ");
                    }

                    for (int j = 1; j <= i + (b - 1); j++)
                    {
                        Console.Write(j + " ");
                    }
                    Console.WriteLine();
                }
            }

            string trunk = "";
            for (int i = 1; i <= bushCount - 2; i++)
            {
                trunk += i.ToString();
            }

            int trunkHeight = bushCount;
            int totalWidth = bushCount * 2;

            for (int i = 0; i < trunkHeight; i++)
            {
                Console.Write(new string(' ', totalWidth - (trunk.Length / 2)));
                Console.WriteLine(trunk);
            }
        }

        Console.WriteLine("\nPress any key to exit program");
        Console.ReadKey();
    }
}

```
