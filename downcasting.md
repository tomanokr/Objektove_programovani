# Downcasting
používáme při zjišťování, zda upcastovaná třída má referenci i na daného potomka
```c#
class Osoba
{
  public string Jmeno { get; set; }
  public Osoba( string jmeno )
  {
    Jmeno = jmeno;
  }
}
class Student : Osoba
{
  public byte Rocnik { get; set; }
  public Student( string jmeno, byte rocnik ) : base ( rocnik )
  {
    Rocnik = rocnik;
  }
}
class Zamestnanec : Osoba
{
  public string Kancelar{ get; set; }
  public Zamestnanec( string jmeno, string kancelar ) : base ( kancelar )
  {
     Kancelar = kancelar;
  }
}
class Program
{
  public void Vypis( Osoba osoba )
  {
    Console.Write( osoba.Jmeno );
    if ( osoba is Student student )
    {
       Console.WriteLine($" {student.Rocnik}. rocnik");
    }
    else Console.WriteLine();
  }
  static void Main( string[] argc )
  {
    Zamestnanec ucitel = new Zamestnanec( "Kral", "nejaka" );
    Student prvak = new Student( "Anicka", 2 );
    
    Vypis( ucitel );
    Vypis( prvak );
  }
}
```
Reference jako downcasting
```c#
Zamestnanec ucitel = osoba as Zamestnanec //pokud nema referenci, pak ucitel == NULL
//nebo
if (osoba is Zamestnanec ucitel) // predchozi metoda s overenim, zda je ucitel != NULL
```
