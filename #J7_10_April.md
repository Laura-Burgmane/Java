# Java

### input feature: Scanner

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner scanner = new Scanner(System.in);

    scanner.nextInt(); // Waits for us to provide an integer
    
    scanner.next(); // Waits for us to provide a string
    
    System.out.println("Hello world!");

    
  }
}

```

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner scanner = new Scanner(System.in);

    int number;
    number = scanner.nextInt(); // Waits for us to provide an integer
    System.out.println("This is the provided number:" + number);
    
    //scanner.nextLine(); // Waits for us to provide a string until pressed enter 
  }
}
```

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner scanner = new Scanner(System.in); //Opening a channel
    System.out.println("Write a number");
    int a = scanner.nextInt();
    System.out.println("Write an another number");
    int b = scanner.nextInt();
    
    System.out.println("A sum of A and B is " + (a + b));
    
    scanner.close(); // Closing the channel
    //scanner.nextLine(); // Waits for us to provide a string until pressed enter 
  }
}
```

```java
public class Main {
  public static void main(String[] args) {
    
    System.out.println("Hello world!");

    int amountOfTimesToDuck = 10;
    while (amountOfTimesToDuck != 0) {
      System.out.println(amountOfTimesToDuck);
      amountOfTimesToDuck = amountOfTimesToDuck - 1;
    }
    
  }
}
```

# loops: while (with f-string and boolean)
```java
public class Main {
  public static void main(String[] args) {
    
    System.out.println("Hello world!");

    int i = 1; 
    boolean isEven = false; // First NUMBER IS ALWAYS ODD
    // isEven is True for second Number
    //Counts from 0 to 10
    //Provides whether or not the number is even or odd
    
    while (i <= 10) {
      String result = "";
      if (isEven == true){
        result = "even";
      } else {
        result = "odd";
      }
      System.out.println(i + " " + result);
      i = i + 1;
      isEven = !isEven; 
      // isEven == true -> isEven = false
      // isEven == false -> isEven = true;
    }
  }
}
```
