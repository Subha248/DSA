
---

### **Program:**
```java
public class Human {
    int age;
    String nickname;

    public static void main(String[] args) {
        // Create an object of the Human class
        Human subha = new Human();
        
        // Set the object's attributes
        subha.age = 19;
        subha.nickname = "pradha";
        
        // Print the object's attributes
        System.out.println(subha.age);        // Output: 19
        System.out.println(subha.nickname);  // Output: pradha
    }
}
```

---

### **Explanation:**
- The `Human` class defines two attributes:
  - `age`: Represents the age of a person (integer).
  - `nickname`: Represents the nickname of a person (string).
- The `main` method serves as the entry point for program execution.
- Inside the `main` method:
  1. An object `subha` of the `Human` class is created.
  2. The `age` and `nickname` attributes are assigned values: `19` and `"pradha"`.
  3. The values of `age` and `nickname` are printed to the console using `System.out.println`.

---
---
This is a simple example of how to define a class, create an object, and access its attributes in Java. 

### **Program:**
```java
class Human {
    int age;
    String nickname;

    public static void main(String[] args) {
        // Create the first object
        Human subha = new Human();
        subha.age = 19;
        subha.nickname = "pradha";

        // Print attributes of the first object
        System.out.println(subha.age);        // Output: 19
        System.out.println(subha.nickname);  // Output: pradha

        // Create the second object
        Human saranya = new Human();
        saranya.age = 19;
        saranya.nickname = "sara";

        // Print attributes of the second object
        System.out.println(saranya.age);        // Output: 19
        System.out.println(saranya.nickname);  // Output: sara
    }
}
```

---

### **Explanation:**
- **Class Definition**:
  - The `Human` class defines two attributes:
    - `age`: Represents the age of a person (integer).
    - `nickname`: Represents the nickname of a person (string).
- **Object Creation**:
  1. An object `subha` is created, its attributes (`age` and `nickname`) are set, and the values are printed.
  2. Another object `saranya` is created, and its attributes are set and printed.
- **Purpose**:
  - Demonstrates how to create multiple objects of a class and assign unique values to their attributes.

---

This program showcases basic object-oriented principles in Java: defining classes, creating objects, and accessing object attributes. 
