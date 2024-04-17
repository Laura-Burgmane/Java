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
