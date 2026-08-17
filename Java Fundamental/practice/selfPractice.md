# Self Practice Questions 
### 1. Temperature Converter
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
### Calculate  Simple Intrest 
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
### Swapping two numbers .
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