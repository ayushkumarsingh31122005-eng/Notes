#### 22 Different 
```
import java.util.*;

public  class Pattern{
static  Scanner s = new Scanner(System.in);

 static  int num = s.nextInt();

 static  void pattern3(){
    Scanner sc = new Scanner(System.in);
    System.out.println("enter the no of time you want to print the star ");
    int x = sc.nextInt();
    for (int i = 1 ; i<=x;i++){
      System.out.println();
      for(int j = 1; j<=i; j++){
        System.out.print(j+" ");
      }
    }
  }

  static  void pattern4(){
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter the Number up to you want to print ");
    int x = sc.nextInt();
     // loops for the pattern 
     for(int i = 1 ; i <=x; i++){
      System.out.println();
      for(int j =1; j<=i; j++){
        System.out.print(i);
      }
     }
  }
  static  void pattern5(){
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter the Number up to you want to print ");
    int x = sc.nextInt();
     // loops for the pattern 
     for (int i = 1 ; i<= x ; i++){
       System.out.println();
       for(int j = x; j>=i; j--){
        System.out.print("* ");
       }
     }
  }
  static  void pattern6(){
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter the Number up to you want to print ");
    int x = sc.nextInt();
     // loops for the pattern 
     for (int i = 1 ; i<= x ; i++){
       System.out.println();
       for(int j = 1; j<=x-i+1; j++){
        System.out.print(j + " ");
       }
     }
  }
  static  void pattern7(){
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter the Number up to you want to print ");
    int x = sc.nextInt();
     // loops for the pattern 
     for (int i = 1 ; i<= x ; i++){
       System.out.println();
       for(int j = 1; j<=i; j++){
        System.out.print("* ");
       }
     }
  }

   static  void pattern8(){
    Scanner sc = new Scanner(System.in);
    System.out.println("ENter the Number of rows..");
    int r = sc.nextInt();

    for(int i = 0; i<=r; i++){
    // Space 
      for(int j =0;j<r-i-1;j++){
        System.out.print(" ");
      }
      // Star
      for(int j = 0 ; j<2*i+1; j++){
        System.out.print("*");
      }
      // space
      for(int j  = 0 ; j<r-i-1; j++){
        System.out.print(" ");
      }
      System.out.println();
    }
   }
    
   static  void  pattern9(){
    Scanner sc = new Scanner(System.in);
    System.out.println("Enter the no of Rows ");
    int n = sc.nextInt();
    for(int i =0 ; i<n; i++){
      // spcae 
      for(int j = 0 ; j<i; j++){
        System.out.print(" ");

      }
      // Star 
      for(int j = 0 ; j<2*n-(2*i+1); j++){
        System.out.print(" * ");
      }
      // space 
      for(int j = 0 ; j<i;j++){
        System.out.print(" ");
      }
      System.out.println();
    }
   }

   static void pattern10(){
     Scanner sc = new Scanner(System.in);
    System.out.println("Enter the no of Rows ");
    int n = sc.nextInt();
    for(int i = 0 ; i<n ; i++){
        for(int j = 0 ; j<n - i -1; j++){
          System.out.print(" ");
        }
        for(int j = 0 ; j<2*i+1; j++){
          System.out.print("* ");
        }
        for(int j = 0 ; j<n-i-1; j ++){
          System.out.print(" ");
        }
        System.out.println();
    }

    for(int i = 0 ; i<n; i++){
      for(int j = 0 ; j<i ; j++){
        System.out.print(" ");
      }
      for(int  j = 0 ; j<2*n-(2*i+1);j++){
        System.out.print("* ");
      }
      for(int j = 0 ;j<i ; j++){
        System.out.print(" ");
      }
      System.out.println();
    }
   }

   static void pattern11(){
     System.out.println("Enter the number of rows");
    for(int i = 1 ; i<=2*num-1; i++){
      int  stars= i ;
      if(i>num){
        stars  = 2*num-i;
      }
      for(int j = 1; j<=stars ; j++){
         System.out.print("*");
      }
      System.out.println();
    }
   }

   static  void pattern12(){
    for(int i = 0 ; i<= num; i++){
      int start = 1; 
      if(i%2== 0){
       start = 1; 
      }else{
        start = 0;
      }
      for(int j = 0; j<=i; j++){
        System.out.print(start);
        start = 1-start;
      }
      System.out.println();
    }
   }

   static  void pattern13(){
    int space = 2*(num-1);
    for(int i = 1 ; i<=num; i++){
      // num
      for(int j = 1 ; j<=i; j++){
        System.out.print(j);
      }
      // space
       for(int j = 1; j<=space; j++){
        System.out.print(" ");
       }
      // Numbers 
      for(int j = i; j>=1; j--)
        System.out.print(j);

      System.out.println();
      space -= 2; 
    }
   }
  
   static void pattern14(){
    int number =  1;
    for(int i = 0 ; i<=num; i++){
      for(int j = 0 ; j<= i ; j++){
        System.out.print(number +" ");
        number++;
      }
      System.out.println();
    }
     
   }
  
   static void pattern15(){
     char a = 65;
     for(int i = 0; i <= num; i++){
      for(int j = 0 ; j<=i;j++){
        System.out.print((char)(a+j)+" ");
        // a++;
      }
      System.out.println();
     }
   }
  
   static void  pattern16(){
    char a =65;
    // loops
    for(int i = 0 ; i<=num; i++){

       for(int j = num ; j>=i; j--){
        System.out.print((char)a);
        a++;
      }
       a= 65;
       System.out.println();
    }
   }
   
  static void pattern17(){
    char a = 65; 
    // loops 
    for(int i = 0 ; i<=num; i++){
      for(int j = 0 ; j<=i; j++){
        System.out.print((char)a);
      }
      a++;
      System.out.println();
    }
  }

  static void pattern18(){
    for(int i = 0; i<=num; i++){
    // Space 
      for(int j =0;j<num-i-1;j++){
        System.out.print(" ");
      }
      // Characters
      char a = 65;
      int breakPoint = (2*i+1)/2;
      for(int j = 0 ; j<=2*i+1; j++){
        System.out.print((char)a);
      if(j<=breakPoint) a++;
      else a--;
      }
      // space
      for(int j  = 0 ; j<num-i-1; j++){
        System.out.print(" ");
      }
      System.out.println();
    }
  }
  
  static void pattern19(){
    char e = 69;
    for(int i = 0 ; i<=num; i++){
      for(int j = (int)e-i; j<=(int)e; j++){
        System.out.print((char)j);
        
      }
      
      System.out.println();
    }
  }
  
  static void  pattern20(){
    int iniS  =0 ;
    for(int i = 0 ; i<=num; i++){
      // stars 
      for(int j = 0 ; j<=num -i; j++){
        System.out.print("*");
      }
      // Spaces 
      for (int j  = 0 ; j<iniS; j++){
        System.out.print(" ");
      }
      // Stars
      for(int j = 0 ; j<=num-i; j++){
        System.out.print("*");
      }
      iniS +=2;
      System.out.println();
    }
    // For Lower Symmetry...
    iniS =num*2;
    for(int i =0 ; i<=num; i++){
      // stars
      for(int j = 0; j<=i; j++){
        System.out.print("*");
      }
      for(int j = 0 ; j<iniS; j++){
        System.out.print(" ");
      }
      for(int j = 0; j<=i; j++){
        System.out.print("*");
      }
      iniS -=2; 
      System.out.println();
    }
  }

  static  void pattern21(){
  int space = 2*num-2; 
   for(int i = 1 ; i<=2*num-1; i++){
    int stars = i; 
    if(i>num) stars = 2*num - i; 
    // stars 
    for(int j =1 ; j<=stars; j++){
      System.out.print("*");
    }
    //space
    for(int j = 0 ; j<=space;j++){
      System.out.print(" ");
    }
    //stars
    for(int j =1; j<stars;j++ ){
      System.out.print("*");
    }
    System.out.println();
    if(i<num) space -=2; 
    else space +=2;
   }
 }

 static void pattern22(){
  for(int i = 0 ; i<num; i++){
    for(int  j = 0 ;j<num; j++){
      if(i==0 || i == num-1 || j==0 || j== num-1){
        System.out.print("*");
      }else System.out.print(" ");
    }
    System.out.println();
  }
 } 

 static void pattern23(){
  for (int i = 0 ; i<num; i++){
    for(int j = 0 ;j<num;j++){

      if(i==0||i==num-1|| j==0||j==num-1){
        System.out.print(4+" ");
      }
      else if(i==1||i==num-2||j==1||j==num-2){
        System.out.print(3+" ");
      }
      else if(i==2||i==num-3||j==2||j==num-3){
        System.out.print(2+" ");
      }else System.out.print(1+" ");
    }
    System.out.println();
  }
 }
 public static void main(String args []){
      // pattern3();
      // pattern4();
      // pattern5();
      // pattern6();
      // pattern7();
      // pattern8();
      // pattern9();
      //  pattern10();
      // pattern11();
      // pattern12();
      // pattern13();
      // pattern14();
      // pattern15();
      // pattern16();
      // pattern17();
      // pattern18();
      // pattern19();
        // pattern20();
        // pattern21();
        // pattern22();
        pattern23();

  }
}
```