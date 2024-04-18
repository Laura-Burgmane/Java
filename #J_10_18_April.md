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

