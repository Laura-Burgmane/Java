```java
import java.util.Scanner; // import the Scanner class 

class Main {
  public static void main(String[] args) {
    Scanner object = new Scanner(System.in);
    String userName;
    String city;
    String age;
    
    System.out.println("What is your name?"); 
    userName = object.nextLine();   

            
Scanner object1 = new Scanner(System.in);
    System.out.println("Which city are you from?"); 
    city = object1.nextLine();  

    Scanner object2 = new Scanner(System.in);
    System.out.println("How old are you?"); 
    age = object2.nextLine();  


    
    System.out.println("My name is "  + userName + " and I am from city " + city + "." + " My age is " + age);
    
  }
}
```
