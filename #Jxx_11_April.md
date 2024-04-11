
# triangle left
```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in); // Opening a channel for user input
    int number = scanner.nextInt(); // Waiting for a number

    String result = ""; // an empty string
                    // 1 <= 5
    for (int i = 1; i <= number; i++) { // We do action before first cycle; condition for cycle; action after every cycle
      result = result + "_";
      System.out.println(result);
    }

    scanner.close();
  }
}
```
# triangle right
```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    /*
        _ // 4 spaces and one underscore
       __ // 3 spaces and two underscores
      ___ // 2 spaces and three underscores
     ____ // 1 space and four underscores
    _____ // 0 spaces and five underscores
    // X = 5
    // spaces = X - i;
    // underscores = i;
    */
    Scanner scanner = new Scanner(System.in);
    System.out.println("Please write a number!");
    int number = scanner.nextInt();

    String space = " ";
    String underScore = "_";
    for (int i = 1; i <= number; i++) { 
      int spacesCount = number - i;
      String lineResult = space.repeat(spacesCount); // Just 4 spaces
      String underscoresResult = underScore.repeat(i); // Just 1 underscore
      lineResult = lineResult + underscoresResult; // Combining 4 spaces and 1 underscore
      System.out.println(lineResult);
    }

    scanner.close();
  }
}
```

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner scanner = new Scanner(System.in);
    int number = 58;

    //1. We have a number
    
    //2. We ask for the user to guess the number
    //3. If the guessed number is bigger, then we say  "Too big"
    //4. If the guessed number is smaller, then we say "Too small"
    //5. If the guessed number is correct, then we say "Correct"
    //2-5 line a loop, we stop the loop, when the user is correct
    boolean userGuessedCorrectly = false;
    while(!userGuessedCorrectly) {
      System.out.println("Please guess a number!");
      int guess = scanner.nextInt(); //A number that user provides

      if(number == guess) {
        System.out.println("Good job, you guessed correctly");
        userGuessedCorrectly = true;
      }
    }
    System.out.println("Guessing game is over!");
    scanner.close();
  }
}
```
# guessing game; break and continue
```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner scanner = new Scanner(System.in);
    int number = 58;

    // 1. We have a number

    // 2. We ask for the user to guess the number
    // 3. If the guessed number is bigger, then we say "Too big"
    // 4. If the guessed number is smaller, then we say "Too small"
    // 5. If the guessed number is correct, then we say "Correct"
    // 2-5 line a loop, we stop the loop, when the user is correct

    while (true) {
      System.out.println("Please guess a number!");
      int guess = scanner.nextInt(); // A number that user provides

      if (number == guess) {
        System.out.println("Good job, you guessed correctly");
        break;
      } 
      if (number < guess) {
        System.out.println("Sorry, the number is too big");
        continue;
      }
      System.out.println("Sorry, the number is too small");
    }
    System.out.println("Guessing game is over!");
    scanner.close();
  }
}
```
# guessing game: simpler way
```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner scanner = new Scanner(System.in);
    int number = 58;

    // 1. We have a number

    // 2. We ask for the user to guess the number
    // 3. If the guessed number is bigger, then we say "Too big"
    // 4. If the guessed number is smaller, then we say "Too small"
    // 5. If the guessed number is correct, then we say "Correct"
    // 2-5 line a loop, we stop the loop, when the user is correct
    boolean userGuessedCorrectly = false;
    while (!userGuessedCorrectly) {
      System.out.println("Please guess a number!");
      int guess = scanner.nextInt(); // A number that user provides

      if (number == guess) {
        System.out.println("Good job, you guessed correctly");
        userGuessedCorrectly = true;
      } 
      else if (number < guess) {
        System.out.println("Sorry, the number is too big");
      }
      else {
        System.out.println("Sorry, the number is too small");
      }
    }
    System.out.println("Guessing game is over!");
    scanner.close();
  }
}
```
