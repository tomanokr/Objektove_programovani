# Statické metody a členské prvky
nepotřebují existující objekt

```#c
class Vypocty
{
    public static double Soucet(double x, double y)
    {
      return x+y;
    }
}
```

volají se pomocí třídy
```#c
class Program
{
  static void Main(string[] argc)
  {
      double vysledek = Vypocty.Soucet( 4.0, 3.2 );
  }
}
```
