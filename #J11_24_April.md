# Java

## last weeks homework rewiev:

```java
public class Main {
  public static void main(String[] args) {
    
//Fill the party list with people you would like to invite to the party.
    
    String[] people = {"Oskars", "Anna", "Andris", "Kristine", "Zane", "Raivo"}; 
    boolean isIntheList = false;
    
// Check whether or not "Anna" is in the array.
    
    for (int i = 0; i < people.length; i++){
       if (people[i] == "Anna") {
         isIntheList = false; 
       break;
      } 
      if(isIntheList){ 
      System.out.println("Anna is not in the party list");
      }else{
          System.out.println("Anna is in the party list!");
        }
    }
      // Check whether or not "Maris" is in the array.
      for (int i = 0; i < people.length; i++){
        
         if (people[i] == "Maris"){
           isIntheList = true; 
        } 
      }
        if(isIntheList){
        System.out.println("Maris is in the party list!");
        }else{
            System.out.println("Maris is not in the party list!");
          }
        
  }
}
```
