## Java 
# Arrays |

- Introduction in arrays
- Experimenting with different data types for arrays
- _Team work:_ Talk about arrays and in what situations they could be used.

  # iepriekšējās reizes mājas darbs, uzlabots:
  ```java
  import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner scanner = new Scanner(System.in);
    System.out.println("Please enter a number: ");

    int number = scanner.nextInt(); //15

    for(int i = 1; i <= number; i++){
      // 1 2 3 4 5 ... 15
      String result = "";
      if (i % 3 == 0){ // 3 6 9 12 15
        result += "Wo";
      } 
      if (i % 5 == 0){ // 5 10 15
        result += "Tech";
      } 
      if(result.equals("")){ //if result is empty
        result = String.valueOf(i); //Then result = i (number)
      }
      System.out.println(result);

      scanner.close();
    }
  }
}
```
```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner scanner = new Scanner(System.in);
    System.out.println("Please enter a number: ");

    int number = scanner.nextInt(); //15

    for(int i = 1; i <= number; i++){
      // 1 2 3 4 5 ... 15

      // 7
      String result = "";
      if (i % 3 == 0){ //15
        result += "Wo"; //Add Wo to the result
      } 
      if (i % 5 == 0){ // 5 10 15
        result += "Tech";
      } 
      
      if (result == ""){ 
        //result = String.valueOf(i); //Then result = i (number)
        System.out.println(i);
      }else{
        System.out.println(result);
      }
      
      

      scanner.close();
    }
  }
}
```
# kvadrāta mājas darba izskaidrojums

```java

/*
// Padding is 3 characters long on one side
// Border is 1 character long on one side
=======================================================
|                                                     |
|   A very long string that is this characters long   |
|                                                     |
=======================================================
//WoTech = 6 characters long
// Width of the rectangle = 6 + 3 * 2 + 1 * 2 = 14
1. User writes a string -> any size
2. Calculate the width of the rectangle
  2.1. How long of a message we have
  2.2. Sum of messageLength and padding and borders
3. Print out upper border ==============
4. Print out an empty line with border |            |
5. Print out border + padding + text + padding + border
5. Print out an empty line with border |            |
6. Print out lower border ==============
*/
```
# arrays
```java
import java.util.Scanner; 
public class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);
    
    int[] arr = new int[5];

    for(int i = 0; i < arr.length; i++){ //[0], [1], [2]
      arr[i] = scanner.nextInt();
    }
    
    for(int i = 0; i < arr.length; i++){
      System.out.println(arr[i]);
    }

  }
}
```
 # more arrays:

 ```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in); //

    int[] arr = new int[5]; // Bounds is from 0 to 4
    // We ask the computer to create a closet
    //Where we could put 5 different boxes of a number
    // arr[0] = 5
    // arr[1] = 8
    // arr[2] = 13
    // arr[3] = 54
    // arr[4] = 80
    // arr[5] Index out of bounds

    for (int i = 0; i < arr.length; i++) { // 0 ... 1 -> 4
      //int number = scanner.nextInt();
      //arr[5] = scanner.nextInt();
      arr[i] = scanner.nextInt(); // 80
      
    }

    for (int i = 0; i < arr.length; i++) { // 0 -> 4
      System.out.println(arr[i]); // We are accessing arr[3]
    }
    
    scanner.close();//
  }
}
```
