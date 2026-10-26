# Infinite Recursion
```
public class Recursion {
static  void func(){
  System.out.println(1);
  func();
 } 
 
 public  static void main(String args []){
  func();
 }
}

```
# Print Name 5 times using Recursion 

```
public  class Recursion {

 static  void func(int i ,int  n){
     if(i>n) return ; // Base condition
     System.out.println("Singh");
     func(i+1,n);
 }
  public static void main(String args []){
    func(1,5);
  }
}
```
#### Time complexity is : O(N);

# Q. Print numbers between using Recursion..
```
import java.util.Scanner;

public class Recursion{
  static void func(int i ,int n){
    if(i>n)return ;

    System.out.println(i);
    func(i+1,n);
  }
  public  static void main(String args []){
    Scanner sc = new Scanner(System.in);
    int a = sc.nextInt();
    int n = sc.nextInt();
    func(a, n);
  }
}
```
# Q. Printing Numbers in reverse order..
```
import java.util.Scanner;

public class Recursion{
  static void func(int i ,int n){
    if(i<n)return ;

    System.out.println(i);
    func(i-1,n);
  }
  public  static void main(String args []){
    Scanner sc = new Scanner(System.in);
    int a = sc.nextInt();
    int n = sc.nextInt();
    func(a, n);
  }
}
```
# Printing Numbers using 1 to N using backTracking...
```
import  java.util.*;

public class Recursion{
  
  static void func(int i , int n){
    if(i<n) return ; 
    func(i-1,n); // writing function one step above of printing will print the numbers in same order using   Back tracking..

    System.out.println(i);
  }
  public static void main(String args []){
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter the ending term and starting term");
    int i = sc.nextInt();
    int n = sc.nextInt();
    func(i, n);
  }
}
```

# Printing the Numbers in Oposite order (by BackTracking);
```
// Print from N to 1 (By Backtracking..)
public  class Recursion {

  static  void func(int i , int n ){
    if(i==n+1)return ;
    func(i+1, n);
    System.out.println(i);
  }
  public  static  void main(String args []){
    func(1,3);
  }
}
```
