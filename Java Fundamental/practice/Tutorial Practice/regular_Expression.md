
### Playing with * System.out.printf() * method

#### using format specifiers 
```
public class operator {

    public static void main(String[] args){
      String name = "Spongebob";
      char firstLetter = 'S';
      int age = 30;
      double height =60.5;
      boolean isEmployed = true;

        System.out.printf("Hello %s\n",name);
        System.out.printf("Your name starts with %c\n",firstLetter);
        System.out.printf("Your name age is   %d\n",age);
        System.out.printf("Your height is  %f inches tall\n", height);
        System.out.printf("You are Employed:  %b\n",isEmployed);

        // adding multiple variable in a single line..
        System.out.printf("%s your name start with %c , you are %d years old , your heigh is %f and your Employed : %b",name,firstLetter,age,height,isEmployed);
    }
}
```
### Various Way to create Strings
```
public class operator {

    public static void main(String[] args){
        String name = "Ayush";
        String name2 = new String("Prince");
        char c[]={'H','e','l','l','o'};
        byte string1[] ={70,71,72,73,75};

        String greet = new String(c); // str creating using char
        String BytStr = new String(string1); // str creating using byte
        System.out.println(name);
        System.out.println(name2);
        System.out.println(greet);
        System.out.println(BytStr);
    }
}
```
### Applying some methods of string 
```
public class operator {

    public static void main(String[] args){
     String str = new String("NOTEBEANS");
      int len= str.length();
      String lowerercase = str.toLowerCase();
            System.out.println(len);
            System.out.println(lowerercase);
        String str2 = str.substring(1, 4);
            System.out.println(str2);
        String  str3 = str.replace('E', 'M');
            System.out.println(str3);
    }
}
```
* ### Q. given  a string = "programmer@gmail.com" ; Now check out the domain name (or does it conain 'gmail'), and extract domain name and then holder name 
```

public class operator {

    public static void main(String[] args){
       String str = "programmer@gmail.com";
    //    System.out.println(str.contains("gmail"));
       int indexOf =str.indexOf("@"); 
       String UserName = str.substring(0,indexOf);
       System.out.printf("The useName  is : %s \n" , UserName);
       String holderName = str.substring(indexOf+1);
       System.out.printf("The holderName is : %s \n", holderName);
       int indexOf2 =  holderName.indexOf(("."));
       System.out.println("Domain name is  : "+ holderName.substring(0, indexOf2));
    }
    
}
```
### Q. Find  if a Number is Binary or not ?

```
import java.lang.*;
import java.util.*;
public class operator {

   static String str ;
        public static void main (String [] args){

             Scanner sc = new Scanner(System.in);
             System.out.println("Enter your Number");
             str = sc.next();
             System.out.println("The given number is binary  : " + str.matches("[01]+"));
             
        }
}
```

####  Q. Find the number is Hexa-Decimal or not?

```

import java.lang.*;
import java.util.*;

/**
 * operator
 */
public class operator {

        public static void main(String[] args){
            long hexaNumber = 0x34235ABC;
            

            String str ="0x" + Long.toHexString(hexaNumber); // way to convert hexa-decimal into string and keeping "0x" as a constant.
            System.out.println("the given number is HexaDecimal  :" + str.matches("0[xX][0-9A-Fa-f]+"));
                                                                                      | |     |
                                                                                      | |     |
                                                                                      | |     |
                                                                                      | |     |
                                                                                      | |     |
                                                                                      | |     |_______ one or more hexadecimal digits.
                                                                                      | |     
                                                                                      | |_____// x  or x
                                                                                      |________ // literal 0
        }
}

```

### Q. Find  is the Data  in Date Format (dd/mm/yyyy);
```

import java.lang.*;

/**
 * operator
 */
public class operator {

        public static void main(String[] args) {
            String data =  "12/3/2024";

            System.out.println("The given data is in the form of Date : "+ 
                data.matches("[0-3][0-9]/[01][0-2]/[0-9]{4}")
            );
        }
}
```

### Q. Remove Special Character from String.
```

import java.lang.*;
import java.util.*;

/**
 * operator
 */
public class operator {
   static String str  ;
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter String ..");
        str = sc.next(); 
            String newStr = str.replaceAll("[^a-zA-Z0-9]","");
            System.out.println(newStr);
    }
}
          

```
### Q Remove extra space from stirng....
```

import java.lang.*;
import java.util.*;

/**
 * operator
 */
public class operator {

    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter String here");
        String str = sc.nextLine();

        String str2 = str.replaceAll("\\s+"," ");
        System.out.printf("Your new String is  :  %s" , str2);


    }
}

```

###  Q. Find out the number of words in the String ....
```

/**
 * operator
 */
public class operator {

    public static void main(String[] args){

        String str = "         Abc            def         gh        ijk";
        str = str.replaceAll("\\s+"," ").trim();
        String wrods[] = str.split("\\s");
        System.out.println("the length of Words in the array is : "+ wrods.length);
    }
}
```