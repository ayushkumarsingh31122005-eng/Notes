# classrooom Demonstration of "try & catch" 
### 1.
```


public class exception {
  
    public static void main(String[] args) {
      
      int a, b, c; 
      try{

        a =10; 
        b = 0 ; 
        c = a/b;
        System.out.println("Result is :"+c);
      }
      catch(ArithmeticException e){
        System.out.println("Division by zero");
      }
    }
}

```
## One try block culd have more than one catch blocks 
* ex : 
```


public class exception {
  
    public static void main(String[] args) {
      
     int A[] = {12,23,43,54,35,0};
     try{

       int c = A[0]/A[5];
  
       System.out.println("Division is : "+c);
       System.out.println(A[9]);
     }
     catch(ArithmeticException e){
      System.out.println("Denominator should not be 0");
     }
     catch(ArrayIndexOutOfBoundsException e){
      System.out.println("Index is Invalid");
     }
     System.out.println("Bey");
    }
}

```

### used 'exception' class .
```
// package checkedunchecked;

public class exception{

  static void fun1(){
    try{

      System.out.println(10/0);
    }
    catch(Exception e){
     System.out.println(e.getMessage());
    }
  }
  static void fun2(){
    fun1();
  }
  static  void fun3(){
    fun2(); 
  }
  
  public static void main(String args []){
    fun3();
  }
}
```
### checked_&_unchecked class
```
class LowBalanceException extends Exception{
  @Override 
  public  String toString(){
    return "Balance Should not be less than 5000";
  }
}

public class exception{
  
  static void fun1(){
    try{
      throw new LowBalanceException();
    }
    catch(LowBalanceException e){
      System.out.println(e);
    }
  }

  static void fun2(){
     fun1();
  }

  static void fun3(){
    fun2();
  }


  public  static  void main(String args []){
    fun3();
  }
}
```
### User custom Exception class..
```
class NegativeDimensionException extends  Exception{
  @Override 
  public String toString(){
    return  "Dimension of the Rectangle cann't be Negative.";
  }
}
public  class ThrowThrows{
  
static int area (int l , int b) throws NegativeDimensionException{
  if(l<0  || b<0)throw new NegativeDimensionException();
  return l*b;
}
 static  void  meth1() throws NegativeDimensionException{
  System.out.println("Area is : "+area(5,-10 ));
 }
  public static  void main(String args [] ){
    try{

      meth1();
    }
    catch(NegativeDimensionException e){
      System.out.println(e);
    }
  }
}
```
### Built in Exception class
```
public  class ThrowThrows{
  
static int area (int l , int b) throws Exception{
  if(l<0  || b<0)throw new Exception();
  return l*b;
}
 static  void  meth1() throws Exception{
  System.out.println(area(5,-10 ));
 }
  public static  void main(String args [] ){
    try{

      meth1();
    }
    catch(Exception e){
      System.out.println(e);
    }
  }
}
```
### Finally Block :- Either there is error or not finally block the line of code inside the finally block will defnitly be executed...

```
public class FinallyDemo{
  public static void main(String args []){
    try{

      System.out.println(10/0);
    }
    finally{

      System.out.println("Finally Message");
    }
  }
}
```

* IF we do have try and catch both block then we don't need finally block ...
* It means that  if we have handelled exception then last codes will defnitly be printed..

```
public class FinallyDemo{
  public static void main(String args [])throws Exception{
    try{

      System.out.println(10/0);
    }
    catch(ArithmeticException e){
      System.out.println(e);
    }
    finally{

      System.out.println("Finally Message");
    }
  }
}
```
* Finally Block is something , if you don't know while writing code weather the exception has handled or not then it's better to keep most necessarily executing code inside the finally Block.
* ex: 
```
public class FinallyDemo{

  static void meth1() throws Exception{
    try{

      throw new Exception();
    }
    finally{
      System.out.println("Finally Message !");
    }

  }
  public static void main(String args [])throws Exception{
    meth1();
  }
}
```
* EveryThing created in java is in heap..
  Anything outside the program is resourse..


  ```
  class StackOverFlowException extends  Exception{

  public  String toString(){
    return "Stack is Full";
  }
}

class StackUnderFlowException extends  Exception{
  public String toString(){
    return  "Stack is Empty";
  }
}

class Stack{
  private  int size , top= -1;
  private  int S[];
  public Stack(int sz){
    size = sz; 
    S = new int[sz];
    S = new int [sz];
  }
  public  void push(int x) throws StackOverFlowException {
    if(top==size-1)
      throw new StackOverFlowException();
    top++;
    S[top] =x;
  }

  public int pop() throws StackUnderFlowException{
    int x = -1;
    if(top == -1)
      throw new StackUnderFlowException();
    x = S[top];
    top--;
    return x;
  }
}
public class SCException1{
  public  static  void main(String args []){
    Stack st = new Stack(5);
    try{
      st.push(106);
      st.push(182);
      st.push(10);
      st.push(15);
      st.push(159);
      st.push(159);
    }
    catch(StackOverFlowException s){
      System.out.println(s);
    }
  }
}
  ```