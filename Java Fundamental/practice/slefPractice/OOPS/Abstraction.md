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