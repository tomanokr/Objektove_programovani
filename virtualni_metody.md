# Virtuální metody
slouží potomkům k překrývání rodičovských metod pomocí slov `virtual` a `override`
```c#
class Produkt
{
  public string Nazev { get; set; }
  public Produkt( string nazev )
  {
    Nazev = nazev;
  }
  
  virtual public string VratTyp()
  {
    return "Produkt";
  }
}

class Monitor : Produkt
{
  public double Uhlopricka { get; set; }
  public Monitor( string nazev, double uhlopricka ) : base ( nazev )
  {
    Uhlopricka = uhlopricka;
  }
  
  override public string VratTyp()
  {
    return "Monitor";
  }
}
```
pokud bychom VratTyp nepřekryli, tak by upcastovaný monitor vracel typ produkt
