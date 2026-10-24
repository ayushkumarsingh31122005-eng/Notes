### find the count of digits in number 
```
static  void countOfDigits(){
     long x = sc.nextLong();
    // System.out.println("Enter the Number ");
    int countOfDigits  = 0 ;
    while(x>0){
      int y =(int) x%10;
      countOfDigits++;
      long z = x/10;
      x = z;
    }
    System.out.println("count of Digits is : "+countOfDigits);
  }
```
#### Another way of doing the same Questions
```
public  class BasicMaths {

  static  int count(int x){
    int cnt = (int)(Math.log10(x)+1);
    return cnt;
  }
  public static void main(String args []){
    // count(1245);
   System.out.println(count(1234));  
  }
}
```
* Time complexity of the above code program is : O(log10(N));

#### Reversing a Number
```
public  class BasicMaths {

  static  long reverseNum(long n){
    long revNum=0;
    while (n>0) {
      int digit = (int)n%10;
      revNum = (revNum*10)+digit;
      n= n/10;

    }
    return  revNum;
   }

   public  static  void  main(String args []){
    System.out.println(reverseNum(12456));
   }
  }

```
## chekcing PlainDrome num
```
public  class BasicMaths{
  static  boolean checkPlainDrome(long n){
    boolean isPlainDrome = false;
    long x = n; 
     long plainDromeNum=0; 
     while(n>0){
      int digit = (int)n%10;
      plainDromeNum = plainDromeNum*10+digit;
      n=n/10;
     }
     if(plainDromeNum == x){
      return  isPlainDrome = true;
     }else{
       return isPlainDrome = false;
     }
  }

  public static void main(String args []){
    System.out.println(checkPlainDrome(121));
  }
}
```
### check ArmStrongNum
```
public  class BasicMaths {

   static  boolean isArmStrongNum(long n ){
    boolean isArmStrong = false;
     long newArmStrongNum = 0 ; 
     long x = n;
     while(n>0){
      int digit = (int)n%10;
      newArmStrongNum = newArmStrongNum+(digit*digit*digit);
      n=n/10;
     }
     if(x== newArmStrongNum){
      return isArmStrong= true;
     }else{
      return  isArmStrong = false;
     }
   }
   public  static  void main(String args []){
    System.out.println(isArmStrongNum(31));
   }
}
```
### Divisor of Number , TC: o(n);
```
 static void divisiorOfNum(long n){

    for(int i = 1; i<=n; i++){
      if(n%i==0){
        System.out.print(i+" ");
      }
    }
    System.out.println();
   }
```
### check weather the num  is prime or not with using (Time complexity = O(square root(N)))
```
/**
 * BasicMaths
 */
public class BasicMaths {

  static  void isPrime(long n){
    int count = 0 ;
    for(int i = 1; i*i<=n ; i++){
      if(n%i==0){
        count++;
        if(n/i !=i)count++;
      }
    }
    if(count ==2){
      System.out.println("The num is Prime");
    }else{
      System.out.println("The num is not Prime..");
    }
  }
  public static void main(String args []){
    isPrime(11);
  }
}
```
###   finding GCD using Equliden ALgo
```
/**
 * BasicMaths
 */
public class BasicMaths {

static   int gcd(int a, int b){
    while(a>0 && b>0){
      if(a>b) a = a%b;
      else b = b%a;
    }
    if(a==0)return  b;
    return  a; 
  }
  public static void main(String args []){
    System.out.println("The GCD of NUMS : "+ gcd(5,90));
  }
}
```