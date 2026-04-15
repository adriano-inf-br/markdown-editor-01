using System;

public class ResumoPedidos
{
    public static void Main()
    {
        var pendentes = 12;
        var enviados = 21;
        var totalHoje = 3490.75m;

        Console.WriteLine($"Pendentes: {pendentes}");
        Console.WriteLine($"Enviados: {enviados}");
        Console.WriteLine($"Faturamento do dia: {totalHoje:C}");
    }
}
