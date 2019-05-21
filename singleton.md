# Singleton
pro vytvoření pouze jednoho objektu
```c#
class Logger
{
  private static Logger logger = null;
  public static Logger Instance
  {
      get
      {
        if ( logger == null )
        {
          logger = new Logger();
        }
        return logger;
      }
  }
  public void Log( string text )
  {
    Console.WriteLine($"{DateTime.Now}: {text}");
  }
}
```
