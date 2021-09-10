# Deliverable-1using System;

namespace Deliverable1
{
    class Program
    {
        static void Main(string[] args)
        {
            bool executeProgram = true;

            do
            {
                // ask user to enter measurement type
                Console.WriteLine("Enter a measurement type: ");

                // user input measurement type
                string measurementType = Console.ReadLine();

                // ask user for an amount
                Console.WriteLine("enter amount: ");

                // user input for amount
                string amount = Console.ReadLine();

                // convert and store amount from string into number (decimal)
                double newAmount = Convert.ToDouble(amount);

                // convert entered number into correct new unit
                if (measurementType == "inch")
                {
                    // convert inch to fidget spinner
                    double result = newAmount * 3.5;
                    Console.WriteLine(newAmount + " inches is " + result + " fidget spinners");
                }
                else if (measurementType == "fidget spinner")
                {
                    // convert fidget spinner to inch
                    double result = newAmount / 3.5;
                    Console.WriteLine(newAmount + " fidget spinners is " + result + " inches");
                }
                else if (measurementType == "meme")
                {
                    // convert meme to foot
                    double result = newAmount / 5;
                    Console.WriteLine(newAmount + " memes is " + result + " feet");
                }
                else if (measurementType == "foot")
                {
                    // convert foot to meme
                    double result = newAmount * 5;
                    Console.WriteLine(newAmount + " feet is " + result + " memes");

                }

                // ask if they want to calculate again
                Console.WriteLine("calculate again?");
                string userResponse = Console.ReadLine();

                // is the user response yes? If so, repeat loop skip if statement.
                // if not yes, set value to false and stop loop.
                if(userResponse != "yes")
                {
                    executeProgram = false;
                }


            } while (executeProgram);


        }
    }
}
