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
