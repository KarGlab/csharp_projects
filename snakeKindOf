using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Threading;

namespace ConsoleApp11
{
    class Program
    {
        static void Main(string[] args)
        {
            Random rnd = new Random();
            int wh = rnd.Next(1, Console.WindowHeight);
            const int liczbaElementow = 6;
            char[] literki = new char[liczbaElementow];
            int[] kolumny = new int[liczbaElementow];
            //wyswietlanie literek ktore waz ma zjesc
            for (int i = 0; i < literki.Length; i++)
            {
                //zapisanie w tablicy w ktorych kolumnach pojawiaja sie literki
                kolumny[i] = rnd.Next(1, Console.WindowWidth);
                Console.SetCursorPosition(kolumny[i], wh);
                //zapisanie w tablicy literek, ktore sie pojawią
                literki[i] = Convert.ToChar(rnd.Next(65, 91));
                Console.Write(literki[i]);
                kolumny[i] = kolumny[i];
            }
            int spacja = 1;
            string snek = ">";
            for (int i = 0; i < Console.WindowWidth - liczbaElementow; i++)
            {
                for (int j = 0; j < kolumny.Length; j++)
                {
                    //ten if jest po to, zeby literki byly zjadane przy zetknieciu sie z glowa weza
                    if (kolumny[j] - spacja == i)
                    {
                        //waz jest ciagiem znakow, do ktorego dodaje kolejne literki z tablicy literek ktore sie pojawily
                        snek = literki[j] + snek;
                        //a to w sumie liczy ilosc spacji i jest glownie do tego ifa wyzej
                        spacja++;
                        break;
                    }
                }
                //ustawianie kursora tak zeby to dawalo obraz przesuwania się tak jakby
                Console.SetCursorPosition(i, wh);
                Thread.Sleep(100);
                //ta spacja sprawia ze waz sie przesuwa
                Console.Write(" ");
                Console.Write(snek);
            }

            Console.ReadKey();
        }
    }

}
