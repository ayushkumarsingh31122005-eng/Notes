 ### Calculating area of Triangle  using normal Formula

 ```
 import java.lang.*; // importing java language with all librabries
import java.util.Scanner; // importing Scanner class

public class arithematic {

    static float base,height;
    static   float area;
      public static void main (String [] args){
          Scanner sc = new Scanner(System.in); // introducing Scanner class

          //Taking input Base & Height
          base = sc.nextFloat();
          height =sc.nextFloat() ;
            
          // Calculating Area (area of Triangle = 1/2(base*height))

          area = ((0.5f)*(base*height));
          System.out.println("Area of Trianle is :" +area);
      
      }
}
```
### Caluculating area of Triangle using another Formula..

```
import java.lang.*; // importing java language with all librabries
import java.util.Scanner; // importing Scanner class

public class arithematic {

        static float side1,side2 ,side3;
        static double area;
       
      public static void main (String [] args){
          Scanner sc = new Scanner(System.in); // introducing Scanner class

          //Taking input  sides of Triangle
          System.out.println("Enter 3 sides of a Triangle !");
          side1 = sc.nextFloat();
          side2=sc.nextFloat() ;
          side3=sc.nextFloat() ;
            
          // Calculating Area (area of Triangle = (s*(s-a)*(s-b)*(s-c)){Where S =1/2(a+b+c)})

          // calculating s

          float s = (1f/2f)*(side1+side2+side3);
         area = Math.sqrt(s*(s-side1)*(s-side2)*(s-side3));

          System.out.println("Area of the Triangle :" + area);
      
      }
}
```
# Finding Roots of Quadratic Equation 
```
import java.lang.*;
import java.util.Scanner;

/**
 * operattor
 */

//Finding Roots of Quadratic Equation

public class operator {

                static int a,b, c;
                static double r1,r2;
      public static void main(String[] args) {
              // The Quadratic Equation (ax^2 + bx +c =0)
              Scanner sc = new Scanner(System.in);  // Calling  Scanner class to get input ..
              // Taking input a,b,c from the user..
              System.out.println("Enter  values of a,b,c");
        
                  a= sc.nextInt();
                  b= sc.nextInt();
                  c= sc.nextInt();

        // calculating Disctiminent..

            double Disctiminent = ((b*b)-(4*a*c));

        
      if(Disctiminent>0){
            // caluculating r1 
            r1 = (-b+Math.sqrt(Disctiminent))*(1f/(2f*a));
            //caluculating r2
            r2 = (-b-Math.sqrt(Disctiminent))*(1f/(2f*a));
                System.out.println("Roots of the Quadratic Equation is :" + "Root1 is "+ r1 );
                System.out.println();
                System.out.println( "Root2 is "+ r2 );
      }else if(Disctiminent==0){
              
            r1 = (-b+Math.sqrt(Disctiminent))*(1f/(2f*a));
            //caluculating r2
            r2 = (-b-Math.sqrt(Disctiminent))*(1f/(2f*a));
                System.out.println("Discriment is 0 so the both roots are equal");
                System.out.println("Root1 is :"+r1);
                System.out.println("Root2 is :"+r2);
        }
      else {
                System.out.print("Your Discriment is Negative :" +"Root is Nan"  );
                
              }

    }
}
     
```
# Calculating  totalArea and Volume of Cuboid
```
import java.lang.*;
import java.util.*;

/**
 * operator
 */
public class operator {

  public static void main(String[] args) {
    int l, b, h;
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter Length , breadth and height of the Cuboid ");
    l= sc.nextInt();
    b= sc.nextInt();
    h= sc.nextInt();
    // Caluculating Volume of the Cuboid 
    int Volume = l*b*h;
    // Calculating total area of triangle..
    int totlalArea = 2*(l*b+l*h+b*h);

    System.out.println(("total Area of cuboid is :" + totlalArea +" "+ "Volume  is : "+ Volume));

  }
}
```