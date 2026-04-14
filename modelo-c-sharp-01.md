using System;

public class RelatorioVendas
{
    public static void Main()
    {
        var total = 18990.50m;
        var meta = 15000m;
        var atingiuMeta = total >= meta;

        Console.WriteLine($"Total vendido: {total:C}");
        Console.WriteLine($"Meta atingida? {atingiuMeta}");
    }
}
