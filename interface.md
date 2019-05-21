# Interface (rozhraní)
Funguje jako abstraktní třída.

Třída může implementovat libovolný počet rozhraní.

```c#
interface IZvuk
{
  string VratZvuk();
}

class Pes : IZvuk
{
  public string VratZvuk()
  {
    return "haf haf";
  }
}

class Auto : IZvuk
{
  public string VratZvuk()
  {
    return "brm brm";
  }
}
```
