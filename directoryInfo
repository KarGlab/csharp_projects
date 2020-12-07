using System;
using System.IO;
using System.Collections.Generic;

namespace ConsoleApp11
{
        
    class Program
    {
      
        static void Wczytaj(string sciezka)
        {
            DirectoryInfo di = new DirectoryInfo(sciezka);
            string sciezka2 = @"C:\Users\karol\Desktop\info.txt";

            foreach(var plik in di.GetFiles())
            {
                Console.WriteLine($"{plik.Name,-10}{plik.Extension,-10}{plik.CreationTime,-10}");
            }
            Console.WriteLine("Czy chcesz zapisać informacje do pliku?(t/n)");
            string wybor = Console.ReadLine();
            StreamWriter sw = new StreamWriter(sciezka2);
            if (wybor == "t")
            {
                foreach (var plik in di.GetFiles())
                {
                    sw.WriteLine($"{plik.Name};{plik.Extension};{plik.CreationTime};");
                }
                Console.WriteLine("Informacje pomyslnie zapisano do pliku");
            }
            sw.Close();

        }
        static void Main(string[] args)
        {
            string sciezka = @"C:\Users\karol\Desktop\Studia\Etyka Gospodarcza";
            Wczytaj(sciezka);
            Console.ReadLine();

        }
    }
}
