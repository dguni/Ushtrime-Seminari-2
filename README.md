# Ushtrime-Seminari-2
//Ush1
using System;
class Program
{
    static void Main(String[] args)
    {
        Console.WriteLine("Jepni nje numer: ");
        int n = Convert.ToInt32(Console.ReadLine());
        for (int i = 1; i <= n; i++)
        {
            Console.WriteLine(i + " ");
        }
        Console.WriteLine();
    }
}

//Ush1: Using while
using System;
class Program
{
    static void Main(String[] args)
    {
        Console.WriteLine("Jepni nje numer: ");
        int n = Convert.ToInt32(Console.ReadLine());
        int i = 1;
        while (i <= n)
        {
            Console.WriteLine(i + " ");
            i++;
        }
        Console.WriteLine();
    }
}

//Ush2
using System;
class Program
{
    static void Main(String[] args)
    {
        Console.WriteLine("Jepni numrin e pare: ");
        int nr1 = Convert.ToInt32(Console.ReadLine());
        Console.WriteLine("Jepni numrin e dyte: ");
        int nr2 = Convert.ToInt32(Console.ReadLine());
        Console.WriteLine("Jepni numrin e trete: ");
        int nr3 = Convert.ToInt32(Console.ReadLine());

        int max = nr1;
        if (nr2 > max)
        {
            max = nr2;
        }
        if (nr3 > max)
        {
            max = nr3;
        }
        Console.WriteLine($"Nr me i madh eshte: {max}");

    }
}

//Ush3
using System;
class Program
{
    static void Main(String[] args)
    {
        Console.WriteLine("Jepni nje numer: ");
        int nr = Convert.ToInt32(Console.ReadLine());

        int count = 0;
        do
        {
            nr /= 10;
            count++;
        }
        while (nr > 0);

        Console.WriteLine($"Numri i shifrave eshte: {count}");
    }
}

//Ush4
using System;
class Program
{
    static void Main(String[] args)
    {
        Console.WriteLine("Jepni nje vit: ");
        int viti = Convert.ToInt32(Console.ReadLine());

        if (viti % 4 == 0)
        {
            if (viti % 100 == 0)
            {
                if (viti % 400 == 0)
                {
                    Console.WriteLine($"Viti eshte i brishte: {viti}");
                }
                else
                {
                    Console.WriteLine($"{viti} nuk eshte vit i brishte");
                }
            }
            else
            {
                Console.WriteLine($"Viti eshte i brishte: {viti}");
            }
        }
        else
        {
            Console.WriteLine($"{viti} nuk eshte vit i brishte");
        }
    }
}

//Ush5
using System;
class Program
{
    static void Main(String[] args)
    {
        Console.WriteLine("Shkruani nje fjale");
        string fjala = Console.ReadLine();
        bool isEqual = true;
        char a = fjala[0];

        for (int i = 1; i < fjala.Length; i++)
        {
            char b = fjala[i];
            if (b != a)
            {
                isEqual = false;
            }
        }

        Console.WriteLine(isEqual);
    }
}

//Ush6
using System;
using System.ComponentModel;
class Program
{
    static void Main(String[] args)
    {
        Console.WriteLine("Shkruani numrin: ");
        int n = Convert.ToInt32(Console.ReadLine());

        Console.WriteLine($"Numrat cift nga 1 te {n}");
        for (int i = 1; i <= n; i++)
        {
            if (i % 2 == 0)
            {
                Console.WriteLine(i);
            }
        }

    }
}

//Ush7
using System;
class Program
{
    static void Main()
    {
        Console.Write("Shkruani nje numer: ");
        int n = Convert.ToInt32(Console.ReadLine());

        Console.WriteLine($"Tabela e shumezimit per {n}:");

        for (int i = 1; i <= n; i++)
        {
            for (int j = 1; j <= n; j++)
            {
                Console.Write($"{i * j}\t");
            }
            Console.WriteLine();
        }
    }
}

//Ush8
using System;

class Program
{
    static void Main()
    {
        Console.Write("Shkruani një fjali: ");
        string fjalia = Console.ReadLine();
        if (string.IsNullOrWhiteSpace(fjalia))
        {
            Console.WriteLine("Ju nuk keni shkruar një fjali!");
            return;
        }
        string[] fjalet = fjalia.Split(' ', StringSplitOptions.RemoveEmptyEntries);
        int numriFjaleve = fjalet.Length;
        Console.WriteLine("Numri i fjalëve në fjalinë tuaj është: " + numriFjaleve);
    }
}

//Ush9
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Shkruani numrin e pare:");
        double numri1 = Convert.ToDouble(Console.ReadLine());

        Console.WriteLine("Shkruani numrin e dyte:");
        double numri2 = Convert.ToDouble(Console.ReadLine());


        Console.WriteLine("Zgjidhni nje operator (+, -, *, /):");
        char operatori = Console.ReadLine()[0];

        double rezultati = 0;
        bool llogaritjaESuksesshme = true;

        switch (operatori)
        {
            case '+':
                rezultati = numri1 + numri2;
                break;
            case '-':
                rezultati = numri1 - numri2;
                break;
            case '*':
                rezultati = numri1 * numri2;
                break;
            case '/':
                if (numri2 != 0)
                {
                    rezultati = numri1 / numri2;
                }
                else
                {
                    Console.WriteLine("Gabim: Nuk mund te pjesetohet me zero!");
                    llogaritjaESuksesshme = false;
                }
                break;
            default:
                Console.WriteLine("Gabim: Operator i pavlefshem!");
                llogaritjaESuksesshme = false;
                break;
        }


        if (llogaritjaESuksesshme)
        {
            Console.WriteLine($"Rezultati: {numri1} {operatori} {numri2} = {rezultati}");
        }
    }
}
//Ush10
using System;

class Program
{
    static void Main()
    {

        Console.WriteLine("Shkruani nje numer te plote:");
        int numri = Convert.ToInt32(Console.ReadLine());


        int numriReverse = BejReverse(numri);


        Console.WriteLine($"Numri i bere reverse eshtë: {numriReverse}");
    }

    static int BejReverse(int numri)
    {
        int numriReverse = 0;


        while (numri != 0)
        {
            int shifra = numri % 10;
            numriReverse = numriReverse * 10 + shifra; kundert
            numri = numri / 10;
        }

        return numriReverse;
    }
}

//Ush11
using System;

class Program
{
    static void Main()
    {

        Console.WriteLine("Shkruani një numer per te llogaritur faktorialin:");
        int numri = int.Parse(Console.ReadLine());

        long faktoriali = 1;
        for (int i = 1; i <= numri; i++)
        {
            faktoriali *= i;
        }

        Console.WriteLine($"Faktoriali i {numri} eshte: {faktoriali}");
    }
}
//Ush12
using System;
class Program
{
    static void Main()
    {
        Console.WriteLine("Shkruani një fjale ose fjali për të kontrolluar nese eshte palindrome:");
        string input = Console.ReadLine();

        if (EshtePalindrom(input))
        {
            Console.WriteLine($"'{input}' eshtë palindrome!");
        }
        else
        {
            Console.WriteLine($"'{input}' nuk eshte palindrome.");
        }
    }

    static bool EshtePalindrom(string str)
    {
        str = str.Replace(" ", "").ToLower();


        string kunderta = "";
        for (int i = str.Length - 1; i >= 0; i--)
        {
            kunderta += str[i];
        }

        return str == kunderta;
    }
}
//Ush13
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Shkruani nje numer nga 1 deri në 7 per te pare diten perkatese te javes:");
        int dita = Convert.ToInt32(Console.ReadLine());
        switch (dita)
        {
            case 1:
                Console.WriteLine("E Hene");
                break;
            case 2:
                Console.WriteLine("E Marte");
                break;
            case 3:
                Console.WriteLine("E Merkure");
                break;
            case 4:
                Console.WriteLine("E Enjte");
                break;
            case 5:
                Console.WriteLine("E Premte");
                break;
            case 6:
                Console.WriteLine("E Shtune");
                break;
            case 7:
                Console.WriteLine("E Diele");
                break;
            default:
                Console.WriteLine("Numri i dhene eshtë i pavlefshem. Ju lutem shkruani nje numer nga 1 deri ne 7.");
                break;
        }
    }
}

//Ush14
using System;

class Program
{
    static void Main()
    {
        
        Console.WriteLine("Shkruani lartesinë e piramides (n):");
        int n = Convert.ToInt32(Console.ReadLine());

        
        for (int i = 1; i <= n; i++) 
        {
            
            for (int j = 1; j <= n - i; j++)
            {
                Console.Write(" "); 
            }
            for (int j = 1; j <= i; j++)
            {
                Console.Write(j);
            }
            for (int j = i - 1; j >= 1; j--)
            {
                Console.Write(j);
            }
            Console.WriteLine();
        }
    }
}





