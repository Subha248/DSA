### **3:**

### **Do All Methods Need a `return`?**
No, not all methods in Java need a `return` statement. It depends on the method's **return type**.

---

### **1. Methods That Must Have `return`**
- If a method has a **non-void return type** (e.g., `int`, `boolean`, `String`), it **must return a value** of that type.

#### Example:
```java
int add(int a, int b) {
    return a + b;  // Returns an integer
}

boolean isAdult(int age) {
    return age >= 18;  // Returns a boolean
}
```

---

### **2. Methods That Don’t Need `return`**
- Methods with a **void return type** don’t need a `return` statement. They are used for actions like printing or updating.

#### Example:
```java
void greet(String name) {
    System.out.println("Hello, " + name);  // No return needed
}
```

- **Optional Early Exit**:
  - A `void` method can use `return;` to exit early.
  ```java
  void checkAge(int age) {
      if (age < 18) {
          System.out.println("Too young.");
          return;  // Exits early
      }
      System.out.println("Welcome!");
  }
  ```

---

### **Key Rule**
- **Void Methods**: Don’t require `return`.
- **Non-Void Methods**: Must have a `return` statement with a value matching the return type.
- 
### ** EXAMPLE PROGRAM**
