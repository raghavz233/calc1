using System.Threading.Channels;

namespace Calculator
{
    class Program
    {
        public static void addition (int a, int b)
        {
            int result = a+ b;
            Console.WriteLine(  "Addition Result is : {0}",result);
        }
        public static void subtraction(int a, int b)
        {
            int result = a - b;
            Console.WriteLine("subtraction Result is : {0}", result);
        }
        public static void multiplication(int a, int b)
        {
            int result = a * b;
            Console.WriteLine("multiplication Result is : {0}", result);
        }
        public static void division(int a, int b)
        {
            int result = a / b;
            Console.WriteLine("multiplication Result is : {0}", result);
        }
        private static void Main(string[] args)
        {
            Console.WriteLine("Enter first number");
            int num1 = int.Parse(Console.ReadLine());

            Console.WriteLine("Enter second number");
            int num2 = int.Parse(Console.ReadLine());

            Console.WriteLine("Enter operator");
            string op = Console.ReadLine();

            if (op.Equals("+"))
            {
                Program.addition(num1, num2);
            }
            else if (op.Equals("-"))
            {
                Program.subtraction(num1, num2);
            }
            else if (op.Equals("*"))
            {
                Program.multiplication(num1, num2);
            }
            else if (op.Equals("/"))
            {
                Program.division(num1, num2);
            }
            else
                Console.WriteLine("invalid");

            Console.ReadLine();
        }

    }




}
