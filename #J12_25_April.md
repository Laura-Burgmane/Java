# Java
## Methods ||

- Reference vs primary type
- __Team work:__ Various tasks to strengthen knowledge about reference vs primary type

## yesterday's team work:
```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    //Creating scanner
    Scanner scanner = new Scanner(System.in);

    //Calling method for getting title
    String title = getTitle();

    //Calling method to get description
    String description = getDescription();

    //Calling method to get printout with lines
    getPrintout(title, description);

    //Closing scanner
    scanner.close();
  }

  // Method to ask user for title
  public static String getTitle() {

    Scanner scanner = new Scanner(System.in);
    // Ask for title
    System.out.print("Enter a title: ");

    //Read title
    String title = scanner.nextLine();

    //Return title
    return title;
  }

  // Method to ask user for description
  public static String getDescription() {

    Scanner scanner = new Scanner(System.in);
    // Ask for descript
    System.out.print("Enter a description: ");

    //Read descript
    String description = scanner.nextLine();

    //Return descript
    return description;
  }

    // Method to display the result with the title wrapped in = characters + description

  public static void getPrintout(String title, String description) {

    // Calc length
    int length = title.length();
    // Create top border
    for (int i = 0; i < (length); i++) {
      System.out.print("=");
    }
    System.out.println("");
    // Display the title
    System.out.print(title);

    System.out.println("");
    // Create bottom border
    for (int i = 0; i < (length); i++) {
      System.out.print("=");
    }
    System.out.println("");

    // Display the description
    System.out.println("");
    System.out.println(description);

  }
}
```

```java
    System.out.print("Enter a title: ");
    String title = getText();

    System.out.print("Enter a description: ");
    String description = getText();
```

```java
import java.util.Scanner;

/*
  Ask user for a title - inputText()
  Ask user for a description - inputText()


  PrintInformation()
    Figure out the size of title
    Print out a border of the size of the title -> printBorder()
    Print out the title
    Print out a border of the size of the title -> printBorder()
    Print out the description
*/


public class Main {
  public static void main(String[] args) {

    //Creating scanner
    Scanner scanner = new Scanner(System.in);

    //Calling method for getting title
    System.out.print("Enter a title: ");
    String title = getText();

    System.out.print("Enter a description: ");
    String description = getText();

    //Calling method to get printout with lines
    getPrintout(title, description);

    //Closing scanner
    scanner.close();
  }

  // Method to ask user for description
  public static String getText() {
    Scanner scanner = new Scanner(System.in);

    //Read user input
    String text = scanner.nextLine();

    //Return user input
    return text;
  }

    // Method to display the result with the title wrapped in = characters + description

  public static void getPrintout(String title, String description) {

    // Calc length
    int length = title.length();
    // Create top border
    for (int i = 0; i < (length); i++) {
      System.out.print("=");
    }
    System.out.println("");
    // Display the title
    System.out.print(title);

    System.out.println("");
    // Create bottom border
    for (int i = 0; i < (length); i++) {
      System.out.print("=");
    }
    System.out.println("");

    // Display the description
    System.out.println("");
    System.out.println(description);

  }
}

```java
import java.util.Scanner;

/*
  Ask user for a title - inputText()
  Ask user for a description - inputText()


  PrintInformation()
    Figure out the size of title
    Print out a border of the size of the title -> printBorder()
    Print out the title
    Print out a border of the size of the title -> printBorder()
    Print out the description
*/


public class Main {
  public static void main(String[] args) {

    //Creating scanner
    Scanner scanner = new Scanner(System.in);

    //Calling method for getting title
    System.out.print("Enter a title: ");
    String title = getText();

    System.out.print("Enter a description: ");
    String description = getText();

    //Calling method to get printout with lines
    getPrintout(title, description);

    //Closing scanner
    scanner.close();
  }

  // Method to ask user for description
  public static String getText() {
    Scanner scanner = new Scanner(System.in);

    //Read user input
    String text = scanner.nextLine();

    //Return user input
    return text;
  }

    // Method to display the result with the title wrapped in = characters + description
/*    

    Figure out the size of title
    Print out a border of the size of the title -> printBorder()
    Print out the title
    Print out a border of the size of the title -> printBorder()
    Print out the description*/
  public static void getPrintout(String title, String description) {

    // Calc length
    int length = title.length();
    // Create top border
    printBorder(length);
    // Display the title
    System.out.print(title);

    System.out.println("");
    // Create bottom border
    printBorder(length);

    // Display the description
    System.out.println("");
    System.out.println(description);

  }

  public static void printBorder(int length){
    for (int i = 0; i < (length); i++) {
      System.out.print("=");
    }
    System.out.println("");
  }
}
```

## purpose of methods to avoid repeating the code for the same action:

```java
public class Main {
  public static void main(String[] args) {
    int number = 51;

    checkNumber(number);

    int number2 = 49;
    
    checkNumber(number2);
    /* We get the number
    We check whether or not it is bigger than 50
    We check whether or not it is smaller than 50
    We assume it is equal to 50 if all of the upper conditions are false
    */
  }

  public static void checkNumber(int number){
    if(number > 50){
      System.out.println("Number is greater than 50");
    }else if(number < 50){
      System.out.println("Number is less than 50");
    }else{
      System.out.println("Number is equal to 50");  
    }
  }
}
```
## void for action; return for String method:
```java
public class Main {
  public static void main(String[] args) {
    int number = 51;

    String result = checkNumber(number);
    System.out.println(result);
    
    int number2 = 49;
    
    String result2 = checkNumber(number2);
    System.out.println(result2);
    /* We get the number
    We check whether or not it is bigger than 50
    We check whether or not it is smaller than 50
    We assume it is equal to 50 if all of the upper conditions are false
    */
  }
  //Void is just for action
  //int it is returning a number
  //string is returning a text
  //double is returning a double 
  //...
  public static String checkNumber(int number){
    if(number > 50){
      return "Number is greater than 50";
    }else if(number < 50){
      return "Number is less than 50";
    }else{
      return "Number is equal to 50";  
    }
  }
}
```
