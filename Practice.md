# Tutorial Pracitce 
 
 #### Calculating area of Triangle  using normal Formula

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