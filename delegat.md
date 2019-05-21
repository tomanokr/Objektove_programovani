# Delegát
reference na metody s konkrétním návratovým typem a parametry
```c#
delegate void MujDelegat(int x);
static void VypisA(int x)
{
  Console.WriteLine($"A: {x}")
}
static void VypisB(int x)
{
  Console.WriteLine($"B: {x}")
}

static void Main(string[] args)
{
    MujDelegat d = null;
    d += VypisA;
    d += VypisB;
    
    d.Invoke(3);
    
    d -= VypisA;
    
    d.Invoke(6);
}
```
