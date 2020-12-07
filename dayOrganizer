using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Threading;

namespace ConsoleApp11
{ 
    enum DniTygodnia
    {
        Poniedzialek,
        Wtorek,
        Sroda,
        Czwartek,
        Piatek,
        Sobota,
        Niedziela,
        Brak

    }
    struct Zadania
    {
        public static DniTygodnia KtoryDzienTygodnia(int dzien)
        {
            switch(dzien)
            {
                case 1:
                    return DniTygodnia.Poniedzialek;
                case 2:
                    return DniTygodnia.Wtorek;
                case 3:
                    return DniTygodnia.Sroda;
                case 4:
                    return DniTygodnia.Czwartek;
                case 5:
                    return DniTygodnia.Piatek;
                case 6:
                    return DniTygodnia.Sobota;
                case 7:
                    return DniTygodnia.Niedziela;
                default:
                    return DniTygodnia.Brak;
            }
        }
        public static string ZaplanujZadanie()
        {
            return Console.ReadLine();
        }
    }
   
    class Program
    {
        static void SprawdzZadanie(string[] tab)
        {
            string odpowiedz;
            do
            {
                Console.WriteLine("Jaki dzień tygodnia chcesz sprawdzić?(1-7)");
                int dzien = int.Parse(Console.ReadLine());
                switch (dzien)
                {
                    case 1:
                        Console.WriteLine(DniTygodnia.Poniedzialek +": " + tab[dzien-1]);
                        break;
                    case 2:
                        Console.WriteLine(DniTygodnia.Wtorek+": "+tab[dzien-1]);
                        break;
                    case 3:
                        Console.WriteLine(DniTygodnia.Sroda+": "+tab[dzien-1]);
                        break;
                    case 4:
                        Console.WriteLine(DniTygodnia.Czwartek+": "+tab[dzien-1]);
                        break;
                    case 5:
                        Console.WriteLine(DniTygodnia.Piatek+": "+tab[dzien-1]);
                        break;
                    case 6:
                        Console.WriteLine(DniTygodnia.Sobota+": "+tab[dzien-1]);
                        break;
                    case 7:
                        Console.WriteLine(DniTygodnia.Niedziela+": "+tab[dzien-1]);
                        break;
                    default:
                        Console.WriteLine("Podałeś złą cyfrę");
                        break;

                }
                Console.WriteLine("Chcesz sprawdzić inny dzień tygodnia?(t/n)");
                odpowiedz = Console.ReadLine();


            } while (odpowiedz != "n");
        }
        static void Main(string[] args)
        {
            Console.WriteLine("Wpisz zadania na tydzien");
            string[] dniTygodnia = new string[7];
            for(int i = 0; i < dniTygodnia.Length; i++)
            {
                Console.WriteLine(Zadania.KtoryDzienTygodnia(i+1));
                dniTygodnia[i] = Zadania.ZaplanujZadanie();
            }
            Console.Clear();
            SprawdzZadanie(dniTygodnia);
            Console.ReadKey();
        }
    }

}
