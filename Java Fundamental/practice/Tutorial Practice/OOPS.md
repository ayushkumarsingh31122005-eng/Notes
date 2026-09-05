## How to declare class and how to make object..

```
// Making circle class. 

class circle{
  public double radius;

  public double area(){
    return Math.PI * radius * radius;
  }
  public double perimeter(){
    return Math.PI *2* radius;
  }
  public double circumference(){
    return perimeter();
  }
}

// Main class 

/**
 * one
 */
public class one {

   public static void main(String args[]){
    circle c1 = new circle(); // way to create object of circle class.
    circle c2 = new circle();
    c2.radius = 14;
    c1.radius =  7;
    System.out.println("Area : "+c1.area()); // accessing the method inside the circle class/
    System.out.println("Perimeter : "+c1.perimeter());
    System.out.println("Circumference"+c1.circumference());
   
    System.out.println("Area2: "+c2.area()); // accessing the method inside the circle class/
    System.out.println("Perimete2 : "+c2.perimeter());
    System.out.println("Circumference2 :"+c2.circumference());

   }
}
```
### Rectangle class 
```
import java.util.*;
class rectangle{
  int length ; 
  int breadth; 

  // Method for finding Rectangle..
  public int area(){
    return length*breadth;
  }
  public int perimeter(){
    return 2*(length+breadth);
  }
  // Method for finding is it Square..
  public boolean isSquare(){
    boolean isSquare = false;
    if(length == breadth){
      isSquare = true;
    }else{
      isSquare = false;
    }
    return isSquare;
  }
}

/**
 * one
 */
public class one {

   public static void main(String args[]){
    Scanner sc = new Scanner(System.in);
    rectangle r1 = new rectangle(); 
    System.out.println("Enter the length and breadth of the Rectangle.!");
    r1.length = sc.nextInt();
    r1.breadth = sc.nextInt();
    System.out.println("THe area of the rectangle is :"+ r1.area());
    System.out.println("THe perimeter of the rectangle is :"+ r1.perimeter());
    System.out.println("Is the given Rectangle is Squara : "+ r1.isSquare());
   }
}
```
### Cylinder class..
* remaining task is to decrease the number of digit after decimal.
```
import java.util.*;

class cylinder{
  float radius;
  int height;

  // Method for lid Area ..
  public double lidArea(){
    return Math.PI*radius*radius;
  }
  //Method for circumference 
  public double circumference(){
    return (2*Math.PI*radius);
  }
  //Method for Total Surface area 
  public double totalSurfaceArea(){
    return (2*Math.PI*radius*radius)+(height)*circumference();
  }
  //Method for volume of cylinder 
  public double volume(){
    return 2*Math.PI*radius*height;
  }
}

/**
 * one
 */
public class one {

  public static void main(String args[]){
    Scanner sc = new Scanner(System.in);
    cylinder c1 = new cylinder();
    System.out.println("Enter the Cylinder and radius and height of  the cylinder !");
    c1.radius = sc.nextFloat();
    c1.height = sc.nextInt();
    System.out.println("The lid area of the given cylinder is :"+c1.lidArea());
    System.out.println("The totalSurfac area of the given cylinder is :"+c1.totalSurfaceArea());
    System.out.println("The lid volume of the given cylinder is :"+c1.volume());
  }
}

```
### Student class
* 
```
import java.util.*;
class student{
  int rollNo;
  String name;
  int noOfCourse;
  
  int m1,m2,m3;

  //Method for finding total Marks
  public int total(){
    return m1+m2+m3;
  }
  // Method  for average ..
  public float avg(){
    return total()/3;
  }
  // Method for givng Grade ..
  public String grade(){
    String grade ;
    if(avg() >= 70 && avg()<100){
      grade = "A";
    }else if(avg()<70 && avg() >= 60){
      grade = "B";
    }else if(avg()<60 && avg()>=50){
      grade = "C";
    }else if(avg()<50 && avg()>=40){
      grade = "D";
    }else{
      grade= "F";
    }
    return grade;
  }
  // Method for details 
  public String details(){
    return "ROLL-NO :"+ rollNo +"\n"+"Name :"+name +"\n" +"Course :"+ noOfCourse+ "\n" ;
  }
}

/**
 * one
 */
public class one {
  public static void main(String [] args){

      Scanner sc = new Scanner(System.in);
      student s = new student();
      System.out.println("Enter the  makrs of student in 3 subjects !");
      s.m1 = sc.nextInt();
      s.m2 = sc.nextInt();
      s.m3 = sc.nextInt();
      
      System.out.println("Entner the studen Name :" );
      s.name = sc.next();
      System.out.println("Entner the studen rollNo.  :" );
      s.rollNo = sc.nextInt();
      System.out.println("Entner the number of course  studen enrolled :" );
      s.noOfCourse = sc.nextInt();
      
       System.out.println("The details of the student is :"+s.details());
      System.out.println("The total marks is : "+s.total());
      System.out.println("The average marks is : "+s.avg());
      System.out.println("The grade of  student  is : "+s.grade());
    }

  }

```
### Data Hiding ..
```
// Practicing "Data Hiding !"

class Rectangle{
  private  double length ;
  private  double breadth ;
  // getter method for getting length ..
  public  double getLength (){
    return  length;
  }
  // Method for getting breadth ...
  public double getbreadth(){
    return  breadth;
  }
  // Setter methods for setting breadth ..
  public void setBreadth(double b){
    if(b >0 ){

      breadth = b;
    }else{
      breadth = 0 ; 
    }
  }
// setter methods for setting length ..
 public void setLength(double l){
    if(l>0)
       length = l;
      else{
        length = 0 ;
      }
 }

 // Method for calculating area ..
  public double area(){
    return  getLength()*getbreadth();
  }

   // Method for calculating Perimeter. .
   public double Perimeter(){
    return  2*(length+breadth);
   }
   public  boolean isSquare(){
    if(length == breadth){
      return  true;
    }else{
      return  false;
    }
   }
}

/**
 * one
 */
public class one {

   public  static void main (String args[]){
    Rectangle r = new Rectangle();
     r.setBreadth(-1.0);
     r.setLength(1.5);
     System.out.println("is Square : " + r.isSquare());
     System.out.println("Length is : " + r.getLength());
     System.out.println("breadth  is : " + r.getbreadth());
     System.out.println("Perimeter is : " + r.Perimeter());
     System.out.println("area is : " + r.area());
   }
}
```
### Types of Properties..
```
// class shows read and write property ..

class rectangle{
  private double lenght ; 
  private double bredth ; 

  public double getLength(){
    return lenght;
  }

  public  void  setLength(double l){
    lenght  =  l ;
  }
}

// classes shows read only property ..

class student{
  private  int roll;
  
  public int getRoll(){
    return  roll;
  }
}

// class shows only set property ..

class acount{
  private   int accountBalance ;
  public  void setaccNo(int acc){
    accountBalance = acc;
  }
}
```
### Constructors..
```
class rectangle{
  private  double length;
  private  double breadth;
  
  //Non paraMetrized constructor
  public rectangle(){
    length = 1 ;
    breadth = 1;
  }
  //PeraMetrized constructor..
  public  rectangle(double l , double b){
    length = l;
    breadth = b;
  }
  // Single paraMetrized constructor..
  public rectangle(double s){
    length = breadth = s;
  }

  // getter method ..
  public double getLength(){
    return length;
  }
  public double getBreadth(){
    return breadth;
  }

  // Setter Method ...
  public void setLenth(double len){
     if(len>0){
       length = len;
     }else{
      length = 0 ; 
     }
  }

  public void setBreadth(double b){
    if(b>0){
      breadth = b; 
    }else{
      breadth = 0;
    }
  }
  // Method for calculating area ..
  public double area(){
    return  getLength()*getBreadth();
  }
  // Method for calculating only perimeter ..
  public  double perimeter(){
    return 2*(length+breadth);
  }
  // Method for checking is Squeare..
  public boolean isSquare(){
    if(length == breadth){
      return true;
    }else{
      return false;
    }
  }
}

/**
 * one
 */
public class one {

  public static void main(String args []){
    rectangle r = new rectangle(5,6);

     System.out.println("is Square : " + r.isSquare());
     System.out.println("Length is : " + r.getLength());
     System.out.println("breadth  is : " + r.getBreadth());
     System.out.println("Perimeter is : " + r.perimeter());
     System.out.println("area is : " + r.area());
  }
}
```

### Cylinder class with constructor , propties and  methods..
```
class Cylinder{
  // Declare properties
  private double radius;
  private double height;

  // Declare constructor of two parametrized for the properties

  public Cylinder (double r, double h){
     radius = r; 
     height = h;
  }

  // getMethod for getting the value of prop..
   public  double getRadius(){
    return  radius ;
   }

   public double getHeight(){
    
    return  height;
   }
   // setMethod for setting value of properties..

   public void setRadius(double r){
    if(r>0)
      radius = r; 
    else 
      radius = 0 ;
   }
   public void setHeight(Double h){
    if (h>0)
    height = h;
   else 
     height = 0 ;
   }

   // Method for calculating lid area...
   public double lidArea(){
    return  2*Math.PI* radius*radius;
   }
   //Method for calculating surface Area ...
   public  double totalSurfaceArea( ){
    return  lidArea()+(height+ (2*Math.PI*radius))*2;
   }
  // Method for calculating Volume ...
  public  double Volume(){
    return  2*Math.PI*radius*height;
  }
}

/**
 * one
 */
public class one {

  public  static void main(String args[]){
    Cylinder c = new Cylinder(2, 3);
    System.out.println("The radius of the cylinder : "+c.getRadius());
    System.out.println("The Height of the cylinder : "+c.getHeight());
    System.out.println("The lid area of the circle : "+ c.lidArea());
    System.out.println("The total Surface area of the circle : "+ c.totalSurfaceArea());
    System.out.println("The Volume of the circle : "+ c.Volume());
  }
}
```
