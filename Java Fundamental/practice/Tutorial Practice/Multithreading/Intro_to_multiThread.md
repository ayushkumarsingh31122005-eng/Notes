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

## Thread class and their various Methods 
```
import java.util.*;
import java.lang.Thread.*;


class MyThread extends  Thread {
  public MyThread (String name){
    super(name);
    setPriority(Thread.MIN_PRIORITY+2);
  }
}

public class Test {
  public static  void main(String args [])throws Exception{
    MyThread t = new MyThread("My Thread 1");

    System.out.println("ID " +t.getId() );
    System.out.println("Name "+t.getName());
    System.out.println("Priority : "+t.getPriority());
    t.start();
    System.out.println("State "+t.getState());
    System.out.println("Alive "+t.isAlive());
  }
}

```
## Demo over sleep Method 
```
import java.util.*;
import java.lang.Thread.*;


class MyThread extends  Thread {
  public MyThread (String name){
    super(name);
    
  }

  public void run(){
    int count = 1;
     while(true){
      System.out.println(count++);
      try{

        Thread.sleep(10);
      }
      catch (InterruptedException e){
        System.out.println(e);
      }
     }
  }
}

public class Test {
  public static  void main(String args [])throws Exception{
    MyThread t = new MyThread("My Thread 1");

    t.start();
    t.interrupt();
  }
}

```
## demo over "Demon" and "join" methods
```
class MyThread extends  Thread{
  public void run(){
    int count = 1; 
    while(true){
      System.out.println(count++);

    }
  }
}

public class Test {

  public static void main(String args []) throws Exception{
    MyThread t = new MyThread();
    t.setDaemon(true); // it make the thread  end when the method ends 
      t.start();
      try{
        Thread.sleep(100);
      }
      catch(Exception e){};
      // After applying Try and cathc block  manin method will wait for 100 millis then "Demon" method won't be  endup the thread until and unless the method ends

      Thread mainThread = Thread.currentThread();
      mainThread.join(); // This method autometiacally join the running thread 
      
  }

}
```
# Demo over "yield" method
```
class MyThread extends  Thread{
  public void run(){
    int count = 1; 
    while(true){
      System.out.println(count++  +" My Thread ");

    }
  }
}

public class Test {

  public static void main(String args []) throws Exception{
    MyThread t = new MyThread();
    t.setDaemon(true); // it make the thread  end when the method ends 
      t.start();
      int  count = 1; 
       while (true) {
        System.out.println(count++ +" Main");
        Thread.yield();
       }

  }

}
```
# Synchronization
  #### without using synchronization
  ```
   class MyData{
  void display(String str){
    for(int i=0; i<str.length();i++){
      System.out.print(str.charAt(i)+" ");
    }
  }
 }
 class Mythread1 extends  Thread{
  MyData d; 
  Mythread1(MyData data){
     d = data;
  }
  public  void run(){
    d.display("Hello world");
  }
 }

 class Mythread2 extends  Thread {
  MyData data; 
  Mythread2(MyData dat){
     data  = dat;
  }
  public void run(){
    data.display("Welcome");
  }
 }
 public class Test {
 
  public static  void main(String args []){
    MyData d = new MyData();
    Mythread1 t1 = new Mythread1(d);
    Mythread2  t2 = new Mythread2(d);
    t1.start();
    t2.start();
  }
 }
  ```

  ### using synchronization
  ```
  
  class MyData{
 synchronized void display(String str){ // just adding synchronized key word

    for(int i=0; i<str.length();i++){
      System.out.print(str.charAt(i)+" ");
    }
  }
 }
 class Mythread1 extends  Thread{
  MyData d; 
  Mythread1(MyData data){
     d = data;
  }
  public  void run(){
    d.display("Helloworld");
  }
 }

 class Mythread2 extends  Thread {
  MyData data; 
  Mythread2(MyData dat){
     data  = dat;
  }
  public void run(){
    data.display("Welcome");
  }
 }
 public class Test {
 
  public static  void main(String args []){
    MyData d = new MyData();
    Mythread1 t1 = new Mythread1(d);
    Mythread2  t2 = new Mythread2(d);
    t1.start();
    t2.start();
  }
 }

  ```
  ## ATM demonstration 
  ```
  
package DSA.dsa;
 import java.util.*;

// ATM class...
 class ATM{
  public synchronized void checkBalance(String name){
    System.out.println(name+" Checking ");
    try{
      Thread.sleep(1000);
    }catch(Exception e){
      
    }
    System.out.println("Balance");
  }

  public synchronized  void withdrawBalance(String name , int amount){
    System.out.println(name+"    Withdrawing ");
    try{
      Thread.sleep(1000);
    }catch(Exception e){

    }
    System.out.println(amount);
  }
 }

// Customer class
 class Customer{
  ATM atm; 
  String  name; 
  int amount; 

  Customer(String n , ATM a, int am){
    name = n; 
     atm = a; 
     amount = am;
  }

  void useATM(){
    atm.checkBalance(name);
    atm.withdrawBalance(name, amount);
  }
  public  void run(){
    useATM();
  }
 }


class Basics {

  public static void main(String[] args) {
    ATM atm = new ATM();
    Customer c1 = new Customer("Smith", atm, 100);
    Customer c2 = new Customer("prince", atm, 500);

    c1.run();
    c2.run();

  }
}

  ```
  