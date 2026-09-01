# Playing with Array
### * Finding the sum of all elements.
```
/**
 * relational
 */
public class relational {

    public static void main(String args []){
      int arr[] = {3,9,7,8,12,6,15,5,4,10};
      int sum = 0;
      for(int i = 0; i<arr.length; i++){
        sum = sum + arr[i];

      }
      System.out.println("Sum of all element of  the array is :" + sum);
    }
}
```
### Finding the Maximum Element in the array.
```
/**
 * relational
 */
public class relational {

    public static void main(String args []){
      int arr[] = {3,9,7,8,12,6,15,5,4,10};
      int max = 0;
      for(int i = 0; i<arr.length; i++){
        if(max > arr[i]){
           max = max;
        }else{
          max = arr[i];
        }

      }
      System.out.println("Maximum element  of all element of  the array is :" + max);
    }
}
```
### Finding the second largest element in array 
```
/**
 * relational
 */
import java.lang.*;

public class relational {

    public static void main(String args []){
      int arr[] = {3,9,7,8,12,6,15,5,4,10};
      int max = 0;
      for(int i = 0; i<arr.length; i++){
        if(max > arr[i]){
           max = max;
        }else{
          max = arr[i];
        }

      }
      int secondMaximum = 0;
      for(int i = 0; i<arr.length ; i++){
        if (secondMaximum < arr[i] && arr[i] < max) {
          secondMaximum = arr[i];
        }else  {
          secondMaximum = secondMaximum;
          
        }
      }
      System.out.println(" Largest element  of all element of  the array is :" + max);
      System.out.println("Second Largest element  of all element of  the array is :" + secondMaximum);
    }
}
```
#### Another way 
```

import java.lang.*;

public class relational {

    public static void main(String args []){
      int arr[] = {3,9,7,8,12,6,15,5,4,10};
      int max1 , max2 ;
      max1 = max2 =  arr[0];
      for(int i = 0; i<arr.length; i++){
        if(arr[i]>max1){
          max2 = max1;
          max1 = arr[i];
        }else if(arr[i]>max2){
          max2 = arr[i];
        }
      }
      System.out.println("Second Larges element is "+ max2);
    }
}
```
### searching key in the array 
```
/**
 * relational
 */
import java.lang.*;
import java.util.*;

public class relational {

    public static void main(String args []){
      int arr[] = {3,9,7,8,12,6,15,5,4,10};
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the Key that you want to search !");
      int key = sc.nextInt();
      for(int i = 0 ; i<arr.length; i++){
        if(arr[i] == key){
          System.out.println("The key is found and it's index is :" + i + " and the value is "+ arr[i]);
          System.exit(0);
        }
      }
      System.out.println("Key does not found !");
    }
}
```
### Rotation of array. 
#### left- rotation.
```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

     public static void main(String [] args){
      int arr[] = {1,2,3,4,5};
     //Printing original array.
     for(int x: arr){
      System.out.print(x+", ");
     }

     System.out.println();

     //Store first element 
     int temp = arr[0];

     //Shift elements to the left
     for(int i = 1; i<arr.length; i++){
      arr[i-1]= arr[i];
     }
     // put first element at the last
     arr[arr.length-1] = temp;

     // print rotated array

     for(int x : arr){
      System.out.print(x+", ");
     }

     }
}
```
#### Right Rotation.
```
import java.lang.*;
import java.util.*;

/**
 * relational
 */
public class relational {

     public static void main(String [] args){
      int arr[] = {1,2,3,4,5};
     //Printing original array.
     for(int x: arr){
      System.out.print(x+", ");
     }

     System.out.println();

     //Store first element 
     int temp = arr[arr.length-1];

     //Shift elements to the left
     for(int i = arr.length-1; i>0; i--){
      arr[i] = arr[i-1] ;
     }
     // put first element at the last
     arr[0] = temp;

     // print rotated array

     for(int x : arr){
      System.out.print(x+", ");
     }

     }
}
```
### Insertion of Element
```
// Inserting an Element

/**
 * relational
 */
public class relational {

    public static void main(String [] args){
      int arr[] = new int[10];
      arr[0]=1;
      arr[1]=4;
      arr[2]=8;
      arr[3]=7;
      arr[4]=2;
      arr[5]=3;
      arr[6]=6;
      arr[7]=9;
      int key = 87;
      int index = 2;
      //Printing original arry
     for(int i = 0; i<arr.length; i++){
      System.out.print(arr[i]+", ");
      System.out.print("");
     }
      // making the index empty  in the array
      for(int i = 8; i> index; i--){
        arr[i] = arr[i-1];
      }
      // assigning the key to the index
      arr[index] = key;

      System.out.println();
      //Printing the modified array.
      for(int i = 0; i<9;i++){
        System.out.print(arr[i]+", ");
      }

    }
}
```
### Deletion of an element from array
```
// Inserting an Element

/**
 * relational
 */
public class relational {

    public static void main(String [] args){
      int arr[] = new int[8];
      arr[0]=1;
      arr[1]=4;
      arr[2]=8;
      arr[3]=7;
      arr[4]=2;
      arr[5]=3;
      arr[6]=6;
      arr[7]=9;
      int index = 2; 
      int size = arr.length;
      for(int i =0; i<size; i++){
        System.out.print(arr[i]+", ");
        // System.out.println("");
      }
      // left shift 
      for(int i =index; i<size-1; i++){
        arr[i] = arr[i+1];
      }
      size--;
      System.out.println("");
      //printing new array
      for(int i = 0;i<size;i++){
        System.out.print(arr[i]+", ");
      }
      
    }
}
```

### Copying an Array 
* Solution 
```
/**
 * operator
 */
public class operator {

         public static void main (String [] args){
            int [] arr = {8,9,10,9,2,15,7,13,14,11};
            int [] arr2 =new int [10];
            
            for(int i = 0; i<=arr.length-1; i++){
              arr2[i] = arr[i] ;
                
                System.out.print(arr2[i] +" ,");
            }
            //  for(int i = 0 ; i<arr2.length-1;i++){
            //  }
         }
}
```
### Reverse copying an Array 
* Soultion 
```
/**
 * operator
 */
public class operator {

         public static void main (String [] args){
            int [] arr = {8,9,10,9,2,15,7,13,14,11};
            int [] arr2 =new int [10];
            
            for(int i = arr.length-1,j =0; i>= 0 ; i-- , j++){
                System.out.print(arr[i]+", ");
                arr2[j] = arr[i];

                
            }
            System.out.println();
            System.out.println("New arr ");
            for(int i = 0; i<=arr2.length-1; i++){
                System.out.print(arr2[i]+", ");
            }
           
            
         }
}
```
### Increasing the Size of Array 
```
// Increasing size of Array 

/**
 * operator
 */
public class operator {

        public static void main(String [] args){
            int A[] = {1,2,3,4,5};
            System.out.println("Length of array A =" + A.length);
            int B[] = new int[2*A.length];
             for(int i =0; i<= A.length-1; i++){
                B[i] = A[i];
             }
             A=B;
             B = null;
             System.out.println("Lenth newly incresed Array " + A.length);
        }
}
```