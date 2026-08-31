## 1. What is a 2-D Array? 
Imagine a standard 1-D array as a single row of lockers side-by-side. 
A **2-D array** is like a whole wall of lockers. It has **rows** and **columns**. 
Think of it like an Excel spreadsheet, a chessboard, or a movie theater seating chart.

In Java, a 2-D array is actually an **"array of arrays"**. This means the main array holds other arrays inside it!

### 🖼️ Visualizing a 2-D Array
Let's imagine a 2-D array with **3 rows** and **4 columns**:

```text
             Col 0    Col 1    Col 2    Col 3
           +--------+--------+--------+--------+
  Row 0    |  [0][0]|  [0][1]|  [0][2]|  [0][3]|
           +--------+--------+--------+--------+
  Row 1    |  [1][0]|  [1][1]|  [1][2]|  [1][3]|
           +--------+--------+--------+--------+
  Row 2    |  [2][0]|  [2][1]|  [2][2]|  [2][3]|
           +--------+--------+--------+--------+
```
*Notice how counting starts at `0`. This is super important in Java! The first row is Row 0, and the first column is Column 0.*

---

## 2. Syntax: How to Create a 2-D Array

There are three main steps when creating an array: **Declaration**, **Creation**, and **Initialization**.

### Method 1: The Step-by-Step Way (When you don't know the exact data yet)
```java
// 1. Declare the array (saying it exists)
int[][] myGrid; 

// 2. Create the array (telling Java the size: 3 rows, 4 columns)
myGrid = new int[3][4]; 

// 3. Put a value inside a specific box (e.g., row 1, col 2)
myGrid[1][2] = 50; 
```

### Method 2: The Shortcut (When you already know the data)
You can create and fill the array all at once using curly braces `{}`.

```java
int[][] numbers = {
    {1, 2, 3, 4},   // Row 0
    {5, 6, 7, 8},   // Row 1
    {9, 10, 11, 12} // Row 2
};
```

---

## 3. How to Access and Change Data

To get or change a value, you need the exact "address", which is the `[row][column]`.

```java
int val = numbers[0][1]; // Gets the value at Row 0, Col 1 (which is 2)

numbers[2][3] = 99; // Changes the value at Row 2, Col 3 (from 12 to 99)
```

---

## 4. Reading the Whole Array (Using Loops)

To visit every single box in our 2-D array, we use **Nested Loops** (a loop inside another loop).
*   The **outer loop** goes through the rows.
*   The **inner loop** goes through the columns of each row.

### 💻 Example Code: Printing a 2-D Array
```java
public class ArrayExample {
    public static void main(String[] args) {
        
        // Create our 2-D array
        int[][] matrix = {
            {10, 20, 30},
            {40, 50, 60}
        };
        
        // Outer loop for Rows (matrix.length gives the number of rows)
        for (int row = 0; row < matrix.length; row++) {
            
            // Inner loop for Columns (matrix[row].length gives columns in that row)
            for (int col = 0; col < matrix[row].length; col++) {
                System.out.print(matrix[row][col] + " "); // Print value and a space
            }
            
            System.out.println(); // Move to the next line after finishing a row
        }
    }
}
```
**Output of the code:**
```text
10 20 30 
40 50 60 
```

---

## 5. Related Concept: "Jagged Arrays" (Staircase Arrays)

Remember I said a 2-D array in Java is an "array of arrays"? Because of this, the rows do **not** have to be the same length! 
This is called a **Jagged Array** (or Ragged Array).

### 🖼️ Visualizing a Jagged Array:
```text
Row 0: [ ][ ][ ]       (Length 3)
Row 1: [ ][ ]          (Length 2)
Row 2: [ ][ ][ ][ ][ ] (Length 5)
```

### How to code it:
```java
int[][] jagged = new int[3][]; // We only specify the 3 rows right now

jagged[0] = new int[3]; // Row 0 gets 3 columns
jagged[1] = new int[2]; // Row 1 gets 2 columns
jagged[2] = new int[5]; // Row 2 gets 5 columns
```
Jagged arrays are a fantastic tool for saving memory when you have uneven amounts of data (like varying days in a month or uneven lists of students in different classes)!

---

### 🎯 Summary
* **2-D Array:** A grid with rows and columns.
* **Syntax:** `dataType[][] arrayName = new dataType[rows][cols];`
* **Accessing Elements:** Use `arrayName[row][col]` to read or write data.
* **Looping:** Use a nested `for` loop to read everything.
* **Pro Tip:** Rows can have different lengths! This is called a Jagged Array.

### Practice Session
#### Q1. Adding 2-D Matrix
```
/**
 * operator
 */
public class operator {

                public static void main(String [] args){
                        int A[][]= {
                                {1,2,4,3},
                                { 8,5,6,7},
                                {9,8,5,3}
                        };
                        int B [][] = {
                                {1,2,3,4},
                                {4,5,6,7},
                                {1,2,9,7}
                        };
                        int C[][] = new int [3][4];
                        for(int i = 0 ; i<=A.length-1;i++){
                                for(int j =0; j<=A[i].length-1; j++){
                                         
                                        C[i][j] = A[i][j]+B[i][j];
                                }
                        }
                
                for(int i = 0; i<=C.length-1; i++){
                        for(int j = 0 ; j<= C[i].length-1; j++){
                                System.out.print(C[i][j]+"   ");
                        }
                        System.out.println("\n");

                }
                }
}
```
### Multiplication of Matrix using 2-D Matrix
```
/**
 * operator
 */
public class operator {

                public static void main(String [] args){
                        int A[][]= {
                                {1,2,4},
                                { 8,5,6},
                                {9,8,5}
                        };
                        int B [][] = {
                                {1,0,0},
                                {0,1,0},
                                {0,0,1}
                        };
                        int C[][] = new int [3][3];
                        for(int i = 0 ; i<=A.length-1;i++){
                                for(int j =0; j<=A[i].length-1; j++){
                                         C[i][j]=0;
                                     for(int k = 0; k<3;k++){
                                        C[i][j] = C[i][j]+ A[i][k]*B[k][j];
                                     }
                                }
                        }
                
                for(int i = 0; i<=C.length-1; i++){
                        for(int j = 0 ; j<= C[i].length-1; j++){
                                System.out.print(C[i][j]+" ");
                        }
                        System.out.println("\n");

                }
                }
}
```
### Sorting an array using in built java packege 
```
/**
 * operator
 */
public class operator {

                public static void main(String [] args ){
                        String [] arr = {
                                "java","python","pascal","smalltalk","ada","basic"
                        };
                        java.util.Arrays.sort(arr); // java package to sort avilable for sorting.
                        for(String x: arr){
                                System.out.print(x+ " ");
                        }
                }
}
```