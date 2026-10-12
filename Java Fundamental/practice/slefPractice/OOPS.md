# Q1.Create a Book class with private attributes for title, author, and price. Implement getters and setters, ensuring that the price cannot be set to a negative value.

```
class Book{
 private String title,author;
  private double price;

  // getter 
  public  String getTitle(){
    return title;
  }
  public  String getAuthor(){
    return author;
  }
  // setter 
  public  void setPrice(double x){
    if(x>0)this.price = x;
    else this.price = 0;
  }
  public  Book(String title,String author,double price){
    this.author = author;
    this.title = title;
    this.price = price;
  }
  public String toString(){
    return  "author is :"+this.author+"\n title is : "+this.title+"\n Price is : "+this.price;
  }
}
/**
 * AbstractExample
 */
public class AbstractExample {

  public  static void main(String args[]){
    Book b = new Book("Hidden ", "vishnu Gupta", 120);
    b.setPrice(-40);
    System.out.println(b);
  }
}
```
# Q2.  Design a Rectangle class with length and width attributes. Include methods to calculate and return the area and perimeter.
```
import  java.lang.*;
import  java.util.*;
class Rectangle {
 private double length, breadth;
 // constructors for the attributes..
 public  Rectangle(){
  this.length = 1; 
  this.breadth = 1; 
 }
 // parametrized constructors 
 public  Rectangle(double l , double b){
  this.length = l;
  this.breadth = b;
 }
 // Getter Method for the attributes...
 public  double getLength(){
  return  this.length;
 }
 public double getBreadth(){
  return  this.breadth;
 }
 //Setter Methods...
 public void setLength(double l){
  if(l>1){
    this.length = l;
  }else{
    this.length = 1;
  }
 }
 public  void setBreadth(double b){
  if(b>1){
    this.breadth = b; 
  }else{
    this.breadth  = 1;
  }
 }
 // Method for calculating area ...
 public  double area(){
  return length*breadth;
 }
 // Method for calculating perimeter ...
 public double perimeter(){
  return 2*(length+breadth);
 }
}

public class AbstractExample {

  public  static void main(String args []){

    Scanner sc = new Scanner(System.in);
    System.out.println("Enter the length and breadth of the Rectangle");
    double length, breadth; 
    length = sc.nextDouble();
    breadth = sc.nextDouble();
    Rectangle r = new Rectangle(length,breadth);
    System.out.println("The area is : "+r.area()+"\n The perimeter is : "+r.perimeter());
  }
}
```
# Q3. Create a BankAccount class with a private balance. Implement safe deposit(double amount) and withdraw(double amount) methods that validate inputs and prevent overdrafts.

```
import java.util.Scanner;

class BankAccount{
  private  double balance ; 
  // constructor for the attributes..
  public  BankAccount(double balance){
    this.balance = balance;
  }
  // getter for attributes...
  public  double getBalance(){
    return  this.balance;
  }
  // setter for the attributes...
  public void setBalance(double balance){
    if(balance>0){
      this.balance = balance;
    }else{
      System.out.println("invalid amount is trying to add..");
    }
  }
  // new balcance after deposite...
  public  double depositeBalance(double amount){
    if(amount <=0){
      System.out.print("Invalid deposite amount");
    }else{
      this.balance += amount;
      System.out.println("Successfully deposited..");
    }
    return  this.balance;
  }
  // withdral..
  public  double withdral(double amount){
    if(amount <=0){
      System.out.print("Invalid withdrawal amount !!");
    }
   else if(amount> this.balance){
      System.out.print("Insufficient Balance..");
    }else{
      this.balance = this.balance-amount;
    }
    return  this.balance;
  }
  // to string method for printing whole object..
  public  String toString(){
    return "The avilable balance is : "+this.balance;
  }
}

/**
 * AbstractExample
 */
public class AbstractExample {

  public  static  void main(String args []){
    Scanner sc = new Scanner(System.in);

    System.out.println("Enter your Balance");
    double balance = sc.nextDouble();
    
    BankAccount  details = new BankAccount(balance);

    System.out.println("Enter the amount YOu want to deposite");
    double deposite = sc.nextDouble();
    details.depositeBalance(deposite);

    System.out.println("Enter the Amount you want to Withdrawl..");
    double withdral = sc.nextDouble();
    details.withdral(withdral);

    System.out.println(details);
  }
}
```
# Q4. Create an Employee class with an id, name, and salary. Add a method raiseSalary(double percentage) that modifies the salary attribute.

```
import  java.util.*;
class Employee {
  private  String id, name ;
  private  double salary;

  // constructor 
  public  Employee(String id, String name , double salary){
    this.id = id;
    this.name = name;
    this.salary = salary; 
  }
  // Getter Method..
  public  String getId(){
    return  this.id;
  }
  public  String getName(){
    return this.name;
  }
  public double getSalary(){
    return  this.salary;
  }
  // Setter Methods...
  public  void setSalary(double salary){
    if(salary <=0){
      System.out.print("Invalid salary trying to set..");
    }else{
      this.salary = salary;
      System.out.println("Salary set successfully..!");
    }
  }
  // method for salary raised by ....
  public  void  raiseSalary (double percentage){
    this.salary =this.salary+ this.salary*(percentage/100);
    System.out.print("Update salary for "+ this.name +": "+ this.salary);
  }
}

public class AbstractExample {

  public  static void main(String args []){
    Scanner sc = new Scanner(System.in);
    Employee emp  = new Employee("1231Ayush", "Aysuh", 12121200);
    emp.raiseSalary(10);
    System.out.println("\n name : "+emp.getName());
    System.out.println("id : "+emp.getId());
    System.out.println("salary : "+emp.getSalary());
  }
}
```
# Q5. Create a Student class containing an array of numerical marks. Implement a method to calculate the average mark and another to return a pass or fail status string.
```
class Student{
    private int marks[] ;
    // constructor...
    public  Student(int marks[]){
        this.marks = marks;
        
    }
    // getAverage Marks...
    public  double getAverage(){
        int total = 0; 
        for(int i = 0 ; i<marks.length;i++){
            total = total+i;
        }
        return (double)total/marks.length;
    }
    // method for giving grade to students...
    public String grade(){
        int avg = (int)getAverage();
        if(avg>40){
            return "Pass";
        }else{
            return "fail";
        }
    }
}

/**
 * EmployeeDemo
 */
public class EmployeeDemo {

    public  static void main(String args[]){
        Student s = new Student(new int[]{56,76,45,90,87});
        System.out.println("Avg" + s.getAverage());
        System.out.println("Status " + s.grade());
    }
}
```
# Q6. Design a Car class with attributes make, model, and currentSpeed. Implement accelerate() and brake() methods that change the speed safely.

```
class car{
    private  String maker, model;
    private  int currentSpeed ; 

    // constrrctor...
    public car(String maker , String model, int currentSpeed){
        this.maker = maker;
        this.model = model;
        this.currentSpeed = currentSpeed; 

    }
    // getter methods for the attributes...
    public  String getMakerName(){
        return  maker;
    }
    public  String getModel(){
        return  model;
    }
    public  int getCurrentSpeed(){
        return currentSpeed;
    }
    public void acclerate(int x){
        currentSpeed += x;
        System.out.println("Speed increased to "+currentSpeed);
    }
    public void Break(int amount){
        if(currentSpeed - amount <0){
            currentSpeed = 0; 
            System.out.println("Speed cannot go below 0. Speed Set to 0");
        }else{
            currentSpeed -= amount; 
            System.out.println("Speed decreased to "+ currentSpeed);
        }
    }
    public  String toString(){
        return "Maker of car"+maker+"\n Model "+model+"\n"+ "\n current speed "+currentSpeed;
    }
}
public class EmployeeDemo {

    public  static void main(String args[]){
        car c = new car("Toyota", "Fortuner", 150);
        System.out.println(c);
        c.acclerate(20);
        c.Break(50);
       
    }
}


```
# Q7.  Create a Product class with productID, name, and quantityInStock. Implement methods to addStock(int quantity) and sellProduct(int quantity) while verifying stock availability.

```
class Inventory{
    private  String productName , productId ;
    private int  quantityInStock;

    // Constructor...
    Inventory(String productName , String productId , int quantityInStock){
        this.productId = productId;
        this.productName = productName;
        this.quantityInStock = quantityInStock;
    }
    // getter Method for all Attributes..
    public  String getProductName(){
        return  productName;

    }
    public String getProdutId(){
        return productId;
    }
    public int getQunatityInStock(){
        return quantityInStock;
    }
    public  void addStock(int quantityInStock){
      int newAddStock = this.quantityInStock+quantityInStock;
      System.out.println("New Stock : "+newAddStock);

    }

    public  void sellProduct(int selledProduct){
        int remainProduct = this.quantityInStock - selledProduct;
        System.out.println("Procduct Remained : "+ remainProduct);
    }

}
/**
 * EmployeeDemo
 */
public class EmployeeDemo {

    public  static void main(String args []){
        Inventory inv = new Inventory("Face_Wash", "facepack12", 105);
        inv.addStock(50);
        inv.sellProduct(100);
    }
}
```
# Q9. : Create a Circle class with a radius attribute. Provide a default constructor that sets radius to 1.0, and a parameterized constructor. Use this.radius to resolve naming conflicts.
```
class Circle{
  private  float radius; 

  // default constructor...
   public  Circle (){
   this.radius = 1; 
   }
   // Parametrized constructor...
   public  Circle(float r){
    this.radius = r; 
   }
   // Getter method 
   public  float getRadius(){
     return  radius;
   }
   // Setter method ...
   public void setRadius(float r){
     this.radius = r; 
   }
   // calculating area 
   public  void area(){
    double area = Math.PI*radius*radius;
    System.out.println("The area of the given circle is : "+area);
   }
}

public class Interface {

   public  static void main(String args[]){
    Circle c = new Circle(5.4f);
     c.area();
   }
}
```