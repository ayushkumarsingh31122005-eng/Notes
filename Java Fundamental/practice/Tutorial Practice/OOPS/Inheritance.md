# Paramiterized constructor..
```
class parent {
  parent(){
    System.out.println("Non-param const.!");
  }
  parent (int x){
    System.out.println("param of the parent :"+x);
  }
}

class child extends  parent{
  child(){
    System.out.println("Non-param child const !");
  }
  child(int y){
    System.out.println("params of the child "+y);
  }
  child (int x, int y){
    super(x);
    System.out.println("2 params of the child : "+y);
   }
}
public  class example2{
  public  static void main(String args []){
    child c = new child(12,21);
  }
}
```
* example 2 of the parametrized constructor...
```
class rectangle{
  int length, breadth;
  rectangle(){
    length = 1;
    breadth = 1;
  }
  rectangle(int l,int b){
    length = l ; 
    breadth = b;
  }
}

class cuboid extends rectangle{
  int height;
  cuboid(){
    height = 1;
  }
  cuboid(int h){
    height = h; 
  }
  cuboid(int l , int b, int h){
    super(l,b);
    height = h;
  }

  public long volume(){
    long volume = length*breadth*height;
    return volume;
  }
}

class example2{
  public static void main(String args[]){
  cuboid c = new cuboid(3,5,4);
  System.out.println("The volume is : "+c.volume());
  }
}
```
