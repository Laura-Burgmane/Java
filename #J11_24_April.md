# Java

## last weeks homework review:

```java
public class Main {
  public static void main(String[] args) {
    
//Fill the party list with people you would like to invite to the party.
    
    String[] people = {"Oskars", "Anna", "Andris", "Kristine", "Zane", "Raivo"}; 
    boolean isIntheList = false;
    
// Check whether or not "Anna" is in the array.
    
    for (int i = 0; i < people.length; i++){
       if (people[i] == "Anna") {
         isIntheList = false; 
       break;
      } 
      if(isIntheList){ 
      System.out.println("Anna is not in the party list");
      }else{
          System.out.println("Anna is in the party list!");
        }
    }
      // Check whether or not "Maris" is in the array.
      for (int i = 0; i < people.length; i++){
        
         if (people[i] == "Maris"){
           isIntheList = true; 
        } 
      }
        if(isIntheList){
        System.out.println("Maris is in the party list!");
        }else{
            System.out.println("Maris is not in the party list!");
          }
        
  }
}
```

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    
    String[] partyList = {"Oskars", "Maris", "Andrea"};

    Scanner scanner = new Scanner(System.in);
    String name = scanner.nextLine();
    
    boolean isInvited = false;
    
    for (int i = 0; i < partyList.length; i++){
      if(partyList[i].equals(name)){
        isInvited = true;
        System.out.println(name + " is invited");
        break;
      }
    }

    if(!isInvited){
      System.out.println(name + " is not invited");
    }
  }
}
```

## Methods

```java
public class Main {

  
  public static void main(String[] args) {
    printOutABorder();
    
    System.out.println("Hello world!");
    
    printOutABorder();
  }

  public static void printOutABorder() {
    //Function starts here
    
    System.out.println("=====================");

    //Function ends here
  }
}
```

```java
public class Main {
  
  public static void main(String[] args) {
    printOutABorder();
    
    System.out.println("Hello world!");
    int number = getARandomNumber();
    System.out.println(number);
    printOutABorder();
  }


  public static void printOutABorder() {
    //Function starts here
    System.out.println("=====================");
    //Function ends here
  }

  public static int getARandomNumber() {
    //Function starts here
    return 5;
    //Function ends here
  }
}

// void == Returns nothing; This is just an action
```
For anyone who also struggles with understanding what "returning a value" means: 

In the context of methods in Java, "returning a value" means providing a result back to the part of the program that called the method.

Printing something to the console using the System.out.println() method in Java is not the same as returning a value.
Printing to the console is a way to display information to the user or to help with debugging, but it does not provide a result back to the part of the program that called the method. Instead, it outputs the information directly to the console for human viewing.

On the other hand, returning a value from a method means providing a result back to the calling part of the program so that it can use that result in its calculations or operations.

//Access modifiers:
//public
//private
//protected

//Whether or not the function is static:
//static
//

//Return type:
//void
//int
//String
//int[]
//boolean
//... ...

## 2 equivalent codes:

```java
public class Main {
  
  public static void main(String[] args) {
    int number1 = 5;
    int number2 = 7;
    int result = sum(number1, number2);
    System.out.println(result);
  }


  public static int sum (int number1, int number2) {
    return number1 + number2;
  }
}
```
## and:

```java
public class Main {
  
  public static void main(String[] args) {
    int number1 = 5;
    int number2 = 7;
    int result = number1 + number2;
    System.out.println(result);
  }
}
```
## smth very confusing:

```java
/*
  Write a name and check whether or not it is atleast 3 char long
   Write a surname and check whether or not it is atleast 3 char long
If it's not, then say. Sorry, your name is too short.
If both of them are valid, say. Thank you, your information has been registered!
*/

public class Main{
  public static void main(String[] args){

    String name = "Oskars";
    String surname = "Klaumanis";
    boolean isUserNameValid = isNameValid(name);
    boolean isUserSurnameValid = isNameValid(surname);

    if(isUserNameValid && isUserSurnameValid){
      System.out.println("Thank you, your information has been registered!")
    } else {
      System.out.println("Sorry, your check your information");
    }
    
  }

  public static boolean isNameValid(String name){
    if(name.length() < 3){
      System.out.println("Sorry, your name is too short.");
      return false;
    }

    return true;
  }
}
```
