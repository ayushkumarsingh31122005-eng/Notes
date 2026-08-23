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
# Bitwise Operations 

```
import java.lang.*;

/**
 * operator
 */
public class operator {

    public static void main(String[] args) {
        int x=0b1010,y=0b0110,z;
        z=x&y; // (AND operator)
        System.out.println("z is :" + z);// oputput is 2;
        z= x|y;//(OR operator)
        System.out.println("z is :" + z);// oputput is 14;
        z = x^y; //(XOR operator);
        System.out.println("z is :" + z);// oputput is 12;
        z = ~x; //( NOT operator)
        System.out.println("z is :" + z);// oputput is 2;
        z = ~y;// (NOT of y)

        System.out.println("z is :" + z);// oputput is 2;

    }
}
```
# Swapping Two Numbers using Bitwise operations 
```
// Program to Swapping numbers
public class operator {
    public static void main (String [] args){
        int a=10,b=15;
        System.out.println("Before swapped " + "a = "+a +"  b= "+b);
        a=a^b;
         b = a^b;
         a=a^b;
         System.out.println("After swapped " + "a = "+a +"  b= "+b);
    }
    
}
```

# Merging and Masking  program  using Bitwise operators 
### Merging = combining two separate pieces of binary data into one value.
### Masking = using AND (&) with a bit pattern to select/extract specific bits.

```
public class operator {
    public static void main (String [] args){
        byte a=9,b=12;
        byte c;
        c =(byte)(a<<4);
        c =(byte)(c|b); // merging both a & b in c
       System.out.println((c&0b11110000)>>4); // reading first 4bits of c weather it is equal to 9 or not! That is  extracting 9
       System.out.println((c&0b00001111)); // reading last 4bits of c weather it is equal to 12 or not! Extracting 12
    }
    
}
```

### Playing with * System.out.printf() * method

#### using format specifiers 
```
public class operator {

    public static void main(String[] args){
      String name = "Spongebob";
      char firstLetter = 'S';
      int age = 30;
      double height =60.5;
      boolean isEmployed = true;

        System.out.printf("Hello %s\n",name);
        System.out.printf("Your name starts with %c\n",firstLetter);
        System.out.printf("Your name age is   %d\n",age);
        System.out.printf("Your height is  %f inches tall\n", height);
        System.out.printf("You are Employed:  %b\n",isEmployed);

        // adding multiple variable in a single line..
        System.out.printf("%s your name start with %c , you are %d years old , your heigh is %f and your Employed : %b",name,firstLetter,age,height,isEmployed);
    }
}
```
### Various Way to create Strings
```
public class operator {

    public static void main(String[] args){
        String name = "Ayush";
        String name2 = new String("Prince");
        char c[]={'H','e','l','l','o'};
        byte string1[] ={70,71,72,73,75};

        String greet = new String(c); // str creating using char
        String BytStr = new String(string1); // str creating using byte
        System.out.println(name);
        System.out.println(name2);
        System.out.println(greet);
        System.out.println(BytStr);
    }
}
```
### Applying some methods of string 
```
public class operator {

    public static void main(String[] args){
     String str = new String("NOTEBEANS");
      int len= str.length();
      String lowerercase = str.toLowerCase();
            System.out.println(len);
            System.out.println(lowerercase);
        String str2 = str.substring(1, 4);
            System.out.println(str2);
        String  str3 = str.replace('E', 'M');
            System.out.println(str3);
    }
}
```
* Q. given  a string = "programmer@gmail.com" ; Now check out the domain name (or does it conain 'gmail'), and extract domain name and then holder name 
```

public class operator {

    public static void main(String[] args){
       String str = "programmer@gmail.com";
    //    System.out.println(str.contains("gmail"));
       int indexOf =str.indexOf("@"); 
       String UserName = str.substring(0,indexOf);
       System.out.printf("The useName  is : %s \n" , UserName);
       String holderName = str.substring(indexOf+1);
       System.out.printf("The holderName is : %s \n", holderName);
       int indexOf2 =  holderName.indexOf(("."));
       System.out.println("Domain name is  : "+ holderName.substring(0, indexOf2));
    }
    
}
```
### Q. Find  if a Number is Binary or not ?

```
import java.lang.*;
import java.util.*;
public class operator {

   static String str ;
        public static void main (String [] args){

             Scanner sc = new Scanner(System.in);
             System.out.println("Enter your Number");
             str = sc.next();
             System.out.println("The given number is binary  : " + str.matches("[01]+"));
             
        }
}
```

####  Q. Find the number is Hexa-Decimal or not?

```

import java.lang.*;
import java.util.*;

/**
 * operator
 */
public class operator {

        public static void main(String[] args){
            long hexaNumber = 0x34235ABC;
            

            String str ="0x" + Long.toHexString(hexaNumber); // way to convert hexa-decimal into string and keeping "0x" as a constant.
            System.out.println("the given number is HexaDecimal  :" + str.matches("0[xX][0-9A-Fa-f]+"));
              | |     |
              | |     |
              | |     |
              | |     |
              | |     |
              | |     |_______ one or more hexadecimal digits.
              | |     
              | |_____// x  or x
              |________ // literal 0
        }
}

```