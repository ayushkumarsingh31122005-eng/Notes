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
