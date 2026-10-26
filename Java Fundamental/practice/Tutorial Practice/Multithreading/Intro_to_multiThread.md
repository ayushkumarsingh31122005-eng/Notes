#  Making Two Control-flow
* to achive "multithreading" first we must entends Thread class and the override run method and write everything in this method only... 
* and to call the method we must create object of the class and then invoke start method.

ex..
```
class MyThreads extends Thread{
  public void run()
  {
    int i = 1; 
    while (true) {
      System.out.println(i+" Hello");
      i++;
    }
  }
}

public class Test {
  public static void main(String args []){
    MyThreads t = new MyThreads();
    t.start();

    int i =  1; 
    while(true){
      System.out.println(i+"World");
      i++;
    }
  }
}
```
## Another way to achive (writing in same class)

```
public  class Test extends  Thread{
  public  void run(){
    int i = 1;
    while (true) {
      System.out.println(i+"Hello");
      i++;
    }
  }

  public static void main(String args []){
    Test t =  new Test();
    t.start();
    int i = 1; 
    while(true){
      System.out.println(i+"World");
      i++;
    }
  }
}
```

## Achiving  Multing Threading via Implementing Runable interface 

```
 class My implements Runnable{

  public void run(){
    int i = 1; 
    while(true){
      System.out.println(i+" Hello");
      i++;
    }
  }
}

public class Test {
public static void main(String args []){
  My m = new My();
  Thread t = new Thread(m); // creating an object of thread and passing objet of the calss My;
  t.start();

  int i = 1;
  while(true){
    System.out.println(i+"World");
    i++;
  }
}
  
}
```
### Achiving multiTreading via same class
```
public  class Test implements Runnable {

  public  void run(){
    int i = 1; 
    while(true){
      System.out.println(i+"Hello");
      i++;
    }
  }

  public static void main(String args []){

    Test m = new Test();
    Thread t = new Thread(m);
    t.start();
    
    int i = 1; 
    while(true){
      System.out.println(i+"World");
      i++;
    }
  }
}
```