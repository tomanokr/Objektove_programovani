# Abstraktní metody a třídy
používáme tehdy, je-li metoda bez specifikace potomka neznámá, ale každý potomek ji využívá
```c#
abstract class Zviratko
{
  public string Jmeno{ get; set; } 
  
  abstract public string VratZvuk();
}

class Pes : Zviratko
{
  override public string VratZvuk()
  {
    return "haf haf";
  }
}
```
