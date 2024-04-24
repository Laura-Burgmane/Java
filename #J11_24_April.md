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


