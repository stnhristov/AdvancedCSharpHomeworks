using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Problem_03
{
    class CategorizeNumbers
    {
        static void Main(string[] args)
        {
            string[] array = Console.ReadLine().Split(' ');
            double[] numbersArray = new double[array.Length];
            for (int i = 0; i < array.Length; i++) 
            {
                numbersArray[i] = Convert.ToDouble(array[i]);
            }
            List<double> firstCol = new List<double>();
            List<double> secondCol = new List<double>();
            for (int i = 0; i < numbersArray.Length; i++) 
            {
                if (numbersArray[i] % 1 == 0)
                {
                    secondCol.Add(numbersArray[i]);
                }
                else 
                {
                    firstCol.Add(numbersArray[i]);
                }
            }
            Console.Write("[ ");
            foreach (var n in firstCol)
            {
                Console.Write(n+" ");
            }
            Console.Write("] ->");
            Console.WriteLine("min: {0}, max: {1}, sum: {2}, avg: {3:F2}",firstCol.Min(),firstCol.Max(),firstCol.Sum(),firstCol.Average());
            Console.WriteLine();
            Console.Write("[ ");
            foreach (var n in secondCol)
            {
                Console.Write(n + " ");
            }
            Console.Write("] ->");
            Console.WriteLine("min: {0}, max: {1}, sum: {2}, avg: {3:F2}",secondCol.Min(),secondCol.Max(),secondCol.Sum(),secondCol.Average());
        }
    }
}

