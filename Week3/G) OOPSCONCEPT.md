
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

This is a simple example of how to define a class, create an object, and access its attributes in Java. 
