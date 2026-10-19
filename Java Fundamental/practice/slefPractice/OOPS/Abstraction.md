# Easy level ...

## Q1. Abstract Shape with area(); Circle and Rectangle.
Hint: Declare abstract double area(); concrete subclasses must implement it.
```
// Declaring Abstract class

  abstract class Shape {

  // Declaring abstract method...
 public  abstract double area();

} 

class Circle extends Shape{
  float radius;
  public  Circle(float r){
    this.radius = r;
  }
  @Override 
  public double area(){
    return Math.PI*radius*radius;
  }
}


class Rectangle extends  Shape{
  int l ,b; 
  public  Rectangle(int l ,int b ){
    this.l = l ; 
    this.b = b;
  }
  @Override 
  public  double area(){
    return  l*b; 
  }
}

/**
 * InnerShape
*/
public class Abstraction {
  
  public static  void  main(String args []){
    Shape c = new Circle(5.2f);
    Shape r = new Rectangle(5, 8);
    System.out.println("the area of the Rectangle is : "+r.area());
    System.out.println("Maht.PI*radius*radius : "+c.area());
    
  }
}
```
## Q2. Abstract Animal with sound() and sleep().
Hint: Make sound abstract and sleep concrete; subclasses implement sound while inheriting sleep.
```
abstract class Animal{
// Declaring concrete method...
public  void sleep(){
  System.out.println("Animal is sounding...");
}
  // Declaring abstract method...
   public  abstract void sound();
}
// Another Class that implements the abstract class...

class Goat extends  Animal{
  @Override 
  public  void sound(){
    System.out.println("Mee..Mee");
  }
}

public class StudentChallenge {

  public  static void main(String args []){
    Goat g = new Goat();
    g.sound();
  }
}
```
# Q3. Abstract Employee with calculateSalary().
Hint: Put common fields and validation in the base class; each concrete employee computes salary differently
```
abstract class Employee{
  String empId; 
  String empName;
 

  // constructor...
  Employee(String empId, String empName){
    this.empId = empId;
    this.empName = empName;
    
  // Method for Calculating Salary...
}
public  abstract double  calculateSalary();
}
class PartTimeEmployee extends  Employee{
    public  int hrs;
   // calling super class constructor...
   public  PartTimeEmployee(String empId, String empName, int hrs){
       super(empId, empName);
         this.hrs = hrs;
    }
  @Override 
  public  double calculateSalary(){
    return  hrs*400;
  }

}

class FullTimeEmployee extends  Employee{
     
    boolean isFUllTime ; 
    // constructor...
    public FullTimeEmployee(String empId,String empName, boolean isFUllTime){
      super(empId, empName);
      this.isFUllTime= isFUllTime;
    }
  
  @Override  
  public  double calculateSalary(){
    return 400000000;
  }
    
}

/**
 * StudentChallenge
 */
public class StudentChallenge {

  public  static void main(String args []){
    FullTimeEmployee f = new FullTimeEmployee("Ayush1232", "Ayush", true);
    System.out.println(f.calculateSalary());
  }
}
```
# Q.4
```
abstract class parent {
  int e,y; 
  public  parent(){
    System.out.println("Parent constructor..");
  }
}

class child extends parent{
  public child(){
    System.out.println("Child constructor");
  }
}

public class StudentChallenge{
  public  static  void main(String args []){
    child c = new child();
  }
}
```