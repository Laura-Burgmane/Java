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

## "Return" is like making the sandwich for someone else. You put in all the ingredients, make the sandwich, and then give it to someone. They can then do whatever they want with it, like eat it or share it.

On the other hand, "print.ln" is like showing off your sandwich to everyone else. You still make the sandwich, but instead of giving it to someone, you just show it to others. They can see it and know what it looks like, but they can't really do anything with it. They can't eat it or take it with them.

So, in simple terms, "return" gives something to be used later, while "print.ln" just shows something without giving it away.

## more examples:
```java
public class Main {
  public static void main(String[] args) {
    int money = 50;

    String result = buyJeans(money);

    System.out.println(result);
  }

  public static String buyJeans(int money){
    int price = 30;
    if(money > price) // 29.99
    {
      return "Person can afford Jeans";
    }else{
      return "Person cannot afford Jeans";
    }
  }
}

```
```java
// 7, 12, 18 
// Needs to sum them all together


public class Main {
  public static void main(String[] args) {
    int number1 = 7;
    int number2 = 12;
    
    int number3 = 18;

    int result = sum(number1, number2); // 7 + 12 = 19

    int finalResult = sum(result, number3); // 19 + 18 = 37

    System.out.println(finalResult);
  }

  public static int sum(int a, int b){
    return a + b;
  }
}
```
