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
