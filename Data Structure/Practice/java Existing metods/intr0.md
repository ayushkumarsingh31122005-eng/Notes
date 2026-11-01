# Custom classes and objects 
```
class Data{
  private int num ; 
  private String name ;
  private  InternalData internalData;
  Data(int num , String name,  int revenue){
    this.num = num ; 
    this.name = name; 
    this.internalData = new InternalData(revenue); // 
  }

  // Setter Method 
  public void setNum(int num){
    this.num = num;
  }
  public void setName(String name){
    this.name = name;
  }
  // Getter Methdo
  
  public  int getNum(){
    return  this.num;
  }
  public String getName(){
   return  this.name ; 
  }

  // Inner Custom class 
  class InternalData{
    public  int revenue;

    public InternalData(int revenue){
      this.revenue = revenue;
    }
  }
}

/**
 * Basics
 */
public class Basics {

  public static void main(String[] args) {
    Data dataObject = new Data(5, "Ayush", 100);
    Data dataObject1 = new Data(5, "Ayush", 150);
    Data dataObject2 = new Data(5, "Ayush",105);
    dataObject.setName("Pince");

  }
}
```