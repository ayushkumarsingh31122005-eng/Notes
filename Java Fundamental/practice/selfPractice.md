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
### B10 - Day Identifier 
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String[] args) {
      int day ; 
      Scanner sc = new Scanner(System.in);
      day = sc.nextInt();
      switch (day) {
        case 1:
          System.out.println("Monday");
          break;
        case 2:
          System.out.println("tuesday");
          break;
        case 3:
          System.out.println("Wednesday");
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
          System.out.println("Wrong data");
          break;
      }
        }
    }
                      
```
### B11 Simple Calculator
* Read two numbers and an operation (+, -, *, /, %). Perform the selected operation and handle division by zero.
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String [] args){
      int a, b;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter first numbers :");
      a = sc.nextInt();
      System.out.println("Enter second numbers :");
      b = sc.nextInt();
      String operation;
      System .out.println("Enter the operation you want to perform");
       operation = sc.next();
      switch(operation){
        case  "add" :
          System.out.println("Addition of the Numbers is :" + (a+b));
          break;
        case "sub" :
            System.out.println("Subtraction of the numbers is :"+(a-b));
            break;
        case "mul":
          System.out.println("Multiplication of the numbers is :"+(a*b));
          break;
        case "div":
          System.out.println("Division of the number is :"+ (a/b));
          break;
        case "modulo":
          System.out.println("Moudulo of the numbers is :"+(a%b));
          break;
        case "divBy0":
          System.out.println("The number is if divided by 0 then :"+(a/0));
          break;
        default :
        System.out.println("The given input is wrong !");
        break;
      }
    }
}
```
### B12 Print Multiple
* Read n and print the first 20 multiples of n in a clean tale
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String args []){
      int n; 
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the number of which you want to print multiplication");
      n = sc.nextInt();
      for(int i = 1; i<= 20 ; i++){
          System.out.println(n+"*" +i + "="+(n*i));
      }
    }
}
```
# B13 Sum 1..N
* Read n and calculate 1+2+3+...+n
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String args []){
      int n; 
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the number upto which you want to print Summation");
      n = sc.nextInt();
      int sum = 0;
      for(int i = 1; i<= n ; i++){
        sum = sum+i;
        
      }
      System.out.println("the sum is :"+ sum);
    }
}
```
### 14 Factorial 
* Read n and calculate n! using loop . use long and state the practical input limit you choose.
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String args []){
      int n; 
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the number upto which you want to print Summation");
      n = sc.nextInt();
      int Factoril = 1;
      for(int i = 1; i<= n ; i++){
        Factoril = Factoril*i;
        
      }
      System.out.println("the sum is :"+ Factoril);
    }
}
```
### 15 Digit sum 
* Read the number and the calculate the sum it's digit.
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

     public static void main(String[] args) {
      int number ; 
      int sum = 0;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number of which you want to add digit ");
      number = sc.nextInt();
      while(number>0){
        int digit = number%10;
        number = number/10;
        sum = sum+digit;
      }
      System.out.println("Sum of digit is :" + sum);
     }
}
```
### B16  Digit count 
* Count the number of dicimal digit in an integer. Decide how your Program decide 0 and negative values.
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

     public static void main(String[] args) {
      int number ; 
      int count = 0;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number of which you want to count digits ");
      number = sc.nextInt();
      while(number>0){
        int digit = number%10;
        number = number/10;
        if(digit>0){

          count = count+1; 
        }
      }
      System.out.println("count of Number is :" + count);
     }
}
```
### B17 — Reverse Number
* Reverse an integer using % and /. Preserve the sign.
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

     public static void main(String[] args) {
      int number ; 
      int reverseNum ;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number of which you want to reverse ");
      number = sc.nextInt();

      String newNum = "" ; 
      int number1 = number;
      while(number1>0){
        int digit = number1%10;
        number1 = number1/10;
         String n = digit + "";
         newNum = newNum.concat(n);
        }
        reverseNum = Integer.parseInt(newNum);
      System.out.println("Reversed of " + number +" is :" + reverseNum );
     }
}
```
## B18 --- PalinDrome Number 
* Determine wheather an integer reads the same forwads and backwards.
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

     public static void main(String[] args) {
      int number ; 
      int reverseNum ;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number of which you want to reverse ");
      number = sc.nextInt();

      String newNum = "" ; 
      int number1 = number;
      while(number1>0){
        int digit = number1%10;
        number1 = number1/10;
         String n = digit + "";
         newNum = newNum.concat(n);
        }
        reverseNum = Integer.parseInt(newNum);
        if(number == reverseNum){

          System.out.println("The given Number is PlainDrome");
        }else{
          System.out.println("The given Number is not PlainDrom !");
        }
     }
}
```
###  B19 — Prime Checker
* Read n and determine whether it is prime. Do not check every number up to n if you can avoid unnecessary work.

```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

     public static void main(String[] args) {
      int number ; 
      
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number of which you want to check it  is Prime or Not ? ");
      number = sc.nextInt();
      
      boolean isPrime = true; 
      if (number >1){
        isPrime = false;

      }else{
        for(int i = 2; i< number ; i++){
          if(number % i ==0){
            isPrime = false;
            break;
          }
        }
      }
      if (isPrime) {
        System.out.println(number + " is a prime Number");
      }else{
        System.out.println(number + " is a Not prime Number");

      }
      
     }
}
```
## B20 — Primes in a Range ****
* Read two bounds and print every prime between them.
```
import java.lang.*;
import  java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String[] args) {
       int num1 ,num2 ;
       Scanner sc = new Scanner(System.in);
       System.out.println("Enter num1 and num2");
       num1 = sc.nextInt();
       num2 = sc.nextInt();
       int countOfPrime = 0 ;
       boolean isPrime = true;

    


      for(int newNum = num1 ; newNum<= num2; newNum++){
         isPrime = true;
         if (newNum<2) {
          isPrime = false;
         }
         for(int j = 2; j<newNum ; j++){
          if (newNum%j == 0) {
            isPrime = false;
            break;
          }
         }
         if(isPrime){
          countOfPrime++;
         }
      }
      System.out.println("Number of PrimNumbers between the two Numbers is :"+countOfPrime);
    }
}
```
### B21 - Quadratic Equation
* Read a,b,c and compute the discriminant and report two real roots , one repeated real root , or no real roots.
```
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String [] args){
      // Quardratic Equation is = ax^2+bx+c = 0;
      int a ,b,c;
      System.out.println("Enter the a,b,c");
      Scanner sc = new Scanner(System.in);
      a = sc.nextInt();
      b  = sc.nextInt();
      c = sc.nextInt();
      int discriment  = (b*b)-(4*a*c);
      if(discriment>0){
        double root1 = (-b + Math.sqrt(discriment))/2;
        double root2 = (-b - Math.sqrt(discriment))/2;
          
        System.out.println("Two roots since Discriment is greater than 0 and the roots are :"+"root-1 = "+root1 + "and root 2 = "+root2);
      }else if(discriment<0){
        System.out.println("Two imaginary roots since discriment is smaller than 0");
      }else{
        double root = -b/(a*2);
        System.out.println("Only one root since discriment is equal to 0 and the root is :"+ root);
      }

    }
}
```
### B22 — String Length Without length()
* Read a String and determine its length by iterating over characters.
 
 ```
 import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String [] args){
      String str ;
      Scanner sc = new Scanner(System.in);
      System.out.println("Etner the String of which you want to count charcter.");
      str = sc.nextLine();
      int countOfChar=0;
    
      for(char ch: str.toCharArray()){
        countOfChar ++;
      }
      System.out.println("Cont of char = "+countOfChar);
    }
}
 ```
 ###  B23 — First and Last Character
 * Read a non-empty String and print its first character, last character, and their Unicode values.
 ```
 import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

     public static void main(String [] args){
      String str ;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the String.");
      str = sc.next();
      String firstChar = "";
      String lastChar = "";
        char [] letters = str.toCharArray();
        firstChar = String.valueOf(letters[0]);
         int firstUnicode =letters[0];
         lastChar = String.valueOf(letters[letters.length-1]);
         int lastUnicode =letters[letters.length-1];
        System.out.println( "First char of String :"+firstChar +" and it's unicode is "+firstUnicode );

        System.out.println("Last char of string :"+lastChar +" and it's unicode is "+lastUnicode);
     }
}
 ```
 ### B24 — Basic Email Split
 *  Given an email-like string, extract the username and domain using indexOf() and substring(). Also report whether '@' exists
 ```
 import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String [] args){
      String email ;
      Scanner sc = new Scanner(System.in);
      
      System.out.println("Enter the email !");
      email = sc.nextLine();
      int ind1 = email.indexOf("@");
      String userName = email.substring(0, ind1);
      String domainName = email.substring( ind1+1);
      boolean doesCharHave = email.contains("@");
      System.out.println("UserName = "+ userName);
      System.out.println("domainName = "+ domainName);
      System.out.println("does the email id contain @  = "+ doesCharHave);
    }
}
 ```
 # Intermediate. 
 ### I01 -- Armstrong Number 
 ```
//Armstrong Number -: if number is equal to the sum of it's digit cube 
import java.lang.*;
import java.util.*;
/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String [] args){
      int num ; 
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number !");
      num = sc.nextInt();
      int digit;
      int cubeSum = 0;
      int newNum = num ;
      
      while(num>0){
          digit = num%10;
          num = num/10;
          cubeSum = cubeSum + digit*digit*digit;
      }

      if(cubeSum == newNum){
        System.out.println("The given number is armStrong !");
      }else{
         System.out.println("The given Number is not ArmStrong !");
      }
    }
}
 ```
 ### I02 — Perfect Number
 * Check whether n equals the sum of its proper positive divisors..
 ```
 //Armstrong Number -: if number is equal to the sum of it's digit cube 
import java.lang.*;
import java.util.*;
/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String [] args){
      int num  ; 
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Number !");
      num = sc.nextInt();
     
      int properDivisorSum = 0;
      int newNum = num ;
      int properDivisor =0 ;
    
       
        for(int i = 1; i<num; i++){
          if(num % i == 0){
            properDivisor = i;
            properDivisorSum = properDivisorSum+properDivisor;
            
           
          }
        }
      
      if(properDivisorSum == newNum){
        System.out.println("The given Number is perfect !");
      }else{
        System.out.println("The given Number is not perfect !");
      }
    }
}
 ```
 ### I03 Finding LCM and GCD
   * Read two numbers and then find the LCM of the number and GCD .
   ```
   import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String [] args){
      int a, b;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the number a and b");
      a  = sc.nextInt();
      b = sc.nextInt();
      int commonFactor ;
      int [] arr1 = new int[a];
      int [] arr2 = new int[b];
      int index1 = 0 ;
      int index2 = 0 ;
      //find factor of a

      for (int i = 1; i< a; i++){
        if(a % i==0){
          arr1[index1] =i;
          index1++;
        }
      }

      //Finding factor of b

      for(int  i =1; i<b; i++){
        if(b%i == 0){
          arr2[index2] = i;
          index2++;
        }
      }

      // GCD 

      int gcd = 0;

      for(int i =0; i<index1; i++){
        for(int j = 0 ; j<index2; j++){
           if(arr1[i]== arr2[j]){
            if(arr1[i]>gcd){
              gcd = arr1[i];
            }
           }
        }
      }
      System.out.println("GCD = "+gcd);

     //Finding Lcm
     int Lcm = (a*b)/gcd;
     System.out.println(" LCM = "+Lcm);
    }
}
   ```
   ### I04 — Second Largest
   *  Read three distinct integers and determine the second-largest without sorting.
   ```
   // Findig the second largest number between three numbers , without sorting.
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main (String [] args){
      int a, b,c;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the three Numbers !");
      a = sc.nextInt();
      b = sc.nextInt();
      c = sc.nextInt();
      int largest =0;
      int secdondLargest = 0;
      // Findig largest Number 
      if(a>b && a>c){
        largest = a;
    }else if(b>c && b>a){
      largest =b;
    }else if(c>a && c>b){
      largest = c;
    }
      // Finding secondLargest Number.
      if(a == largest ) {
        secdondLargest = Math.max(b,c);
        
        }else if(b== largest ){
          secdondLargest = Math.max(a,c);
         
        }else if(c == largest ){
          secdondLargest = Math.max(a,b);
          
        }

        System.out.println(" largest Number is "+ largest);
        System.out.println("Second largest Number is "+ secdondLargest);


         
    }
}
   ```
   ### I05 — Fibonacci Series
   *  Print the first n Fibonacci numbers iteratively. Avoid recursive solutions
   ```
   // Findig the second largest number between three numbers , without sorting.
import java.lang.*;
import java.util.*;

/**
 * selfPractice
 */
public class selfPractice {

    public static void main (String [] args){
      int a, b,lastTerm;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the first Term !");
      a = sc.nextInt();
      System.out.println("Enter the second Term");
      b = sc.nextInt();
      System.out.println("Enter the last Term !");
      lastTerm = sc.nextInt();
      String fabonacciSeries = a + "," + b;
      int thirdTerm = a+b;
       while(thirdTerm <= lastTerm){
         fabonacciSeries = fabonacciSeries +   "," + thirdTerm;
         a= b;
         b = thirdTerm;
         thirdTerm = a+b;
        

       }
       System.out.println(fabonacciSeries);
      
    }
}
         
   ```
   ###  Printing some Pattern 
   ```
    * - - - -
    ** - - -
    *** - -
    **** -
    *****
   ```
   #### solution 
   ```
   /**
 * selfPractice
 */
public class selfPractice {

     public static void main(String[] args) {
      
        for(int i = 1; i<=5 ; i++){

          for(int j = 1 ; j<= i ; j++){
            System.out.print("*");
          }
          for(int k = 4; k>=i; k--){
            System.out.print(" -");
          }
          System.out.println();
        }
     }
}
   ```
   # Pattern Printing.
  #### 1.
   ```
  *
  **
  ***
  ****
  *****
  Printing this Pattern 
  ```
  * solution 
  ```

public class selfPractice {

     public static void main(String [] args){
      for(int i = 1; i<=5 ; i++){
        for(int j =1; j<=i ; j++){
          System.out.print("*");
        }
        System.out.println();
      }
     }
}
  ```

* Q 2 Printing this Pattern 
```
             *
          *  *
         * * *
       * * * *
     * * * * *
```
* solution 
```
/**
 * selfPractice
 */
public class selfPractice {

     public static void main(String [] args){
      for(int i = 1; i<=5 ; i++){
        for(int j = 4; j>=i ; j--){
          System.out.print(" ");
        }
        for(int k = 1 ; k<=i; k++){
          System.out.print("*");
        }
        System.out.println();
      }
     }
}
```
### Q3 Printing this pattern 
```
* * * * * 
* * * * 
* * * 
* * 
* 
```
* solution :
```
public class selfPractice {

     public static void main(String [] args){
      for(int i = 1; i<=5 ; i++){
        for(int j = 5; j>=i ; j--){
          System.out.print("* ");
        }
        
        System.out.println();
      }
     }
}
```
### Q4. Printing this pattern 
 ```
 * * * * *
   * * * *
     * * *
       * *
         *
 ```
 * Solution 
 ```
 /**
 * selfPractice
 */
public class selfPractice {

     public static void main(String [] args){
      for(int i = 1; i<=5 ; i++){
       for(int j = 2; j<=i; j++){
        System.out.print("  ");
        }
        for(int k = 5; k>=i; k--){
          System.out.print(" *");
        }
        System.out.println();
      }
     }
}
 ```
 ### Q5. Printing this Pattern 
 ```
  *
  * *
  * * *
  * * * *
  * * *
  * *
  *
 ```
 * solution 
 ```
 /**
 * selfPractice
 */
public class selfPractice {

     public static void main (String args [] ){
      for (int i = 1 ; i<=4; i++){
        for (int j = 1 ; j<= i; j++){
          System.out.print(" *");
        }
        System.out.println();
      }
      for(int i = 1; i<= 3; i++){
        for(int j = 3; j>= i ; j--){
          System.out.print(" *");
        }
        System.out.println();
      }
     }
}
 ```

### Printing this pattern 
```
      *
    * * *
   * * * * *
  * * * * * * *
 * * * * * * * * *
```
* solution 
```
/**
 * selfPractice
 */
import java.lang.*;
import java.util.*;

public class selfPractice {

     public static void main(String args [] ){
      int n ; 
       Scanner sc = new Scanner(System.in);
       System.out.println("Enter the number of rows you want !");
       n = sc.nextInt();
      for(int i = 1; i<= n; i++){
         // My approach for the spaces.
        // for (int j = 4; j>= i;j--){
        //   System.out.print(" ");
        // }

        //Tutors approach for the spaces 
         for(int j = 1; j<=n-i; j++){
          System.out.print(" ");
         }
         for(int k = 1; k<= 2*i -1 ; k++){
          System.out.print(" *");
         }

        System.out.println();
      }
     }
}

```
### Q. Print this pattern 
```
 * * * * * * * * *
  * * * * * * *
   * * * * *
    * * *
     *
```
* Solution 
```
/**
 * selfPractice
 */
import java.lang.*;
import java.util.*;

public class selfPractice {

     public static void main(String args [] ){
      int n ; 
       Scanner sc = new Scanner(System.in);
       System.out.println("Enter the number of rows you want !");
       n = sc.nextInt();
      for(int i =n; i>=1; i--){
         for(int j = 1; j<= n-i; j++){
           System.out.print(" ");

         }
         for(int k =1 ; k<= 2*i -1; k++){
          System.out.print(" *");
         }
         System.out.println();
      }
     }
}

```
