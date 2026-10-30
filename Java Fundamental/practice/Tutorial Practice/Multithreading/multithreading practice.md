# Q1.  [Beginner] Create a class that extends Thread. Override run() to print your name 5 times. Create and start
one object.
```

package DSA.dsa;
 


class thread extends  Thread{
  @Override 
  public  void run(){
    for(int i = 0; i<5; i++){
      System.out.println("Ayush");
    }
  }
}

class Basics {

  public static void main(String[] args) {
    thread t = new thread();
    t.start();

  }
}
```
# Q2. . [Beginner] Create two threads: one prints numbers 1–10 and the other prints letters A–J. Start both and
observe how their outputs interleave. Explain why the order can change between runs.
```

package DSA.dsa;
 


class IntergerPrintThread extends  Thread{
  @Override 
  public  void run(){
    for(int i = 1; i<=10; i++){
      System.out.print(i+" ");
    }
  }
}

class LetterPrintThread extends  Thread{
   int n = 65; 
   public  void run(){
    for(int i = n ; i<=74; i++){
      System.out.print((char)i +" ");
    } 
   }
}
class Basics {

  public static void main(String[] args) {
    IntergerPrintThread it = new IntergerPrintThread(); 
    LetterPrintThread lt = new LetterPrintThread();
    it.start();
    lt.start();

  }
}
```
# Q3.  [Beginner] Rewrite the previous task by implementing Runnable instead of extending Thread. Compare the
two approaches in a short comment.
```

package DSA.dsa;
 


class IntergerPrintThread implements  Runnable{
  @Override 
  public  void run(){
    for(int i = 1; i<=10; i++){
      System.out.print(i+" ");
    }
  }
}

class LetterPrintThread implements  Runnable{
   int n = 65; 
   public  void run(){
    for(int i = n ; i<=74; i++){
      System.out.print((char)i +" ");
    } 
   }
}
class Basics {

  public static void main(String[] args) {
    IntergerPrintThread it = new IntergerPrintThread(); 
    LetterPrintThread lt = new LetterPrintThread();
   
    Thread t1 = new Thread(it);
    Thread t2 = new Thread(lt);
    t1.start();
    t2.start();

  }
}
```
# Q4. 5. [Beginner] Create a thread named Download-Worker. Print its name from inside run(), then change its
name and print it again.
```
package DSA.dsa; 

class Wroker implements  Runnable{
  @Override  
  public  void run(){
    System.out.println(Thread.currentThread().getName());
    Thread.currentThread().setName("Download-Manager");
    System.out.println(Thread.currentThread().getName());
  }
}
/**
 * Basics
 */
public class Basics {

  public  static void main(String args []){
    Wroker w = new Wroker();
    Thread t = new Thread(w,"Download-Worker"); 
    t.start();
  }
}
```
# Write one program that calls run() directly and another that calls start(). Print the current
thread's name in each case and explain the difference.

```
package DSA.dsa; 

class thread  implements  Runnable{
  @Override  
  public  void run(){
    System.out.println(Thread.currentThread().getName());

     Thread.currentThread().setName("Pinky");
     System.out.println(Thread.currentThread().getName());
  }
}

/**
 * Basics
 */
public class Basics {

  public  static  void main(String args []){
    thread t  = new thread();
    Thread T = new Thread(t, "yello");
    t.run();
    T.start();
  }
}
```
# [Beginner] Print “Start”, pause the current thread for 2 seconds using Thread.sleep(), then print “End”.
Handle InterruptedException correctly.
```
package DSA.dsa;

class PrintStar implements  Runnable {
  @Override  
  public  void run(){
    System.out.print("Start");
    try{
      Thread.currentThread().sleep(2000);
    }catch(InterruptedException e){
       Thread.currentThread().interrupt();
       return ;
    }
    System.out.println(" End");
  }
}

/**
 * Basics
 */
public class Basics {

  public  static  void main(String args []){
    PrintStar p = new PrintStar();
    Thread t = new Thread(p);
    t.start();
  }
}
```
