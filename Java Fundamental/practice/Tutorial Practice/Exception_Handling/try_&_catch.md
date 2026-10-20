# classrooom Demonstration of "try & catch" 
### 1.
```


public class exception {
  
    public static void main(String[] args) {
      
      int a, b, c; 
      try{

        a =10; 
        b = 0 ; 
        c = a/b;
        System.out.println("Result is :"+c);
      }
      catch(ArithmeticException e){
        System.out.println("Division by zero");
      }
    }
}

```
## One try block culd have more than one catch blocks 
* ex : 
```


public class exception {
  
    public static void main(String[] args) {
      
     int A[] = {12,23,43,54,35,0};
     try{

       int c = A[0]/A[5];
  
       System.out.println("Division is : "+c);
       System.out.println(A[9]);
     }
     catch(ArithmeticException e){
      System.out.println("Denominator should not be 0");
     }
     catch(ArrayIndexOutOfBoundsException e){
      System.out.println("Index is Invalid");
     }
     System.out.println("Bey");
    }
}

```