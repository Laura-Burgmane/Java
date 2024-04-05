# Java
## Scopes and User input 

- Understanding variable scopes
- Use Scanner, to provide values for simple programs.
- __Team work:__ Create a program, that asks user some questions and then creates a story based on the values.

## 💡else if
```java
double temp = -22.12;
      if (temp <= 5) {
        String message = "The weather is good outside";
        System.out.println("message");
      } else if (temp <= 15) {
        System.out.println("message");
      } else if (temp <= 30) {
        System.out.println("message");
      } else {
        System.out.println("mesage");
      }
    }
  }
```
## 💡scope
```java
//Ledusskapis
public class Main {
    public static void main(String[] args) {
      
          System.out.println("Let's go and check out what is in the fridge!");
          var isFridgeOpen = true;
          String result;

          if (isFridgeOpen) {
            var item1 = "Cheese";
            var item2 = "Milk";
            var item3 = "Eggs";
            result = item1 + item2 + item3;
          } else {
            result = "Fridge is closed, open the fridge";
          }
          System.out.println(result);
          // ERROR System.out.println(item1);
        }
      }
```
## 💡 class, scope, methods
```java
//Saprast, kāpēc izdrukā rezultātu 14 - 200 - 50 (bet ne 20)

public class Main {

  static int sharedValue = 200;
    
    public static void main(String[] args) {
      int mainValue = 14;
      System.out.println (mainValue);
      secondMethod();
      firstMethod();
    }
    
    public static void firstMethod (){
      int firstValue = 50;
      System.out.println (firstValue);
    }

    public static void secondMethod (){
     int secondValue = 120;
      System.out.println(sharedValue);    
    }   
  }

```  
## 🤼‍♀️ __Team work:__
