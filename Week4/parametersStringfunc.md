
---

```java
// 🌸 Java Program: Function with Parameter and Return Type (String Function)
// Demonstrates how to pass a parameter to a method and return a String value.

import java.util.*;

public class Demo {

    public static void main(String[] args) {
        // Calling the method and storing the returned value
        String msg = greet("Subha");
        
        // Printing the returned message
        System.out.print(msg);
    }

    // Method with parameter and return type
    // Takes a String parameter 'name' and returns it
    public static String greet(String name) {
        String r = name; // store the input in variable r
        return r;        // return the value of r
    }
}
```

---


---

```java
import java.util.Scanner;

public class Demo {

    public static void main(String[] args) {
        // Create Scanner object for user input
        Scanner scan = new Scanner(System.in);

        // Take name as input from the user
        System.out.print("Enter your name: ");
        String name = scan.next();

        // Call the greet() method and store the returned value
        String msg = greet(name);

        // Display the returned message
        System.out.print(msg);
    }

    // Method Definition
    // Takes a String parameter 'name' and returns a greeting message
    public static String greet(String name) {
        String r = "Yoo " + name + "!";
        return r;
    }
}

/*
🧠 Sample Output:
-----------------
Enter your name: Subha
Yoo Subha!
*/
```

---

---

```java
// 🌸 Java Program: Swap Two Numbers Using a Temporary Variable
// Short explanation included for GitHub

public class Demo {

    public static void main(String[] args) {
        int a = 10;
        int b = 20;

        // Swap process:
        int temp = a;  // temp stores a (10)
        a = b;         // a stores b (20)
        b = temp;      // b stores temp (10)

        // Print swapped values
        System.out.print(a + " " + b); // Output: 20 10
    }
}

/* Short Explanation:
1. temp = a → store original a
2. a = b → move b to a
3. b = temp → move original a to b
*/
```

---

