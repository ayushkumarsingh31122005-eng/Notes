# How Array of Object Created !
```
import java.util.*;

class subject{
  private String subID;
  private String name ;
  private int maxMarks;
  private int marksObtained;

  // constructor  for the above properties..

  public subject(String subid, String  nme, int marksObtain, int maxMark){
    subID = subid ;
    name = nme;
    marksObtained =  marksObtain;
    maxMarks = maxMark;
  }
  public subject(String subId, String nam){
    subID = subId;
    name = nam;
  }
  // Getter method for the properties...
  public String  getSubId(){
    return subID;
  }
  public String getName(){
    return name;
  }
  public int  getMaxMarks(){
    return  maxMarks;
  }
  public int getMarksObtained(){
    return marksObtained;
  }
  // Setter Method for the properties...
  public void setSubId(String subid){
    if(subid.length()>0){
      subID = subid;
    }else{
      subID = subID;
    }
  }
  public void setName(String nme){
    if(nme.length()>0){
      name = nme;
    }else{
      name = name ;
    }
  }
  public void setMarksObtained(int marksObtain){
    if(marksObtain>0){
      marksObtained = marksObtain;
    }else{
      marksObtained = 0 ;
    }
  }
  public void setMaxMarks(int maxMark){
    if(maxMark !=0 ){
      maxMarks = maxMark;
    }
  }
  boolean isQualified(){
    return marksObtained>= maxMarks/10*4;
  }
  public String toString(){
    return "\n Subject id :" +subID +"\n Name : "+ name + "\n Marks obtained : "+marksObtained;
  }
}

/**
 * selfPractice
 */
public class selfPractice {

    public static void main(String args []){

     subject subs [] = new subject[4];
     subs[0] =  new subject("S-101", "DSA", 80,100);
     subs[1] = new subject("S-102", "Algorithm", 70,100);
     subs[2] = new subject("S-103", "COA", 60,100);
     for(subject s: subs ){
      System.out.println(s);
     }
    }
}
```
## Student Class 
```
class Student{
  private  String rollNo;
  private  String name;
  private  String departmentName;
  private  String subject; 

  // constructors 
  public Student(String rollNo , String name, String departmentName, String subject){
    this.rollNo = rollNo;
    this.name = name; 
    this.departmentName = departmentName ; 
    this.subject = subject;
  }
  // getter Method ..
  String getrollNo(){
    return  rollNo;
  }
  String getname(){
    return name;
  }
  String getDepartmentName(){
    return departmentName;
  }
  String getSubject(){
    return  subject;
  }
  // setMethods ..
  void setRollno(String rollNo){
    this.rollNo = rollNo;
  }
  void setName(String name){
    this.name = name; 
  }
  void setDepartmentName(String departmentName){
    this.departmentName = departmentName;
  }
  void setSubjetc(String subject){
    this.subject = subject ; 
  }
  // to string method 
  public  String toString(){
    return "\n roll No :"+ rollNo+ "\n Name : "+name + "\n Department Name : "+ departmentName + "\n subject : "+subject;
  }
}

/**
 * selfPractice
 */
public class selfPractice {

  public static void main(String args []){
    Student stud [] = new Student[4];
    stud[0] = new Student("1033dfas", "Ayush", "cs", "Dsa");
    stud[1] = new Student("1033dfas", "Ayush", "cs", "Dsa");
    stud[2] = new Student("1033dfas", "Ayush", "cs", "Dsa");

    for(Student s: stud){
      System.out.println(s);
    }
  }
}
```