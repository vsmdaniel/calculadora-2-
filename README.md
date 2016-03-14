# calculadora-2-
safdasdasdasd
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication3
{
    class Program
    {
        static void Main(string[] args)
        {
            double result;

            for (; ; )
            {
                Console.Write("Digite um número: ");
                double num1 = double.Parse(Console.ReadLine());

                Console.Write("\nEscolha a operação: ");
                char opp = char.Parse(Console.ReadLine());

                if (opp != 'R')
                {
                    Console.Write("\nDigite outro número: ");
                    double num2 = double.Parse(Console.ReadLine());

                    if (opp == '+')
                    {
                        Console.ForegroundColor = ConsoleColor.Green;
                        result = num1 + num2;
                        Console.WriteLine("\nO resultado da operação é: " + result);
                    }
                    else if (opp == '-')
                    {
                        Console.ForegroundColor = ConsoleColor.Blue;
                        result = num1 - num2;
                        Console.WriteLine("\nO resultador da operação é: " + result);
                    }
                    else if (opp == '*')
                    {

                        Console.ForegroundColor = ConsoleColor.Red;
                        result = num1 * num2;
                        Console.WriteLine("\nO resultaldo da operação é: " + result);

                    }
                    else if (opp == '/')
                    {
                        Console.ForegroundColor = ConsoleColor.Yellow;
                        result = num1 / num2;
                        Console.WriteLine("\nO resultaldo da operação é: " + result);
                    }
                    else if (opp == '^')
                    {
                        Console.ForegroundColor = ConsoleColor.Yellow;
                        result = Math.Pow(num1, num2);
                        Console.WriteLine("\nO resultaldo da operação é: " + result);
                    }
                }
                else if (opp == 'R')
                {
                    Console.ForegroundColor = ConsoleColor.DarkGray;
                    result = Math.Sqrt(num1);
                    Console.WriteLine("\nO resultaldo da operação é: " + result);
                }

                Console.ForegroundColor = ConsoleColor.Gray;
                Console.Write("\n");

                if (Console.ReadKey().Key == ConsoleKey.Spacebar)
                {
                    break;
                }
            }
        }
    }
}
