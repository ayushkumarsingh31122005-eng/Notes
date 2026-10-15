# Easy level 

## Q1. Create Person with name and age; Student extends Person and adds rollNumbe
 ```
 class Person{
    public String name;
   public  int age; 

  // constructor ...
  public  Person(String name , int age){
    this.name = name ; 
    this.age = age;
    System.out.println("The name is : "+name+"\n age is : "+age);
  }
  // 
}

class Student extends  Person{
  private  String rollNo;

  // constructor ...
  public  Student( String name, int age , String rollNo){
    super(name, age);
    this.rollNo = rollNo; 
    
   System.out.println("\n rollNo : "+rollNo);
  }

}
/**
 * Inheritance
 */
public class Inheritance {

  public  static void main(String args [] ){
    // creating Person object..
    Person p = new Person("Ayush",20);
    Student s = new Student("Prince ", 22, "0133CS241087");
  }
}
 ```
 ## Q2. Create Vehicle, then Car and Bike; demonstrate constructor chaining.

```
class Vehicle {
  public  String companyName , wheelOfVehicle; 

  // constructor..
  public  Vehicle(String companyName , String wheelOfVehicle){
    this.companyName = companyName; 
    this.wheelOfVehicle = wheelOfVehicle; 

    System.out.println("Company Name : "+companyName+"\n No. of wheels in Vehicle : "+wheelOfVehicle);
  }

}

class Car extends Vehicle{
  public  String vehicleName;

  public  Car(String companyName , String wheelOfVehicle ,String vehicleName){
    System.out.println("Child class");
      super(companyName, wheelOfVehicle);
     this.vehicleName = vehicleName;
     System.out.println("Vehihicle Name :"+vehicleName);
  }
}

class Bike extends  Vehicle{
  public  String vehiclNmae; 
  public  Bike(String companyName, String WheelofVehicle, String vehicleNmae){
    System.out.println("Second child class");
    super(companyName, WheelofVehicle);
    this.vehiclNmae = vehicleNmae; 
    System.out.println("Vehihicle Name :"+vehicleNmae);
  }
}

public class Inheritance {

  public static void main(String args [] ){
    Vehicle v = new Vehicle("Suzuki ", "2");
    Car c = new Car("Toyata","4","Fortuner" );
    Bike b = new Bike("Yamha","2","FZ");
  }
}
```
## Q3. Employee with id, name, salary; Manager adds department.
Hint: Keep common state in Employee. Initialize inherited fields through the parent constructor, then initialize department.

```
class Employee{
  String EmpId, name;
  double salary; 
  
// constructor...
public  Employee(String name, String EmpId, double salary){
  this.EmpId = EmpId; 
  this.name = name; 
  this.salary = salary;

  System.out.println("Emp ID : " + EmpId+"\n EMP_Name : "+name+"\n Salary : "+salary);
}

}

class Manager extends  Employee{
  String department; 
  // constructor 
   public  Manager(String name , String EmpId , double salary , String department){
    super(name, EmpId, salary);
    this.department = department;
    System.out.println("Departmet : "+department);
   }
}

/**
 * Inheritance
 */
public class Inheritance {

   public static void main(String args [] ){
    Employee  em = new Employee("Aysuh", "Ayus23423", 528452134);
    System.out.println();
    Manager man = new Manager(em.name,em.EmpId,em.salary,"CSe");
   }
}
```
## Q4.. Shape has describe(); Circle and Rectangle override it.
Hint: Use identical method signatures and @Override. Call through Shape references to see dynamic dispatch.
```
class Shape{
  boolean isRegular , isIrregular; 
  // method 
  public  void describe(){
    System.out.println("the given figure is a shape");
  }
}

class Circle extends  Shape{
  @Override 
  public  void describe(){
    System.out.println("The given Shape is Circle");
  }
}
class Rectangel extends Shape{
  @Override  
  public  void describe(){
    System.out.println("The given fig is Rectangle ...");
  }
}

/**
 * Inheritance
 */
public class Inheritance {

  public  static void main(String args []){
    Shape c1 = new Circle();
    Shape r1 = new Rectangel();
    c1.describe();
    r1.describe();
  }
}
```