# Java
## Arrays ||

- Diving deep in arrays
- Using loops to print out array values
- __Team work:__ Find maximum and minimum values in integer array.


## yesterday's hard task:
```java
/*
A step by step solution to the largest number (I will give hints only for largest number, but the solution for both are the same)

1.Define an int array that is x amounts large
 1.1. Put values in the array 
DONE
 
2.Define an int variable called maxNumber, this is where we store the value of largest number
 2.1. The value of maxNumber should be the first value of the array
 Done
 
3.Go through the array with a loop
 3.1. If the i number is bigger than the maxNumber, we need to change the value of maxNumber to i
 3.2. Repeat  3.1. on the next cycle until the end of the array
Print out - "Largest number of array is " + maxNumber 


*/


public class Main {
  public static void main(String[] args) {

    int[] numbers = new int[5]; // {1, 7, 3, -2, 100};
    numbers[0] = 1;
    numbers[1] = 7;
    numbers[2] = 3;
    numbers[3] = -2;
    numbers[4] = 100;
    int maxNumber = numbers[0]; // 1 > 1 ... 7 > 1 ... 3 > 7 .... ... 100 > 7
    //1st cycle -> maxNumber is 1
    //2nd cycle -> maxNumber is 7
    //3rd cycle -> maxNumber is 7
    //...
    //5th cycle -> maxNumber is 100
    for(int i = 0; i < numbers.length; i++){
      if(numbers[i] > maxNumber){
        maxNumber = numbers[i];
      }
    }
    System.out.println("Largest number of array is " + maxNumber);
  }
}
```

## this is the same thing, different way written down:

```java
    int[] numbers = new int[5];

    numbers[0] = 1;
    numbers[1] = 7;
    numbers[2] = 3;
    numbers[3] = -2;
    numbers[4] = 100;
```
```java
int[] numbers = {1, 7, 3, -2, 100};
```
## simple/basic way without for loop:
```java
/*
A step by step solution to the largest number (I will give hints only for largest number, but the solution for both are the same)

1.Define an int array that is x amounts large
 1.1. Put values in the array 
DONE
 
2.Define an int variable called maxNumber, this is where we store the value of largest number
 2.1. The value of maxNumber should be the first value of the array
 Done
 
3.Go through the array with a loop
 3.1. If the i number is bigger than the maxNumber, we need to change the value of maxNumber to i
 3.2. Repeat  3.1. on the next cycle until the end of the array
Print out - "Largest number of array is " + maxNumber 


*/


public class Main {
  public static void main(String[] args) {

    int[] numbers = new int[5];
    numbers[0] = 1;
    numbers[1] = 7;
    numbers[2] = 3;
    numbers[3] = -2;
    numbers[4] = 100;

    int maxNumber = numbers[0]; // maxNumber = 1

    if (numbers[0] > maxNumber){ // If 1 > 1
      maxNumber = numbers[0];
    }

    if (numbers[1] > maxNumber){ // If 7 > 1
      maxNumber = numbers[1];
    }

    if(numbers[2] > maxNumber){ // If 3 > 7
      maxNumber = numbers[2];
    }

    if(numbers[3] > maxNumber){// If -2 > 7
      maxNumber = numbers[3];
    }

    if(numbers[4] > maxNumber){ // If 100 > 7
      maxNumber = numbers[4];
    }

    System.out.println("Largest number of array is " + maxNumber);
    
  }
}
```

## normal way with for loop:
```java
    //We declare i as 0
    for(int i = 0; i < numbers.length; i++) { // If i < array size, we go in a loop
      //Start of the cycle
      System.out.println(i); // 0 1 2 3 4

      //End of the cycle
    } // At the end of the cycle we increment i by 1
```
## check if the item (provided by user) is on the list:
```java
/*

We have an array with different numbers {1, 3, 4, 2, 5, 8}

User is providing a number

Check whether or not this number exists in the array
*/

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    int[] numbers = { 1, 3, 4, 2, 5, 8 }; // numbers.length = size of the numbers = 6

    System.out.println("Please write your favourite digit");

    Scanner scanner = new Scanner(System.in);
    int favouriteNumber = scanner.nextInt();

    boolean isFound = false;
    
    for (int i = 0; i < numbers.length; i++) {

      if (numbers[i] == favouriteNumber) {
        isFound = true;
        break; //EXITS THE FOR LOOP ALTOGETHER, ignoring the i < numbers.length
      }
      
    }
    if(isFound){
      System.out.println("Your favourite number " + favouriteNumber + " is in the array");
    } else {
      System.out.println("Your favourite number " + favouriteNumber + " is NOT FOUND!");
    }
    
    scanner.close();
  }
}
```
## description in human language:
```java
/*

We have an array with different numbers {1, 3, 4, 2, 5, 8}

User is providing a number

Check whether or not this number exists in the array

1. Define an array with numbers
2. Ask the user for a favouriteNumber
3. Defining a isFound boolean (represents whether or not the number is found)
4. Go through the array with a for loop
4.1. On every cycle we check whether or not the number is equal to the favouriteNumber
4.1.1. If it is, we set isFound to true and exit the searching loop with a "break;"
4.1.2. If it is not, we set isFound to false and we repeat the 4.1. steps 
5. At the end of the cycle we check whether or not isFound is true
5.1. If isFound == true -> Then we print your favourite number is found
5.2. If isFound == false -> Then we print NOT FOUND!

*/

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    int[] numbers = { 1, 3, 4, 2, 5, 8, 1000 }; // numbers.length = size of the numbers = 6

    System.out.println("Please write your favourite digit");

    Scanner scanner = new Scanner(System.in);
    int favouriteNumber = scanner.nextInt();

    boolean isFound = false;
    
    for (int i = 0; i < numbers.length; i++) {

      if (numbers[i] == favouriteNumber) {
        isFound = true;
        break; //EXITS THE FOR LOOP ALTOGETHER, ignoring the i < numbers.length
      }
      
    }
    
    if(isFound){
      System.out.println("Your favourite number " + favouriteNumber + " is in the array");
    } else {
      System.out.println("Your favourite number " + favouriteNumber + " is NOT FOUND!");
    }
    
    scanner.close();
  }
}
```
## another code...
```java
/*

We have an array with different numbers {1, 3, 4, 2, 5, 8}

User is providing a number

Check whether or not this number exists in the array

1. Define an array with numbers
2. Ask the user for a favouriteNumber
3. Defining a isFound boolean (represents whether or not the number is found)
4. Go through the array with a for loop
4.1. On every cycle we check whether or not the number is equal to the favouriteNumber
4.1.1. If it is, we set isFound to true and exit the searching loop with a "break;"
4.1.2. If it is not, we set isFound to false and we repeat the 4.1. steps 
5. At the end of the cycle we check whether or not isFound is true
5.1. If isFound == true -> Then we print your favourite number is found
5.2. If isFound == false -> Then we print NOT FOUND!

*/

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    int[] numbers = { 1, 3, 4, 2, 5, 8, 1000 }; // numbers.length = size of the numbers = 6

    System.out.println("Please write your favourite digit");

    Scanner scanner = new Scanner(System.in);
    int favouriteNumber = scanner.nextInt(); // 2

    boolean isFound = false; // default value is that it is not found
    
    for (int i = 0; i < numbers.length; i++) { // GO through every index in the array
          //       2 == 2
      if (numbers[i] == favouriteNumber) { // if the number is equal to the favouriteNumber
        isFound = true;
        break; //EXITS THE FOR LOOP ALTOGETHER, ignoring the i < numbers.length
      } // If the number is not equal -> move on to the next cycle
      
    }
    
    if(isFound == true){
      System.out.println("Your favourite number " + favouriteNumber + " is in the array!");
    } else {
      System.out.println("Your favourite number " + favouriteNumber + " is NOT FOUND!");
    }
    
    scanner.close();
  }
}
```
