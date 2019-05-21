# Upcasting
Rodičovská třída:
```c#
class Osoba
{
  public string Jmeno { get; set; }
  public Osoba( string jmeno )
  {
    Jmeno = jmeno;
  }
}
```

Potomek:
```c#
class Student : Osoba
{
  public byte Rocnik { get; set; }
  public Student( string jmeno, byte rocnik ) : base (jmeno)
  {
    rocnik = Rocnik;
  }
}
```

Reference třídy
```c#
static void Main(string[] argc)
{
     Student prvak = new Student( "Anicka", 2 );
     Osoba prvakJeOsoba = prvak; //upcasting
}
```
na Aničku ukazují dva pointry - Anička je student a zároveň i osoba
