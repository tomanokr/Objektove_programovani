# Dependency injection
```c#
interface IMotor
{
  void Nastartuj();
}
class NaftovyMotor : IMotor
{
  public void Nastartuj()
  {
    Console.WriteLine("Stlacil jsem vzduch");
  }
}
class BenzinovyMotor : IMotor
{
  public void Nastartuj()
  {
    Console.WriteLine("Zapalil jsem svicku")
  }
}
class Automobil
{
  private IMotor motor;
  public Automobil(Imotor motor)
  {
    this.motor = motor;
  }
  public void Jed()
  {
    motor.Nastartuj();
  }
```
