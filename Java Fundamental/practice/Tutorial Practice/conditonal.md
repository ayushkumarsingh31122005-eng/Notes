# if else-if else conditionals
### Q. Find a number is odd or even 

```
import java.lang.*;
import java.util.*;

public class relational {
    public static void main (String [] args){
      int num;
      Scanner sc = new Scanner(System.in);
      num =sc.nextInt();
      if(num%2==0){
        System.out.println("Your given Number is Even");
      }else{
        System.out.println("YOur given Number is Odd. !");
      }
    }
  
}
```
### Q. Find Person is Adult or not!

```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

     public static void main(String[] args){
       Scanner  sc = new Scanner(System.in);
       System.out.println("Kindly Enter Your age !");
       int age = sc.nextInt();
       if(age>18){
        System.out.println("You are Adult !");
       }else{
        System.out.println("You are not Adult !");
       }
     }
}
```
### Q Finding the radix of  the given Number .
```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

  
     public static void main(String[] args){
      String num ;
      Scanner sc = new Scanner(System.in);
      num = sc.next();

      if(num.matches("[01]+")){
          System.out.println("You have Entered Binary Number and the Radix is :"+"2");
      }else if(num.matches("[0-7]+")){
        System.out.println("The ENtered Number is Octal and the radix is 8");
      }else if(num.matches("[0-9]+")){
        System.out.println("The Entered Number is  Octal and the radix is : 10");
      }else if(num.matches("[0-9A-Fa-f]+")){
        System.out.println("The given Number is Hexa-Decimal and the radix is : 16");
      }
     }
}
```
### Q. Finding the grade of student 

```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

     public static void main(String[] args){
      int [] m = new int [4];
      Scanner sc = new Scanner(System.in);
      for(int i= 1; i<=3; i++){
        System.out.println("Enter the marks of subject m"+i);
        m[i] = sc.nextInt();
      }
      

      int avg = (m[1]+m[3]+m[3])/3;
      if(avg>=70){
        System.out.println("The grade of the Student is :" + "A and avg marks is :" +avg);
      }else if ( avg>=60 && avg<70){
        System.out.println("The grade is : B and marks is "+avg);
      }else if(avg>= 50 && avg < 60){
        System.out.println("The garde is : C and the marks is "+avg);
      }else if(avg>=40 && avg <40){
        System.out.println("the grade is : D and the marks is "+ avg);
      }else{
        System.out.println("The candidate has Failed !");
      }
     }
}
```

 ### Q. Find that the given yaer is leapyear or not!

 ```

import java.lang.*;
import java.time.Year;
import java.util.*;

/**
 * relational
 */
public class relational {

  public static void main(String[] args){
      long year;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter Year !");
      year = sc.nextLong();

        if(year % 4== 0){
              if (year%100 ==0) {
                if (year%400 ==0) {
                  System.out.print("Leap Year");
                }else{
                  System.out.println("NOt leap Year");
                }
                                  
              }else {
                System.out.println("Leap Year");
              }
        }else {
          System.out.println("Not Leap Year");
        }
       
  }
}
 ```
 ###  Q. Finding Day  based on Number 

 ```
 import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

    public static void main(String[] args) {
      Scanner sc = new Scanner(System.in);
    int []  dayNo = {1,2,3,4,5,6,7};
    String [] days = {
      "Monday",
      "Tuesda",
      "Wednesday",
      "Thursday",
      "Friday",
      "Saurday",
      "Sunday"
    };
    System.out.println("Enter DayNumber !");
    int input = sc.nextInt();
    for(int i = 0; i<dayNo.length; i++){
      if(dayNo[i]==input){
        System.out.println("Day is :" +days[i]);
        break;
      }
    }

    }   
}
 ```

### Q. Finding protocall and type of website..
```
/**
 * relational
 */
public class relational {

  public static void main(String[] args) {
    String web = "https:\\www.google.com";
    int index = web.indexOf(":");
    String protocall = web.substring(0, index);
    int index2 = web.lastIndexOf(("."));
    String domain = web.substring(index2);
    System.out.println(domain);
    System.out.println(protocall);
    if(protocall.equals("https")){
      System.out.println("Hypertext protocall");
    }else{
      System.out.println("Some other Protocall");
    }
    if(domain.equals(".com")){
      System.out.println("commercial web");
    }else{
      System.out.println("Some other type of website");
    }
  }

}
```
# Switching Conditional.
### Q. Display name of a day based on number using Switch.

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
     System.out.println("Enter DayNo.");
     n= sc.nextInt();

     switch (n) {
      case 1:
        System.out.println("Monday!");
        break;
      case 2:
        System.out.println("Tuesday");
        break;
      case 3:
        System.out.println("Wedmesday");
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
        System.out.println("Invalid Input");
        break;
     }
   }
}
```
### Q. Display website Name using Switch.
```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

     public static void main(String[] args){
      String websiteName;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the WebSite Name !");

       websiteName = sc.next();
      int indexof = websiteName.lastIndexOf(".");
      String extenssion = websiteName.substring(indexof+1);

      switch(extenssion){
        case "com":
          System.out.println("Commercial website");
          break;
        case "org":
          System.out.println("Orginational website");
          break;
        case "net":
          System.out.println("Network website");
          break;
        case "gov":
          System.out.println("government wesite");
          break;
        default :
        System.out.println("Wrong input");
        break;          
      }
     }
}
```
### Q. Menu Driven Program.
```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

    public static void main(String[] args){
      System.out.println("MENU");
      System.out.println("=====");
      System.out.println("ADD");
      System.out.println("SUB");
      System.out.println("MUL");
      System.out.println("DIV");

      System.out.println("Enter two Numbers");
      int num1, num2;
      String menu;
      Scanner sc = new Scanner(System.in);
      num1 = sc.nextInt();
      num2 = sc.nextInt();
      sc.nextLine(); //this is because  if won't be then there would be buffer issue  and it allows to another data type input.
      System.out.println("Enter Operation You want to Perform !");
      menu = sc.nextLine();

      switch(menu){
        case "ADD":
          System.out.println("Addetion of  Numbers is :"+ (num1+num2));
          break;
        case "SUB":
          System.out.println("Subtraction of  Numbers is :"+ (num1-num2));
          break;
       case "MUL":
            System.out.println("Multiplication  of  Numbers is :"+ (num1*num2));
            break;
        case "DIV":
            System.out.println("Division of Numbers is :"+ (num1/num2));
             break;
        default :
        System.out.println("Wrong Input !");
      }

    }
}
    

```