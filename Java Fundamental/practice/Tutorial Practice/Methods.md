### Method overLoad
```
/**
 * variable
 */
import java.lang.*;
import java.util.*;

public class variable {
      static double area(double x , double y){
         double area = x*y;
         return area;
      }
      static double area( float r){
        double area = (22f/7f)*r*r;
        return area;
      }
     public static void main(String args[]){

      Scanner sc = new Scanner(System.in);
      System.out.println("==MENU==");
      System.out.println("1.Calculate Area of Rectangle !");
      System.out.println("2.Calculate Area of Circle !");
      System.out.println("3.Exist ..");

      int choice ; 
       System.out.println("Enter your choice !");
       choice = sc.nextInt();
       switch (choice) {
        case 1:
          double l, b;
          System.out.println("Enter the length and breadth of Rectangle.");
          l = sc.nextDouble();
          b = sc.nextDouble();
          System.out.println("The area of Rectangle is : " + area(l,b));
          
          break;
          case 2:
            float r ; 
            System.out.println("Enter the Radius of the circle.");
            r = sc.nextFloat();
            System.out.println("The area of circle is : " + area(r));

           break;
          case 3:
            System.out.println("Existing ...");
            break;
        default:
           System.out.println("Invalid iput !");
          break;
       }

     }
}
```
### Overloaded method to reverse a int or array 
```
/**
 * variable
 */
public class variable {

 // Method for reversing number;
   static int reverse(int n ){
    String num = "";
    while(n>0){
      int digit = n%10; 
       num = num +digit;
       n = n/ 10; 
    }
    int x = Integer.parseInt(num);
    return x;
   }
  // another way of Reversing the number 
  // reverse = 0;
  // store the reverse = reverse*10+n%10;

   // Method for reversing an array element.
    static int[] reverse(int x[]){
      int B[] = new int[x.length];
      for(int i = x.length-1,j =0; i>=0; i--,j++){
        B[j] = x[i];
      }
      return B;
    }
  public static void main(String [] args){
    int n = 786;
    int A[] = {1,2,3,4,5,6};
    System.out.println("The reversed Num is : "+ reverse(n));
    int x[] = reverse(A);
    for(int i = 0; i<=x.length-1;i++){
      System.out.print( + x[i] + " ");
    }
  }
}
```
### Overloaded method to validate name and age.
```
/**
 * variable
 */
public class variable {
// Method for validating name .
  static boolean validate(String name){
    boolean isValid = name.matches("[a-zA-Z]");
    return isValid;
  }
    //Method for validating age 
    static boolean validate(int age){
       boolean isAdult = false;
       if(age>=18){
         isAdult = true;
       }else{
        isAdult = false;
       }
       return isAdult;
    }
   public static void main(String [] args){
    String name = "Singh";
    int age = 19;
    System.out.println("The name is valid : "+validate(name));
    System.out.println("The man  is Adult : "+validate(age));
   }
}
```

### Methods with variable arguments 
```
/**
 * variable
 */
public class variable {

    static void show(int ... A){  // this way will take the input of variable argument and various element of array too!
      // show(int A[]) --> will take only array as argument.

      for(int x :A){
        System.out.println(x);
      }
    }
     public static void main(String [] args){
      show(10,20,30);
      show(new int[] {2,3,4,5});
     }
}
```

```
/**
 * variable
 */
public class variable {

    static void show(String ... A){
      for(int i = 0 ; i<A.length; i++){
        System.out.println(i+1+". "+A[i]);
      }
      }
    
     public static void main(String [] args){
      show("Ayush","Prince","bob");
     }
}
```
### Maximum of Numbers using varagrs.
```
public class variable {
  // Method for finding maximum 
  static  int  max(int ...x){
    int max = x [0]; 
   if(x.length==0)return Integer.MIN_VALUE;
    for(int i = 0; i<x.length; i++){
      if(x[i]>max){
        max = x[i];
      }else{
        max = max;
      }
    }
    return max;
  }
  public static void main(String ... args){
     System.out.println(max(1,2,3,5,6,34,42,23,67,87));
  }
    
}
```
### Sum of all elements using varagrs.
```
public class variable {
  // Method for finding maximum 
  static  int  sum(int ...x){
    int sum = 0; 
   
    for(int i = 0; i<x.length; i++){
     sum = sum+x[i];
    }
    return sum;
  }
  public static void main(String ... args){
     System.out.println(sum(1,2,3,5,6,34,42,23,67,87));
  }
    
}
```

### Calculate Discount using varargs.
```
public class variable {
  // Method for finding maximum 
  static  double  discount(double ...x){
    double sum = 0; 
    double discount = 0;
    for(int i = 0; i<x.length; i++){
     sum = sum+x[i];
    }
    if(sum<500) {
      discount =  sum* 0.10; }
      else if( sum >500 && sum<1000){
        discount = sum * 0.20;
      }else{
        discount = sum * 0.30;
      }
    return discount;
  }
  public static void main(String ... args){
     System.out.println(discount(1,2,3,5,65.8,34,42.08,23,674.3,87.6));
  }
    
}
```