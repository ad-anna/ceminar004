# ceminar004

// Задача 25: Напишите цикл, который принимает на вход два числа (A и B) и возводит число A в натуральную степень B.

Console.Clear();

Console.WriteLine("Введите число");
int A = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Введите степень числа");
int B = Convert.ToInt32(Console.ReadLine());

RaiseNumberRoot(A, B);

void RaiseNumberRoot(int A, int B)
{
    Console.Write(Math.Pow(A, B) + " ");       
}

// Задача 27: Напишите программу, которая принимает на вход число и выдаёт сумму цифр в числе.

Console.Clear();

Console.WriteLine("Введите число N");
int number = Convert.ToInt32(Console.ReadLine());
int len = GetNumberLen(number);
GetSumNumbers(number, len);

int GetNumberLen(int number)
{
    int index = 0;
    while (number > 0)
    {
        number /= 10;
        index++;
    }
    return index;
}


void GetSumNumbers(int number, int len)
{
    int sum = 0;
    for (int i = 0; i <= len; i++)
    {
        sum += number % 10;
        number /= 10;
    }
    Console.WriteLine(sum);
}    

// Задача 29: Напишите программу, которая задаёт массив из 8 элементов и выводит их на экран. 

int[] randomArray = new int[8];
for (int i = 0; i <= 8; i++)
{
    randomArray[i] = new Random().Next(1,1000);
    Console.Write(randomArray[i] + " ");
}
