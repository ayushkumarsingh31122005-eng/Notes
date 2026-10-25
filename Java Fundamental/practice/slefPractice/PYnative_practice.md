# Exercise 3: Swap without Temp Variable
```
static void  swapNum(){
    Scanner sc = new Scanner(System.in);
    System.out.println("Entner the two Nums");
    int x = sc.nextInt();
    int y = sc.nextInt();
    System.out.println(" you have entered num : "+x+" ,"+y);
    // swaping without third var
    x = x+y; 
    y = x -y;
    x = x-y;
    System.out.println("Nums after swaped : "+x+", "+y);
  }
```
# Exercise 6: Compound Interest Calculator
```
 static  void calculateCompoundIntrest(){
    Scanner sc = new Scanner(System.in);
    System.out.println("enter the principle");
    double p = sc.nextDouble();
    System.out.println("Enter the rate of intrest ");
    float r = sc.nextFloat();
    System.out.println("Enter the Number of times Intrest compounded ");
    int n = sc.nextInt();
    System.out.println("Enter the time ");
     float t = sc.nextFloat();
    double A = p*Math.pow((1+(r/n)), t);
    double CI = A-p;
    System.out.println("Amount is : "+A+"\n Compound Intrest is: "+CI);
  }
```
# Exercise 8: Even or Odd Checker
```
 static void OddEvenChecker(){
  Scanner sc = new Scanner(System.in);
  long n = sc.nextLong();
  if(n%2== 0 ){
    System.out.println("the num is even");
  }else{
    System.out.println("the num is odd");
  }
 }
```
# Exercise 14: Print Numbers Divisible by 3 or 5 Using Continue
```
static void divisibleBy3and5(int n){
  for(int i = 0 ; i<=n; i++){
    if(i%3 !=0 && i%5 !=0){
      continue;
    }
    System.out.print(i+" ");
  }
}
```
# Exercise 15: Print Even Numbers Using a Do-While Loop
```
static void EvenNum(int n){
  int i = 1; 
do{
  if(i%2==0){
    System.out.print(i+" ");
  }
  i++;
} while(i<=n);
    
}

```
# Exercise 16: Multiplication Table
```

static  void table(){
  Scanner sc = new Scanner(System.in);
  System.out.println(" Enter the Number");
  int x = sc.nextInt();
  for(int i = 1; i<=10; i++){
    System.out.println(x+"*"+i+"="+(x*i));
  }
}
```
# Exercise 17: Factorial of a Number
```
static  void Factorial(){
  Scanner sc = new Scanner(System.in);
  System.out.println("Enter the Num");
   int x = sc.nextInt();
  <!-- int x = 4;  -->
  int val=1;
  if(x>0){
    for(int i = 1 ; i<=x; i++){
    
       val = val*i;
    }
  }
  else{
    System.out.println("Invalid input !");
  }
  System.out.println(val);
}

```
# Exercise 18: Fibonacci Series
```
 int n = 8;
        int a = 0, b = 1;
        for (int i = 0; i < n; i++) 
            System.out.print(a + " ");
            int next = a + b;
            a = b;
            b = next;
```
# Exercise 19: Reverse a Number
```
static void reverseNum(long x){
  long revNum=0;
  long y = x;
  while (x>0) {
    int digit= (int)x%10;
    revNum = (revNum*10)+digit;
    x = x/10;
  }
  System.out.println("Reversed Num is :"+revNum);
  if(y == revNum){
    System.out.print("The num is plainDrome");
  }else{
    System.out.print("Not Plain Drome !");
  }
}

```
# Exercise 21: Prime Number Checker
```
  static  void PrimeChecker(int x){
    if(x<=1){
      System.out.println("Not Prime !");
      return ;
    }
    int count = 0 ;
    for(int i = 1;i*i<=x; i++){
      if(x%i == 0 ){
        count++;
        if(x/i !=i){
          count++;
        }
      }
    }
    if(count ==2){
      System.out.println("Prime !");
    }else
      System.out.println("Not Prime !");
  }
```
# Exercise 25: Array Sum and Average
```
static  void sumAndAvergae(int x[]){
  int sum = 0 ;
  double avg = 0 ; 
  for(int i = 0; i<x.length; i++){
    sum = sum+x[i]; 
    avg = sum/x.length;
  }
  System.out.println("The sum of all Numbers of Array is : "+sum+"\n the avg is : "+avg);
}
```
# Exercise 26: Find Min and Max in Array
```
  static  void MinAndMax(int n[]){
    int min = n[0] ; 
    int max =n[0];
    for(int i = 0 ; i<n.length; i++){
      if(n[i]>max){
        max= n[i];
      }
     if(min>n[i]){
      min = n[i];
     }
    }
    System.out.println("The max is: "+max+"\n Min : "+min);
  }

```
# Exercise 27: Reverse an Array
```
  static  void ReverseArray(int n[]){
    int y [] = new int [n.length];
    for(int i = 0,j=y.length-1 ; i<n.length; i++, j--){
      y[j]= n[i];
    }
    for(int num :y){
      System.out.print(num+" ");
    }
  }
```
# Practice Problem: Write a program that sorts an integer array in ascending order
```
static void arrageInAscendingOrder(int n[]){
  for(int i = 0 ; i<n.length;i++){
    for(int j = i+1;j<n.length;j++){
      if(n[i]>n[j]){
        int temp = n[i];
        n[i] = n[j];
        n[j]= temp;
      }
    }
  }
  for(int num : n){
    System.out.print(num+" ");
  }
}
```
# Exercise 29: Find Duplicate Elements
```
static void FindingDuplicate(int arr []){
  int count = 1 ;
 for(int i = 0 ;i<arr.length-1; i++){
  int temp  = arr[i];
  // if(temp == arr[i+1])count++;
  for(int j = i+1 ;j<arr.length; j++){
    if(temp == arr[j])count++;
    else count = count;
  }
 }
 if(count>1)System.out.println("There is Duplicate !");
 else System.out.println("There is not Duplicate");
}
```
# Exercise 30: Merge Two Arrays
```
static  void MergingTwoArray(int arr[], int arr2[]){
  int z [] = new int [arr.length+arr2.length] ;
  for(int  i = 0  ; i<arr.length; i++){
     z[i] = arr[i];
  }
  for(int i = 0 ; i<arr2.length; i++){
    z[arr.length+i] = arr2[i];
  }
for(int num: z){
  System.out.print(num + " ");
}

}
```
# Exercise 31: Matrix Addition
```
static void addMatrix(int arr1[][],int arr2[][]){
  int newArr [][] = new int [3][3];
  for(int i = 0 ; i<3;i++){
    for(int j = 0; j<3; j++){
      newArr [i][j] = ((arr1[i][j]) + (arr2[i][j]));
    }
  }

  for(int i = 0; i<3; i++){
    for(int j = 0 ;j<3; j++){
      System.out.print(newArr[i][j]+ " ");
    }
    System.out.println();
  }
}
```
# Exercise 32: String Length (Manual Count)
```
static void strLength(String str){
  str = str.trim();
  int count = 0 ; 
  char []a = str.toCharArray();
  for(int i = 0 ; i<a.length;i++){
    if(i>=0){
      count++;
    }
  }
  System.out.println("The length of the String is :  "+count);
}
```
# Exercise 33: Palindrome String Checker
```
static void strLength(String str){
  str = str.trim();
  int count = 0 ; 
  String newStr = "";
  char []a = str.toCharArray();
  for(int i = 0 ; i<a.length;i++){
    newStr = newStr+a[a.length-1-i];
  }
  // System.out.println(newStr);
  if(str.equalsIgnoreCase(newStr)){
    System.out.println("the given String is plainDrome !");
  }else{
    System.out.println("the given String is not plainDrome !");
  }
}
```
# Exercise 36: Character Frequency Counter
```
  static void frequencyOfChar(String str){
    char ch;

    char c [] = str.toCharArray();
    boolean visited[] = new boolean[c.length];
    for(int i = 0 ;i<c.length; i++){
      if(visited[i]){
        continue;
      }
      int count = 0 ; 

      ch = c[i];
      for(int j = 0 ; j<c.length; j++){
        if(ch == c[j]){
          count++;
          visited[j] = true;
        }
      }
        System.out.println(ch +" : "+count);
        // count = 0 ; 
    }
```
# Practice Problem: Write a Java program to check whether two given strings are anagrams of each other.
```
 static  void checkAnagrams(String s1, String s2){
  s1.toLowerCase();
  s2.toLowerCase();
  char sOne [] = s1.toCharArray();
  char sTwo [] = s2.toCharArray();
  Arrays.sort(sOne);
  Arrays.sort(sTwo);

  if(Arrays.equals(sOne, sTwo)){
    System.out.println("The str is Anagram : !");
  } else{
    System.out.println("The given str is not anagram !");
  }
 }
  
```
