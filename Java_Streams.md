Array String, filtering items containing word "table":

```java
public class Main {
    public static void main(String[] args) {
        var shopsItems = new ArrayList<String>();
        shopsItems.add("Glass table");        
        shopsItems.add("Wooden table");
        shopsItems.add("Round table");
        shopsItems.add("Doors");
        shopsItems.add("Trapdoor");
        shopsItems.add("Couch");
        shopsItems.add("Bed");
        shopsItems.add("Sofa");

        var filteredShopsItems = new ArrayList<String>();
        for(var item: shopsItems){
            if(item.contains("table")){
                filteredShopsItems.add(item);
            }
        }
        System.out.println(filteredShopsItems);
    }
}
```
Introducing Stream functionality: (with some kind of issues)

```java
        var filteredShopsItems = shopsItems
            .stream()
            .filter(item -> item.contains("table"))
            .collect(Collectors.toList());
```
Te pilns kods ar Stream lietām praktiskā darbībā:

```java
import java.util.ArrayList;
import java.util.stream.Collectors;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        var shopsItems = new ArrayList<String>();
        shopsItems.add("Glass table");
        shopsItems.add("Wooden table");
        shopsItems.add("Round table");
        shopsItems.add("Doors");
        shopsItems.add("Trapdoor");
        shopsItems.add("Couch");
        shopsItems.add("Bed");
        shopsItems.add("Sofa");

        var filteredShopsItems = shopsItems
                .stream()
                .skip(3)
                .limit(2)
                .collect(Collectors.toList());

        System.out.println(filteredShopsItems);
    }
}
```

