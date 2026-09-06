# 1. Core Syntax, Input, Data Types & Operators


### 2. [Recall] Read the radius of a circle as float and print its area and circumference. Use an appropriate numeric type
for the result
remainder. Explain what happens when integer division is used.
```
import java.util.*;

// circle class..
class circle{
   float radius;

  // constructor for the property radius..
  public circle(float r){
    this.radius= r;
  }
  // get  method ..
  public float getRadius(){
    return  radius ;
  }
  // set Method 
  public void setRadius(float r){
    if(r>0)
    radius = r;
   else 
     radius = 0;
  }
  // method to calculate circumerence ..
   public    float circumerence(){
     return  (float)(2*Math.PI*radius);
       
  }
  // method for area ...
  public float area(){
    return (float)(Math.PI*radius*radius);
  }
}

/**
 * revisionOne
 */
public class revisionOne {

    public static void main(String args[]){

      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the radius !");
      float r = sc.nextFloat();
      circle c = new circle(r);
      System.out.println("The radius of the circle : "+ c.radius+"\n The circumference of the circle is : "+c.circumerence()+ "\n and the area is : "+ c.area());
    }
}
```
### 3. [Apply] Given three sides of a triangle, calculate its area using Heron's formula. Reject the input if the three sides
cannot form a valid triangle

#### adding concept of data hiding..

```
import java.util.*;

class triangle{
  private int s1, s2,s3; 

  // constructor 
  public  triangle (int side1,int side2,int side3){
    s1 = side1;
    s2 = side2;
    s3 = side3;
  }

  // Getter methods for getting all sides
  public int getSideOne(){
    return s1;
  }
  public int getSideTwo(){
    return s2; 
  }
  public  int getSideThree(){
    return  s3;
  }
  // setter Method for setting all sides .
  public  void setSideOne(int s){
    if(s>0) s1 =s;
    else s1 =0;
  } 
  public  void setSideTwo(int s){
    if(s>0) s2 =s;
    else s2 =0;
  } 
  public  void setSideThree(int s){
    if(s>0) s3 =s;
    else s3 =0;
  } 
  // Methdo for checking weather the side make tirangle.
  public  boolean isValidSides(){
    boolean isValid = false ;
    if(s1+s2 > s3 && s2+s3 >s1 && s1+s3 > s2  ){
      isValid = true;
    }else{
      isValid = false;
    }
    return isValid;
  }

  // Method for finding area ..
  public  double areaOfTriangle(){
    double  area = 0;
    if(isValidSides()== true){
      double s = (s1+s2+s3)/2.0;
      area = Math.sqrt(s*(s-s1)*(s-s2)*(s-s3));
    }
    return area;
  }

}

/**
 * revisionOne
 */
public class revisionOne {

   public static void main(String args []){
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter the side of the trangel !");
    int sideOne = sc.nextInt();
    int sideTwo = sc.nextInt();
    int sideThree = sc.nextInt();
    triangle t = new triangle(sideOne, sideTwo, sideThree);
    System.out.println("The sides of the triangle is ---> \n side one :"+ t.getSideOne()+"\n sideTwo is : "+t.getSideTwo()+" \n sideThree is : "+ t.getSideThree() + "\n is the sides are valid  for triangle is :"+ t.isValidSides()+"\n  the area of the Triangle is :  "+t.areaOfTriangle());
     
   }
}
```
### 4. [Apply] Write a program to calculate the total surface area and volume of a cuboid. Make the program work
correctly for decimal dimensions 
```
import java.util.*;

class cuboid{
  // properties of the class.
  private float length , breadth, height;

  // constructor for prop..
  public cuboid(float l , float b , float h){
    length = l; 
    breadth =b; 
    height = h;
  }
  // getter method for prop..
  public float getLength(){
    return  length;
  }
  public  float getBreadth(){
    return breadth;
  }
  public float getHeight(){
    return height;
  }
  // setter Method for prop ..
  public void setLength(float l){
    if(l>0){
      length = l ; 
    }else{
      length = 0; 
    }
  }
  public void getBreadth(float b){
    if(b>0){
      breadth = b ; 
    }else{
      breadth = 0; 
    }
  }
  public void setHeight(float h){
    if(h>0){
      height = h ; 
    }else{
      height = 0; 
    }
  }
  // method for calculating surface area ...
  public double  surfaceAre(){
    return  2*((length*breadth)+(length*height)+(breadth*height));
  }
  // method for calculating volume 
  public double volume(){
    return length*breadth*height;
  }
}
/**
 * revisionOne
 */
public class revisionOne {

  public static void main(String args [] ){
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter the all dimensions of the cuboid !");
    float l = sc.nextFloat();
    float b = sc.nextFloat();
    float h = sc.nextFloat();

    // making object from cuboid class
    cuboid c = new cuboid(l, b, h);
    System.out.println("Sides of the cuboid is \n  Length is : " +c.getLength()+"\n Breadth is : "+c.getBreadth()+ "\n Height is : "+c.getHeight()+"\n the area is : "+ c.surfaceAre()+"\n volume is : "+c.volume());


  }
}
```
### 5. [Trace] Predict the output and explain the type conversion involved:
int x = 5; double y = 2; System.out.println(x / y); System.out.println(x / 2);

```
import java.util.*;
import java.math.BigDecimal;

class predict{
  private int x;
  private   double y;

  // constructor
  public predict (int a, double b){
    x = a; 
    y = b; 
  }
  // getter Method 
  public int getFirsNum(){
    return  x; 
  }
  public  double getSecondNum(){
    return y;
  }
  // setter Method 
  public void setFirstNum(int p){
    if(p != 0){
      x = p ;
    }else{
      System.out.println("YOu are entering wrong data !");
    }
  }
  public void setSecondNum(double q){
    if(q != 0){
      y = q;
    }else{
      System.out.println("YOu are entering wrong data !");

    }
  }
  //Method for calculation 
  public double calculation(){
    return (x/y);
  }
}
/**
 * revisionOne
 */
public class revisionOne {

  public static void main(String args[]){
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter the First and Second Num !");
    int x = sc.nextInt();
    int y = sc.nextInt();
    predict p = new predict(x, y);

    System.out.println("first  Num is : "+ p.getFirsNum()+"\n second Num is : "+p.getSecondNum() +"\n the final result is : "+ p.calculation());

  }
}
```
### 6. [Apply] For a quadratic equation ax² + bx + c = 0, calculate the discriminant and handle all three cases: two real
roots, one repeated real root, and no real roots.

```
import java.util.*;

class Quadratic{
  private int a, b, c;
  // Constructor 
  public  Quadratic(int x ,int y , int z){
    a = x ; 
    b = y; 
    c = z; 

  }
  // getter method 
  public int geta(){
    return a; 
  }
  public int getb(){
    return b; 
  }
  public int getc(){
    return c; 
  }
  // setter Method 
  public void seta(int x){
    a = x;
  }
  public void setb(int y){
    b = y;
  }
  public void setc(int z){
    c = z;
  }
  // method for calculating "Discriment"
  public double discriment(){
    return  b*b - 4*a*c;
  }
  //Method for the solution..
  public double[] sol(){
    
    if(discriment()>0){
      double sol1 = (-b + Math.sqrt(discriment()))/(2.0*a);
      double sol2 = (-b - Math.sqrt(discriment()))/(2.0*a);
      return new double[]{sol1,sol2};

    
     } else if(discriment() == 0){
      double sol3 =  -b/2*a;
      return new double[]{sol3};
    }else{
      System.out.println("Imaginary solutions !");
      return new double[]{};
    }
     
  }
}
/**
 * revisionOne
 */
public class revisionOne {

  public static void main (String args[]){
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter the  a, b, c for the caclculation of Quadratic Equation !");
    int a = sc.nextInt();
    int b = sc.nextInt();
    int c = sc.nextInt();
    Quadratic  q = new Quadratic(a, b, c);
    // double [] solutions = q.sol();

    System.out.println("Distrciment is "+ q.discriment()+" \n solution is :"+Arrays.toString(q.sol()));


  }
}
```
