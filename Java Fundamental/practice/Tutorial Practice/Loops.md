
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
* ### Displaying the Number in words after reversing it..
```
 import java.lang.*;
 import java.util.*;

 /**
  * relational
  */
 public class relational {
 
    public  static void main(String args []){
        int n , reversedNum=0;
        String str="" ;
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the Number !");
        
        n = sc.nextInt();
        while(n>0){
          int r =  n%10;
          reversedNum= reversedNum*10 +1;
          n = n/10;
          str = str + r;  
        }
        String newNum = "";
        
        for(int i =0; i<str.length() -1; i++){
          
          switch (str.charAt(i)){
            case '0' :
            newNum = newNum + "Zero ";
            break;
            case '1':
              newNum = newNum + "one ";
              break;
            case '2':
              newNum = newNum + "Two ";
              break;
            case '3':
              newNum = newNum + "Three ";
              break;
            case '4':
              newNum = newNum + "four";
              break;
            case '5':
              newNum = newNum + "five ";
              break;
            case '6':
              newNum = newNum + "six ";
              break;
            case '7':
              newNum = newNum + "seven ";
              break;
            case '8':
              newNum = newNum + "eight ";
              break;
              case '9':
                newNum = newNum + "Nine ";
          }
        }
        System.out.println("Number is :" + newNum);
    }
 }
```
### Q. Displaying Arithmetic Progression.
##### //Arithematic Progression ..
// here with common difference , starting number and up to howmuch number ...  Usiing this we have to print the seris  that is Arithematic Series..
* general Form is = a+ ad+ a2d+ a3d+ a4d + .... + aNd..
```
 */
public class relational {

    public static void main(String [] args){
      int startNum, commonDiff , upToNum;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Starting Num..");
      startNum = sc.nextInt();
      System.out.println("Enter the CommonDiff Num..");
      commonDiff = sc.nextInt();
      System.out.println("Enter the upToNum Num..");
      upToNum = sc.nextInt();
      String arithmeticProgression = "";
      int term = startNum;

      for(int i = 0; i<= upToNum;i++){

        System.out.print(term + ",");
        term = term+commonDiff;
        
      }
      
    }
}
```

#### Q. Display GP series 
                  
* general form =a +ar + ar^2 + ar^3 + ar^4 + ar^5 .. 

```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

      public static void main(String [] args){
        int a , r , upToNum;

        Scanner sc = new Scanner(System.in);

        System.out.println("Enter the Starting Num");
        a = sc.nextInt();

        System.out.println("Enter the  ration");
        r = sc.nextInt();

        System.out.println("Enter the uptoNum");
        upToNum = sc.nextInt();
        int term = a;
        String geometricProgression = "";
        for(int i = 0 ; i< upToNum; i++){
          System.out.print(term +",");
          term = term*r;
        }
        
      }
}
```

### // Fibonacci Series : it is a series where first two terms are given and third term is  found by adding previous two terms .

```


import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

    public static void main(String args []){

      int  firstTerm, secondTerm, thirdTerm=0 , howmuchTerm;

      Scanner sc = new Scanner(System.in);

      System.out.println("Enter First Term ");
      
      firstTerm = sc.nextInt();
      System.out.println("Enter second term");

      secondTerm = sc.nextInt();
      System.out.println("Up to how much term you want to print !");

      howmuchTerm = sc.nextInt();

        System.out.print(firstTerm + "," + secondTerm +",");

      for(int i = 0 ; i<= howmuchTerm -1; i++){

        thirdTerm = firstTerm  + secondTerm; 

        System.out.print(thirdTerm + ",");
        
        firstTerm = secondTerm;
        secondTerm = thirdTerm;
      }

    }
}
```
### Playing with Nested Loops.
```
/**
 * relational
 */
public class relational {

    public static void main (String args []){
       for(int i = 1 ; i<=5 ; i++){
        for(int j = 1; j<=5 ; j++){
          System.out.print("("+j +") ");
        }
        System.out.println("");
       }
    }
}
```
2nd 
```
public class relational {

    public static void main (String args []){
       for(int i = 1 ; i<=5 ; i++){
        for(int j = 1; j<=5 ; j++){
          System.out.print("("+i +") ");
        }
        System.out.println("");
       }
    }
}
```
3rd
```
public class relational {

    public static void main (String args []){
       for(int i = 1 ; i<=5 ; i++){
        for(int j = 1; j<=5 ; j++){
          System.out.print("("+(i+j) +") ");
        }
        System.out.println("");
       }
    }
}
```
4t
```
/**
 * relational
 */
 */
public class relational {
  
    public static void main (String args []){
      int count  =0;
       for(int i = 1 ; i<=5 ; i++){
        for(int j = 1; j<=5 ; j++){
          System.out.format("%02d ",++count);
        }
        System.out.println("");
       }
    }
}
```
5th
```
/**
 * relational
 */
public class relational {
  
    public static void main (String args []){
      
       for(int i = 1 ; i<=5 ; i++){
        for(int j = 1; j<=i ; j++){
          System.out.print(j+"");
        }
        System.out.println("");
       }
    }
}
```
6th
```
/**
 * relational
 */
public class relational {
  
    public static void main (String args []){
      int count = 0 ;
       for(int i = 1 ; i<=5 ; i++){
        for(int j = 1; j<=i ; j++){
          System.out.print(++count+" ");
        }
        System.out.println("");
       }
    }
}
```
7th
```
/**
 * relational
 */
public class relational {
  
    public static void main (String args []){
      
       for(int i = 1 ; i<=5 ; i++){
        for(int j = 1; j<=5-i+1 ; j++){
          System.out.print(j+" ");
        }
        System.out.println("");
       }
    }
}
```
8th
```
/**
 * relational
 */
public class relational {
  
    public static void main (String args []){
      int count = 0;

       for(int i = 1 ; i<=5 ; i++){
        for(int j = 1; j<=5-i+1 ; j++){
          System.out.format(" %02d ", ++count);
        }
        System.out.println(" ");
       }
    }
}
```
9th
```
/**
 * relational
 */
public class relational {
  
    public static void main (String args []){
      int count = 0;
      
       for(int i = 1 ; i<=5 ; i++){
        for(int j = 1; j<=5 ; j++){
          if(j>=i){
            System.out.print("* ");
          }else{
            System.out.print("  ");
          }
        }
        System.out.println(" ");
       }
    }
}
```
10th
```
/**
 * relational
 */
public class relational {
  
    public static void main (String args []){
      int count = 0;
      
       for(int i = 1 ; i<=5 ; i++){
        for(int j = 1; j<=5 ; j++){
          if(5<j+i){
            System.out.print("* ");
          }else{
            System.out.print("  ");
          }
        }
        System.out.println(" ");
       }
    }
}
```