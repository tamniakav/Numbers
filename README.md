# Numbers
Just another repository
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Numbers
{
    class Numbers
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            int sum = n;

            int firstNum = n / 100;
            int secondNum = (n / 10) % 10;
            int thirdNum = n % 10;

            int firstLoop = firstNum + secondNum;
            int secondLoop = firstNum + thirdNum;

            for (int i = 0; i < firstLoop; i++)
            {
                for (int j = 0; j < secondLoop; j++)
                {
                    if (sum % 5 == 0)
                    {
                        sum -= firstNum;
                    }
                    else if (sum % 3 == 0)
                    {
                        sum -= secondNum;
                    }
                    else
                    {
                        sum += thirdNum;
                    }

                    Console.Write($"{sum} ");
                }
                Console.WriteLine();
            }
        }
    }
}
