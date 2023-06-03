using System;

namespace GuessTheNumber
{
    class Program
    {
        static void Main(string[] args)
        {
            Random random = new Random();
            int secretNumber = random.Next(1, 101);  // Número aleatorio entre 1 y 100

            Console.WriteLine("Adivina el número del 1 al 100");

            int guess;
            do
            {
                Console.Write("Introduce tu conjetura: ");
                guess = int.Parse(Console.ReadLine());

                if (guess < secretNumber)
                {
                    Console.WriteLine("Demasiado bajo.");
                }
                else if (guess > secretNumber)
                {
                    Console.WriteLine("Demasiado alto.");
                }
            } while (guess != secretNumber);

            Console.WriteLine("¡Felicidades! Has adivinado el número secreto.");
        }
    }
}
