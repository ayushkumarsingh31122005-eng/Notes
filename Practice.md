# Tutorial Pracitce 
 
 #### Calculating area of Triangle 

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