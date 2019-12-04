# CardMagic
 Program that guesses your card



using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace CardMagic
{
    class Program
    {

        
       
        
        static void Main(string[] args)
        {

            List<string> Cards = new List<string>() { "A<3 ", "2<3 ", "3<3 ", "4<3 ", "5<3 ", "6<3 ", "7<3 ", "8<3 ", "9<3 ", "10<3 ", "J<3 ", "Q<3 ", "K<3 ", "A<> ", "2<> ", "3<> ", "4<> ", "5<> ", "6<> ", "7<> ", "8<> " };
            List<string> pileone = new List<string>();
            List<string> piletwo = new List<string>();
            List<string> pilethree = new List<string>();


            Console.WriteLine("Rules: Here is 21 Cards. Pick one to Remember");
            Console.WriteLine("Press the 1 Or 2 or 3 Button Depending of what Pile your card is");
            Console.WriteLine("");

            shuffle(Cards);

            Inputpileone(Cards,pileone,piletwo,pilethree);

            Printpiles(pileone,piletwo,pilethree);
            Cards.Clear();
            ChoosePile(Cards, pileone, piletwo, pilethree);
            pileone.Clear();
            piletwo.Clear();
            pilethree.Clear();
            Console.Clear();

            Console.WriteLine("Press the 1 Or 2 or 3 Button Depending of what Pile your card is now");
            Console.WriteLine("");

            Inputpileone(Cards, pileone, piletwo, pilethree);
            Printpiles(pileone, piletwo, pilethree);
            Cards.Clear();
            ChoosePile(Cards, pileone, piletwo, pilethree);
            pileone.Clear();
            piletwo.Clear();
            pilethree.Clear();
            Console.Clear();



            Console.WriteLine("Again Press the 1 Or 2 or 3 Button Depending of what Pile your card is now");
            Console.WriteLine("");
            Inputpileone(Cards, pileone, piletwo, pilethree);
            Printpiles(pileone, piletwo, pilethree);
            Cards.Clear();
            ChoosePile(Cards, pileone, piletwo, pilethree);


            Console.Clear();

          
            Console.WriteLine("your card was " + Cards[10]);


            Console.ReadLine();
        }



        static void shuffle(List<string> cards)
        {
            Random random = new Random();
            int n = cards.Count;

            for (int i = cards.Count - 1; i > 1; i--)
            {
                int rnd = random.Next(i + 1);

                string value = cards[rnd];
                cards[rnd] = cards[i];
                cards[i] = value;
            }
        }

        static void Inputpileone(List<string> cards, List<string> pile,List<string> pile2, List<string> pile3)
        {
            for (int i = 0; i < 21; i++)
            {
                switch (i)
                {
                    case 0:
                        pile.Add(cards[i]);
                        break;
                    case 1:
                        pile2.Add(cards[i]);
                        break;
                    case 2:
                        pile3.Add(cards[i]);
                        break;
                    case 3:
                        pile.Add(cards[i]);
                        break;
                    case 4:
                        pile2.Add(cards[i]);
                        break;
                    case 5:
                        pile3.Add(cards[i]);
                        break;
                    case 6:
                        pile.Add(cards[i]);
                        break;
                    case 7:
                        pile2.Add(cards[i]);
                        break;
                    case 8:
                        pile3.Add(cards[i]);
                        break;
                    case 9:
                        pile.Add(cards[i]);
                        break;
                    case 10:
                        pile2.Add(cards[i]);
                        break;
                    case 11:
                        pile3.Add(cards[i]);
                        break;
                    case 12:
                        pile.Add(cards[i]);
                        break;
                    case 13:
                        pile2.Add(cards[i]);
                        break;
                    case 14:
                        pile3.Add(cards[i]);
                        break;
                    case 15:
                        pile.Add(cards[i]);
                        break;
                    case 16:
                        pile2.Add(cards[i]);
                        break;
                    case 17:
                        pile3.Add(cards[i]);
                        break;
                    case 18:
                        pile.Add(cards[i]);
                        break;
                    case 19:
                        pile2.Add(cards[i]);
                        break;
                    case 20:
                        pile3.Add(cards[i]);
                        break;
                    case 21:
                        pile.Add(cards[i]);
                        break;
                    default:
                        Console.WriteLine("Default case");
                        break;
                }
            }
        }

        static void Printpiles(List<string> pile, List<string> pile2, List<string> pile3)
        {
            Console.WriteLine("");
            Console.WriteLine("Pile Nr1: ");
            foreach (string value in pile)
            {
                Console.Write(" {0} ", value);

            }
            Console.WriteLine("");
            Console.WriteLine("");
            Console.WriteLine("Pile Nr2: ");
            foreach (string value in pile2)
            {
                Console.Write(" {0} ", value);

            }
            Console.WriteLine("");
            Console.WriteLine("");
            Console.WriteLine("Pile Nr3: ");
            foreach (string value in pile3)
            {
                Console.Write(" {0} ", value);

            }
        }

        static void ChoosePile(List<string> cards, List<string> pile, List<string> pile2, List<string> pile3)
        {
            Console.WriteLine(" ");
            string input = Console.ReadLine();
          

            switch (input)
            {
                case "1":

                    for (int i = 0; i < pile.Count; i++)
                    {
                        cards.Add(pile2[i]);
                    }
                    for (int i = 0; i < pile.Count; i++)
                    {
                        cards.Add(pile[i]);
                    }
                    for (int i = 0; i < pile.Count; i++)
                    {
                        cards.Add(pile3[i]);
                    }
                    break;

                case "2":
                    for (int i = 0; i < pile.Count; i++)
                    {
                        cards.Add(pile[i]);
                    }
                    for (int i = 0; i < pile.Count; i++)
                    {
                        cards.Add(pile2[i]);
                    }
                    for (int i = 0; i < pile.Count; i++)
                    {
                        cards.Add(pile3[i]);
                    }
                    break;
                case "3":
                    for (int i = 0; i < pile.Count; i++)
                    {
                        cards.Add(pile[i]);
                    }
                    for (int i = 0; i < pile.Count; i++)
                    {
                        cards.Add(pile3[i]);
                    }
                    for (int i = 0; i < pile.Count; i++)
                    {
                        cards.Add(pile2[i]);
                    }
                    break;

                default:
                    Console.WriteLine(" You did not type 1 or 2 or 3");
                    Console.WriteLine();
                    Console.ReadLine();
                    break;
            }
        }

    }
}
