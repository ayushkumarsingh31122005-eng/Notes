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
* ### Q. given  a string = "programmer@gmail.com" ; Now check out the domain name (or does it conain 'gmail'), and extract domain name and then holder name 
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

### Q. Find  is the Data  in Date Format (dd/mm/yyyy);
```

import java.lang.*;

/**
 * operator
 */
public class operator {

        public static void main(String[] args) {
            String data =  "12/3/2024";

            System.out.println("The given data is in the form of Date : "+ 
                data.matches("[0-3][0-9]/[01][0-2]/[0-9]{4}")
            );
        }
}
```

### Q. Remove Special Character from String.
```

import java.lang.*;
import java.util.*;

/**
 * operator
 */
public class operator {
   static String str  ;
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter String ..");
        str = sc.next(); 
            String newStr = str.replaceAll("[^a-zA-Z0-9]","");
            System.out.println(newStr);
    }
}
          

```
### Q Remove extra space from stirng....
```

import java.lang.*;
import java.util.*;

/**
 * operator
 */
public class operator {

    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter String here");
        String str = sc.nextLine();

        String str2 = str.replaceAll("\\s+"," ");
        System.out.printf("Your new String is  :  %s" , str2);


    }
}

```

###  Q. Find out the number of words in the String ....
```

/**
 * operator
 */
public class operator {

    public static void main(String[] args){

        String str = "         Abc            def         gh        ijk";
        str = str.replaceAll("\\s+"," ").trim();
        String wrods[] = str.split("\\s");
        System.out.println("the length of Words in the array is : "+ wrods.length);
    }
}
```
# if else-if else conditionals
### Q. Find a number is odd or even 

```
import java.lang.*;
import java.util.*;

public class relational {
    public static void main (String [] args){
      int num;
      Scanner sc = new Scanner(System.in);
      num =sc.nextInt();
      if(num%2==0){
        System.out.println("Your given Number is Even");
      }else{
        System.out.println("YOur given Number is Odd. !");
      }
    }
  
}
```
### Q. Find Person is Adult or not!

```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

     public static void main(String[] args){
       Scanner  sc = new Scanner(System.in);
       System.out.println("Kindly Enter Your age !");
       int age = sc.nextInt();
       if(age>18){
        System.out.println("You are Adult !");
       }else{
        System.out.println("You are not Adult !");
       }
     }
}
```
### Q Finding the radix of  the given Number .
```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

  
     public static void main(String[] args){
      String num ;
      Scanner sc = new Scanner(System.in);
      num = sc.next();

      if(num.matches("[01]+")){
          System.out.println("You have Entered Binary Number and the Radix is :"+"2");
      }else if(num.matches("[0-7]+")){
        System.out.println("The ENtered Number is Octal and the radix is 8");
      }else if(num.matches("[0-9]+")){
        System.out.println("The Entered Number is  Octal and the radix is : 10");
      }else if(num.matches("[0-9A-Fa-f]+")){
        System.out.println("The given Number is Hexa-Decimal and the radix is : 16");
      }
     }
}
```
### Q. Finding the grade of student 

```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

     public static void main(String[] args){
      int [] m = new int [4];
      Scanner sc = new Scanner(System.in);
      for(int i= 1; i<=3; i++){
        System.out.println("Enter the marks of subject m"+i);
        m[i] = sc.nextInt();
      }
      

      int avg = (m[1]+m[3]+m[3])/3;
      if(avg>=70){
        System.out.println("The grade of the Student is :" + "A and avg marks is :" +avg);
      }else if ( avg>=60 && avg<70){
        System.out.println("The grade is : B and marks is "+avg);
      }else if(avg>= 50 && avg < 60){
        System.out.println("The garde is : C and the marks is "+avg);
      }else if(avg>=40 && avg <40){
        System.out.println("the grade is : D and the marks is "+ avg);
      }else{
        System.out.println("The candidate has Failed !");
      }
     }
}
```

 ### Q. Find that the given yaer is leapyear or not!

 ```

import java.lang.*;
import java.time.Year;
import java.util.*;

/**
 * relational
 */
public class relational {

  public static void main(String[] args){
      long year;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter Year !");
      year = sc.nextLong();

        if(year % 4== 0){
              if (year%100 ==0) {
                if (year%400 ==0) {
                  System.out.print("Leap Year");
                }else{
                  System.out.println("NOt leap Year");
                }
                                  
              }else {
                System.out.println("Leap Year");
              }
        }else {
          System.out.println("Not Leap Year");
        }
       
  }
}
 ```
 ###  Q. Finding Day  based on Number 

 ```
 import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

    public static void main(String[] args) {
      Scanner sc = new Scanner(System.in);
    int []  dayNo = {1,2,3,4,5,6,7};
    String [] days = {
      "Monday",
      "Tuesda",
      "Wednesday",
      "Thursday",
      "Friday",
      "Saurday",
      "Sunday"
    };
    System.out.println("Enter DayNumber !");
    int input = sc.nextInt();
    for(int i = 0; i<dayNo.length; i++){
      if(dayNo[i]==input){
        System.out.println("Day is :" +days[i]);
        break;
      }
    }

    }   
}
 ```

### Q. Finding protocall and type of website..
```
/**
 * relational
 */
public class relational {

  public static void main(String[] args) {
    String web = "https:\\www.google.com";
    int index = web.indexOf(":");
    String protocall = web.substring(0, index);
    int index2 = web.lastIndexOf(("."));
    String domain = web.substring(index2);
    System.out.println(domain);
    System.out.println(protocall);
    if(protocall.equals("https")){
      System.out.println("Hypertext protocall");
    }else{
      System.out.println("Some other Protocall");
    }
    if(domain.equals(".com")){
      System.out.println("commercial web");
    }else{
      System.out.println("Some other type of website");
    }
  }

}
```
# Switching Conditional.
### Q. Display name of a day based on number using Switch.

```

import java.lang.*;
import java.util.*;
/**
 * relational
 */
public class relational {

   public static void main(String[] args){
     int n;
     Scanner sc = new Scanner(System.in);
     System.out.println("Enter DayNo.");
     n= sc.nextInt();

     switch (n) {
      case 1:
        System.out.println("Monday!");
        break;
      case 2:
        System.out.println("Tuesday");
        break;
      case 3:
        System.out.println("Wedmesday");
        break;
      case 4:
        System.out.println("Thrusday");
        break;
      case 5:
        System.out.println("Friday");
        break;
      case 6:
        System.out.println("Saturday");
        break;
      case 7:
        System.out.println("Sunday");
        break;
      default:
        System.out.println("Invalid Input");
        break;
     }
   }
}
```
### Q. Display website Name using Switch.
```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

     public static void main(String[] args){
      String websiteName;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the WebSite Name !");

       websiteName = sc.next();
      int indexof = websiteName.lastIndexOf(".");
      String extenssion = websiteName.substring(indexof+1);

      switch(extenssion){
        case "com":
          System.out.println("Commercial website");
          break;
        case "org":
          System.out.println("Orginational website");
          break;
        case "net":
          System.out.println("Network website");
          break;
        case "gov":
          System.out.println("government wesite");
          break;
        default :
        System.out.println("Wrong input");
        break;          
      }
     }
}
```
### Q. Menu Driven Program.
```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

    public static void main(String[] args){
      System.out.println("MENU");
      System.out.println("=====");
      System.out.println("ADD");
      System.out.println("SUB");
      System.out.println("MUL");
      System.out.println("DIV");

      System.out.println("Enter two Numbers");
      int num1, num2;
      String menu;
      Scanner sc = new Scanner(System.in);
      num1 = sc.nextInt();
      num2 = sc.nextInt();
      sc.nextLine(); //this is because  if won't be then there would be buffer issue  and it allows to another data type input.
      System.out.println("Enter Operation You want to Perform !");
      menu = sc.nextLine();

      switch(menu){
        case "ADD":
          System.out.println("Addetion of  Numbers is :"+ (num1+num2));
          break;
        case "SUB":
          System.out.println("Subtraction of  Numbers is :"+ (num1-num2));
          break;
       case "MUL":
            System.out.println("Multiplication  of  Numbers is :"+ (num1*num2));
            break;
        case "DIV":
            System.out.println("Division of Numbers is :"+ (num1/num2));
             break;
        default :
        System.out.println("Wrong Input !");
      }

    }
}
    

```
# Loops
      
 ### Q. Printing table of number.
 ```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

     public static void main(String[] args){
      int num ;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number up to  which you want to make sum");
      num = sc.nextInt();
      System.out.println("The sum is :");
      long sum =0;
      for(int i =1; i <= num; i++){
        System.out.println(sum + "+" + i + "=" +(sum + i) );
        sum = sum + i;
      }
       System.out.println("The final is: " + sum);
     }
}
 
 ```
  ### Q. Find the factorial of number  OR  find the multiplication of first n numbers.

 ```
 import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

    public static void main(String[] args){
      int n; 
      Scanner sc = new Scanner(System.in);
       System.out.println("Enter the number up to which you want to print");
       n = sc.nextInt();
      long mul = 1;
       for(int i = 1; i<=n;i++){
        System.out.println(i + "*" + mul + "=" + (mul * i));
        mul = mul * i;
       }
       System.out.println("Final Ans : "+ mul);
    }
}
       
 ```
 ### Q. Displaying the digits of given number by converting it into String first.
 ```
 import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

     public static void main(String[] args){
      long num ;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number of which digits you want to print !");
      num = sc.nextLong();

      String nums = num+"";
      for(int i = 0; i<nums.length(); i++){
        System.out.println(nums.charAt(i));
      }
     }
}
 ```
 **Another way**
 ```
 import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

     public static void main(String args []){
      int numb ;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number !");
      numb = sc.nextInt();
     while(numb>0){
       
      int n = numb%10;
      numb = numb/10;
      System.out.println(n);

     }
      
     }
}
 ```

 ### Q. Displaying the Number of Digits a that Number have.
 ```


import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

    public static void main(String [] args){
      long n; 
      int count = 0;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number you want !");
      n = sc.nextLong();
      
      while(n>0){
        n = n/10;
         count++;
        
      
      }
      System.out.println("Count of Digits is :"+ count);
    }
}
 ```
 * ## Armstrong Number :  The sum of cube of digits of that number is equal to the number.
  ### Checking weather the number is ArmStrong or not !!
     
  ```
  import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

    public static void main(String [] args){
      long n  ;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number That you want to check !");

      n = sc.nextLong();
      long sum = 0;
      long m = n;
      while(n>0){
        long num = n%10;
        n = n/10;
        sum = sum+(num*num*num);
      }
      System.out.println(sum);
      if(sum == m){
        System.out.println("Your Enterd number is ArmStrong Number !");
      }else{
        System.out.println("your Entered Number is not Armstorng !");
      }
    }
}
```
* ### Q. Reversing  a Number..
 ``` 
  import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

    public static void main(String [] args){
      long n , reversedNum = 0 ;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number That you want to check !");

      n = sc.nextLong();
     
      
      
      while(n>0){
        long num = n%10;
       reversedNum = reversedNum*10 + num; 
        n = n/10;
        
      }
      System.out.println("reversed Number is " + reversedNum );
      
    }
}
```
* ###  IF the reverse of  Number is equal to that Number then it would be called as `Plaindrome`. 

```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

    public static void main(String [] args){
      long n , reversedNum = 0 ;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number That you want to check !");

      n = sc.nextLong();
     
      long m = n;
      
      while(n>0){
        long num = n%10;
        n = n/10;
       reversedNum = reversedNum*10 + num; 
        
      }
      if(m == reversedNum){
        System.out.println("The given Number is Plaindrome ..");
      }else{
        System.out.println("The given Number is not Plaindorme");
      }
      
    }
}
```