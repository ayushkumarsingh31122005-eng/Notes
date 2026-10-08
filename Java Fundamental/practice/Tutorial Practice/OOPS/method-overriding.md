# Method overriding..
--
### 1.
```
class Super{
public void display(){
  System.out.println("Super class display..");
}
}

class child extends Super{
  @Override 
  public  void display(){
    System.out.println("child class display");
  }
}

/**
 * example2
 */
public class example2 {

  public static void main(String args[]){
    Super sup= new Super();
    sup.display();
    child ch = new child();
   ch.display();

  // Dynamic method in java : where reference of super class is used and object of the sub class is used...
    Super sup2 = new child();
    sup2.display();
}

}
```

### 2.
```
class TV{
  public void switchON(){
    System.out.println("TV is switched on");
  }

  public void changeChannel(){
    System.out.println("TV channel is changed..");
  }
}

class smartTv extends  TV{
    @Override 
    public void switchON(){
    System.out.println("SmartTV is switched on");
  }
    @Override 
    public void changeChannel(){
    System.out.println("SmartTV channel is changed..");
  }

  public void browse(){System.out.println("Smart tv browsing..");}
}

/**
 * example2
 */
public class example2 {

  public static void main (String args []){
    // super class object
    TV tv= new TV();
    tv.changeChannel();
    // child class object..
    smartTv smTV = new  smartTv();
    smTV.browse();
    // Dynamic dispatched method...
    TV t = new smartTv();
    t.changeChannel();
    // t.browse(); // in dynamic method only super class methodes are allowed ot use not newly defined method inside the child class...
    
  }
}
```
### 3.
```
class car{
  public void start(){System.out.println("car started...");}
  public void accelerated(){System.out.println("car accelerated...");}
  public void gareChange(){System.out.println("car gareChanged...");}
}
class LuxaryCar extends car{
  @Override 
  public  void gareChange(){System.out.println("Automatic Gear..");}
  public  void openRoof(){System.out.println(" Roof opened..");}
}

/**
 * example2
 */
public class example2 {

  public static void main(String args[]){
    car c= new car();
    c.accelerated();

    LuxaryCar lxcar = new LuxaryCar();
    lxcar.gareChange();
  }
}
```

# Dynamic Method Dispatch..
###  1.
```
class Super{
  
  public void  supermethod1(){System.out.println("Super Class Method 1");}
  public void  supermethod2(){System.out.println("Super Class Method 2");}
}

class child extends Super{
  @Override 
  public  void supermethod2(){
    System.out.println("Child class Method 2");
  }
}

/**
 * example2
 */
public class example2 {

  public static void main(String arg[]){

    // Dynamic method dispatch..
    Super sup = new child();
    sup.supermethod2();
  }
}
```
# Run time Polymorphism is achived by method-overloading and method-overriding..

* by Method overloading..
```
class Test{
  public int max(int a, int b){
    return a>b?a:b;
  }
  public int max(int a, int b , int c){
    if(a>b && a>c){
      return a;
    }else if(b>c)return b;
    return c;
  }
}
/**
 * example2
 */
public class example2 {

  public static void main(String arg[]){
    Test t = new Test();
    
   System.out.println( t.max(12,34));
   System.out.println( t.max(12,21,32));
  }
}
```
* Here the compiler will decide which method will called based on how many arguments passed while invoking it..

### Here Run-Time polymorphism is achived by method-overriding...
```
class Super{
  public  void display(){
    System.out.println("Super Display..");
  }
}

class sub extends Super{
  public void display(){
    System.out.println("Sub Display..");
  }
}

/**
 * example2
 */
public class example2 {

  public static void main(String args[]){
    Super s  = new sub();
    s.display();
  }
}
```
* the compliler will decide run time that which method will be called , since here dynamic method dispatch has been used..
