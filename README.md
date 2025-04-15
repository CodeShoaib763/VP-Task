# VP-Task
 
using System;

namespace VariableDemo
{
   
    class VariableExample
    {
        
        private static string globalMessage = "Hello from the Global Variable!";
        private static int globalCounter = 100;

       
        static void Main(string[] args)
        {
            Console.WriteLine("=== Global Variables ===");
            Console.WriteLine($"Global Message: {globalMessage}");
            Console.WriteLine($"Global Counter: {globalCounter}");

            Console.WriteLine("\n=== Local Variables in Main ===");
            string localMessage = "Hello from the Local Variable in Main!";
            int localCounter = 10;

            Console.WriteLine($"Local Message: {localMessage}");
            Console.WriteLine($"Local Counter: {localCounter}");

            Console.WriteLine("\nCalling another method...\n");
            ShowLocalVariables();

            Console.WriteLine("\nProgram ended.");
        }

        
        static void ShowLocalVariables()
        {
            
            string localMethodMessage = "This is a local variable in ShowLocalVariables()";
            int methodResult = globalCounter + 50;

            Console.WriteLine("=== Local Variables in ShowLocalVariables ===");
            Console.WriteLine($"Local Message: {localMethodMessage}");
            Console.WriteLine($"Using Global Variable inside method: globalCounter + 50 = {methodResult}");
        }
    }
}
