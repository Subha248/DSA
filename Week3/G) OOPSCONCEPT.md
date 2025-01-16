
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
---

---

### **Code Explanation Step-by-Step**

#### **1. Define the Class**
```java
class Human {
    int age;          // Attribute to store the age of a Human
    String nickname;  // Attribute to store the nickname of a Human

    // Method to check if the person has a mobile phone
    boolean hasMobile() {
        return true;  // Always returns `true` for now
    }
}
```
- **`Human` Class**:
  - This is a blueprint for creating objects.
  - It has two properties (`age` and `nickname`) and one behavior (the `hasMobile()` method).

---

#### **2. Define the `main` Method**
```java
public static void main(String[] args) {
    // Step 1: Create an object of the Human class
    Human subha = new Human();
```
- The `main` method is the entry point of the program where execution starts.
- `Human subha = new Human();`:
  - Creates an object of the `Human` class named `subha`.
  - This object will have its own `age`, `nickname`, and the ability to call the `hasMobile()` method.

---

#### **3. Assign Values to the Object**
```java
subha.age = 19;        // Assigns the age attribute of the object `subha` to 19
subha.nickname = "pradha";  // Assigns the nickname attribute of the object `subha` to "pradha"
```
- Now, the `subha` object has:
  - `age = 19`
  - `nickname = "pradha"`

---

#### **4. Call the `hasMobile` Method**
```java
boolean s = subha.hasMobile();  // Calls the `hasMobile` method for the `subha` object
```
- The `hasMobile()` method is called on the `subha` object.
- The method **always returns `true`**, so `s` will now hold the value `true`.

---

#### **5. Print the Result**
```java
System.out.println(s);  // Prints the value of `s`, which is `true`
```
- The value of `s` (which is `true`) is printed to the console.

---

### **Complete Program**
```java
class Human {
    int age;
    String nickname;

    boolean hasMobile() {
        return true;  // This method always returns `true`
    }

    public static void main(String[] args) {
        // Step 1: Create an object of the Human class
        Human subha = new Human();

        // Step 2: Assign values to the object's attributes
        subha.age = 19;
        subha.nickname = "pradha";

        // Step 3: Call the `hasMobile` method and store the result
        boolean s = subha.hasMobile();

        // Step 4: Print the result of the `hasMobile` method
        System.out.println(s);  // Output: true
    }
}
```

---

### **Output**
When you run the program, the output will be:
```
true
```

---

### **Step-by-Step Summary**
1. A `Human` class is defined with:
   - Two attributes: `age` and `nickname`.
   - One method: `hasMobile()`, which always returns `true`.

2. In the `main` method:
   - An object of the `Human` class is created (`subha`).
   - The attributes `age` and `nickname` are assigned values (`19` and `"pradha"`).
   - The `hasMobile()` method is called for the `subha` object, and the result (`true`) is stored in `s`.

3. Finally, the value of `s` is printed, which is `true`.

