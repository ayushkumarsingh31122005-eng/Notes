# Self Practice Questions 
### Q1. Temperature Converter
```
import java.lang.*;
import java.util.*;
public class selfPractice {
  
  public static void main(String[] args) {
    float F;
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter Degree Celcius);
    float C = sc.nextFloat();
    F =(C*(9f/5f))+32;
    System.out.println("Degree F :"+F);
  }
}
```
### Q2 Calculate  Simple Intrest 
```
public class selfPractice {

  public static void main(String[] args) {
    
    double P,R,T;
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter Principal, Rate , Time to calculate Simple Intrest ");
    P= sc.nextDouble();
    R= sc.nextDouble();
    T= sc.nextDouble();
    double SI = (P*R*T)/100;
    System.out.println("Simple INtrest is :" + SI);
  }

}
```
### Q3. Swapping two numbers .
```
 */
public class selfPractice {

  public static void main(String[] args) {
    int a = 10 , b= 20;
    a = a^b;
    b=a^b;
    a = a^b;
    System.out.println("a = " +a +" b = "+b);
  }
}
```
### Q4. Character Analyzer
* Take one character from the user and print:

Character
ASCII/Unicode value
Whether it is uppercase or lowercase
Previous character
Next character

```
import java.lang.*;
import java.util.*;
public class selfPractice {

  public static void main(String [] args){
    //taking input Character from the user ...
    Scanner sc = new Scanner(System.in);
    char Character = sc.next().charAt(0);
    int value = Character;
    System.out.println(value);
    // System.out.println((char)(++value));
    System.out.println((char)(--value));

  } 
}
```
# Q5. Swap Two Numbers — Three Ways

  Take two integers and swap them using:

 * A third variable
 * Arithmetic operators
 *  XOR 
 * using third variable.
 ```
 public class selfPractice {

    public static void main(String[] args){
        // taking input form user 
        System.out.println("Taking input from the user");
        Scanner sc = new Scanner(System.in);
          int a = sc.nextInt();
          int b = sc.nextInt();
          int c ;
          c = a;
          a=b;
          b=c;
          System.out.printf("Value of a is : %d\n",a);
          System.out.printf("Value of b is : %d",b);

    }
}
```
# Q6.
* Calculating unit, tens, hundreds digit of three digit number.
```
public class selfPractice {

    public static void main(String[] args){
        // taking input form user 
        System.out.println("Enter three digit number");
        Scanner sc = new Scanner(System.in);
        double  number = sc.nextDouble();
         //extracting  unit digit of number
         int unitDigit = (int)(number)%10;
            System.out.printf("Unit digit of the Number given by you is : %d\n",unitDigit);
            // extracting tens digit 
            int tensDigit = (int)((number%100)/10);
            System.out.printf("Tens digit of number given by you is  : %d\n",tensDigit);
         //extracting hundreds digit...   
        int hundredsDigit = (int)(number)/100;
        System.out.printf("Hundreds digit of Number given by you : %d", hundredsDigit);
        // int tensDigit = (int)tens%10;
        // Reversing the number given by ..
        System.out.printf("your reversed number is : %d%d%d",unitDigit,tensDigit,hundredsDigit);
    }
}
```
### B01. Rectangle Calculator
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice 
 */
class selfPractice{
  public static void main (String[] args){
   
   int l , b;
   Scanner sc = new Scanner(System.in);
   System.out.println("Enter length ");
    l = sc.nextInt();
    System.out.println("Enter breadth :");
    b = sc.nextInt();
    long perimeter = 2*(l+b);
    long area = l*b;
    System.out.println("Area = "+ area + "  and  " + "Perimeter = "+perimeter);

    }
}

```
### B04.Read cost price and selling price. Report profit/loss amount and percentage
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String[] args) {
      long costPrice , sellingPrice ;

      Scanner sc = new Scanner(System.in);

      System.out.println("Enter costPrice");
      costPrice = sc.nextLong();

      System.out.println("Enter SellingPrice");
      sellingPrice = sc.nextLong();

      if(sellingPrice>costPrice){
        long profit = sellingPrice - costPrice;
        int profitPercent = (int)((profit*100)/costPrice);
        System.out.println("Profit is :" + profit + " and profit percent is :" + profitPercent+"%");
        
      }else{
        
        long loss = costPrice - sellingPrice  ;
        int losstPercent = (int)((loss*100)/costPrice);
        System.out.println("loss is :" + loss + " and loss percent is :" + losstPercent+"%");
        
      }

    }
}
```
### B05 : Read total seconds and convert them into hours, minutes, and remaining seconds
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

     public static void main(String[] args){
      long second;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the seconds !");
       second = sc.nextLong();
       long minutes = second / 60 ;
       long hours =  minutes /60;
       long second2 = second%60;
       System.out.println("Hours : "+hours +"\n Minutes : "+ minutes +"\n second : " + second2);
     }
}
```
### B06 
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

     public static void main(String[] args){
      char ch ; 
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Charcter !");
      ch = sc.next().charAt(0);
      int val = ch;
      int previous = ch-1;
      int next = ch+1;
      System.out.println("unicode of Char - "+ ch +" is : "+ val +"\n privous is :"+ previous + "\n next is : "+ next);

     }
}
```
### B08 --> Read three integers and find the largest without using Math.max(). Handle ties clearly.
* Without **Math.max()**.
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String[] args){
      int a, b, c;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter a");
      a = sc.nextInt();
      
      System.out.println("Enter b");
      b = sc.nextInt();

      System.out.println("Enter c");
      c = sc.nextInt();
      int greatest = 0 ;
      if(a>b && a>c){
        System.out.println("greatest Number is 'a' :"+ a);
        // greatest = a; 
      }else if(b> c && b>a){
        System.out.println("Greatest Number is  'b' :"+b);
        // greatest = b;
      }else{
        System.out.println("Greatest Number is 'c' :"+c);
      }
    }
}
```
* Using **Math.max()**
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String[] args){
      int a, b, c;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter a");
      a = sc.nextInt();
      
      System.out.println("Enter b");
      b = sc.nextInt();

      System.out.println("Enter c");
      c = sc.nextInt();
      int max = Math.max(a,b);
      System.out.println("Greatest is :"+Math.max(c,max) );
    }
}
```
###  B09 — Leap-Year Validator
* Read a year and determine whether it is a leap year using the complete Gregorian rule
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String[] args) {
      int year;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter Year!");
      year = sc.nextInt();

     if (year % 400 == 0) {
    System.out.println("Leap year");
} else if (year % 100 == 0) {
    System.out.println("Not a leap year");
} else if (year % 4 == 0) {
    System.out.println("Leap year");
} else {
    System.out.println("Not a leap year");
}
        }
    }
                      
```
