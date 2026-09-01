# Tutorial Pracitce 
 

# Bitwise Operations 

```
import java.lang.*;

/**
 * operator
 */
public class operator {

    public static void main(String[] args) {
        int x=0b1010,y=0b0110,z;
        z=x&y; // (AND operator)
        System.out.println("z is :" + z);// oputput is 2;
        z= x|y;//(OR operator)
        System.out.println("z is :" + z);// oputput is 14;
        z = x^y; //(XOR operator);
        System.out.println("z is :" + z);// oputput is 12;
        z = ~x; //( NOT operator)
        System.out.println("z is :" + z);// oputput is 2;
        z = ~y;// (NOT of y)

        System.out.println("z is :" + z);// oputput is 2;

    }
}
```
# Swapping Two Numbers using Bitwise operations 
```
// Program to Swapping numbers
public class operator {
    public static void main (String [] args){
        int a=10,b=15;
        System.out.println("Before swapped " + "a = "+a +"  b= "+b);
        a=a^b;
         b = a^b;
         a=a^b;
         System.out.println("After swapped " + "a = "+a +"  b= "+b);
    }
    
}
```

# Merging and Masking  program  using Bitwise operators 
### Merging = combining two separate pieces of binary data into one value.
### Masking = using AND (&) with a bit pattern to select/extract specific bits.

```
public class operator {
    public static void main (String [] args){
        byte a=9,b=12;
        byte c;
        c =(byte)(a<<4);
        c =(byte)(c|b); // merging both a & b in c
       System.out.println((c&0b11110000)>>4); // reading first 4bits of c weather it is equal to 9 or not! That is  extracting 9
       System.out.println((c&0b00001111)); // reading last 4bits of c weather it is equal to 12 or not! Extracting 12
    }
    
}
```