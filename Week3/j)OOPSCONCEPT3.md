
### **What Are Access Specifiers?**
Access specifiers in Java define **who can access a class, method, or variable**. They control the visibility of members (attributes, methods, constructors) in your program.

There are **four main access specifiers** in Java:
1. **public**: Accessible from **anywhere**.
2. **private**: Accessible **only within the same class**.
3. **protected**: Accessible within the **same package** and by **subclasses**.
4. **(default)**: If you don’t specify any access modifier, it is accessible within the **same package** (also called "package-private").

---
```java

// Define the Human class
public class Human {
    // Public instance variable to store the age of a human
    public int age;  
    
    // Public instance variable to store the name of a human
    public String name;

    // Public method to display the age
    public void display() {  
        // Print the age to the console
        System.out.println("Age: " + age);
    }
}

// Define the Main class
class Main {
    // Main method: Entry point of the program
    public static void main(String[] args) {
        // Create an object of the Human class
        Human human = new Human();

        // Assign a value to the 'age' variable of the human object
        human.age = 25; // Setting the age to 25 (Accessing from outside the Human class)

        // Assign a value to the 'name' variable of the human object
        human.name = "Nandhini"; // Setting the name to "Nandhini" (Accessing from outside the Human class)

        // Call the display() method to print the age of the human object
        human.display(); // Calling the method from outside the Human class
                         // Output will be: Age: 25
    }
}
```

Output of the Program:

Age: 25

---

### **Beginner-Friendly Summary Table**
| Access Modifier | Same Class | Same Package | Subclass (Different Package) | Other Classes (Different Package) |
|------------------|------------|--------------|-------------------------------|------------------------------------|
| **public**       | ✅         | ✅           | ✅                            | ✅                                 |
| **private**      | ✅         | ❌           | ❌                            | ❌                                 |
| **protected**    | ✅         | ✅           | ✅                            | ❌                                 |
| **default**      | ✅         | ✅           | ❌                            | ❌                                 |

---



