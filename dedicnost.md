# Dědičnost
Definice rodičovské třídy:
```c#
class Rodic
{
  public string Prijmeni { get; set; }
  public string Bydliste { get; set; }
  
  public Rodic( string prijmeni, string bydliste )
  {
    Prijmeni = prijmeni;
    Bydliste = bydliste;
  }
}
```

Definice potomka:
```c#
class Potomek : Rodic
{
  public string Jmeno { get; set; }
  public Potomek( string jmeno, string prijmeni, string bydliste ) : base ( prijmeni, bydliste )
  {
    Jmeno = jmeno;
  }
}
```

Volání:
```c#
static void Main(string[] argc)
{
    string prijmeni = "Toman";
    string bydliste = "Senicka";
    
    Potomek dcera1 = new Potomek( "Kristyna", prijmeni+"ova", bydliste );
    Potomek dcera2 = new Potomek( "Jana", prijmeni+"ova", bydliste );
}
```
