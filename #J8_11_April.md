## Java
# Loops ||
- Diving deep in for and while loops
- Experimenting with both loops.
- __Team work:__ Develop a program, that iterates through numbers from 0 till 15.
-- For numbers that are divided by 3: print out "Wo";
-- For numbers that are divided by 5: print out "Tech";
-- For numbers divided by 3 and 5: print out "WoTech".
  
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
# guessing game: basics
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
## Teamwork 1
+ Team work: Develop a program, that iterates through numbers from 0 till X amount of times (X is user provided);for numbers that are divided by 3: print out "Wo"; for numbers that are divided by 5: print out "Tech"; or numbers divided by 3 and 5: print out "WoTech".

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner scanner = new Scanner(System.in);

    // user enters a number X
    // prints numbers from 0 to that number X
    // divided by 3 - Wo
    // divided by 5 - Tech
    // divided by 3 and 5 - WoTech
    // if else - print X
    System.out.println("Enter a number: ");
    int number = scanner.nextInt(); //waiting for a number
  

    for (int i = 1; i <= number; i++) {
      if (i % 3 == 0 && i % 5 == 0) {
        System.out.println("WoTech");
      } else if (i % 3 == 0) {
        System.out.println("Wo");
      } else if (i % 5 == 0) {
        System.out.println("Tech");
      } else {
        System.out.println(i);
      }
    }
    
    scanner.close();
   
  }
}
```
## Teamwork 2
+ User provides a text, and then the program puts it in a square, for example, if user provides "WoTech"

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner scanner = new Scanner(System.in);

    // user enters a number X
    // prints numbers from 0 to that number X
    // divided by 3 - Wo
    // divided by 5 - Tech
    // divided by 3 and 5 - WoTech
    // if else - print X

    // How to get a box around WoTech?
    // 1st line - to print 11 times equal sign "="
    // 2nd line - starts with "|" and 9 " " and "|"
    // 3 rd line - starts with "|" then " " + "WoTech" + " " + "|"
    // 4th line - starts with "|" and 9 " " and "|"
    // 5th line - to print 11 times equal sign "="
    // lineResult = lineResult + underscoresResult; // Combining 4 spaces and 1 underscore
    
    System.out.println("Type WoTech");
    String wotech = scanner.nextLine();
  
    String line = "==========";
    String emptyLine = "|        |";
    String woTechLine = "| WoTech |";
    String emptyLine2 = "|        |";
    String line2 = "==========";
  
        System.out.println(line);
        System.out.println(emptyLine);
        System.out.println(woTechLine);
        System.out.println(emptyLine2);
        System.out.println(line2);

// another way to print out:
//System.out.println(line + "\n" + emptyLine + "\n" + woTechLine + "\n" + emptyLine2 + "\n" + line2);
    scanner.close();
   
  }
}
```
