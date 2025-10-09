

---

## 🌸 **4 Types of Methods in Java**

| Type           | Input | Output (Return) | Return Type           | Example Purpose                      |
| -------------- | ----- | --------------- | --------------------- | ------------------------------------ |
| **1️⃣ Type 1** | ❌ No  | ❌ No            | `void`                | Just prints something                |
| **2️⃣ Type 2** | ❌ No  | ✅ Yes           | `int`, `String`, etc. | Returns a value                      |
| **3️⃣ Type 3** | ✅ Yes | ✅ Yes           | `int`, `String`, etc. | Takes input and returns value        |
| **4️⃣ Type 4** | ✅ Yes | ❌ No            | `void`                | Takes input and prints inside method |

---

### 💖 **1️⃣ Type 1 — No Input, No Output**

> Only prints, doesn’t return anything.

```java
public static void greet() {
    System.out.println("Hello, sweetheart!");
}

public static void main(String[] args) {
    greet(); // prints "Hello, sweetheart!"
}
```

---

### 💙 **2️⃣ Type 2 — No Input, With Output**

> Doesn’t take anything, but returns a value.

```java
public static int year() {
    return 2025;
}

public static void main(String[] args) {
    int result = year();
    System.out.println(result); // 2025
}
```

---

### 💚 **3️⃣ Type 3 — With Input, With Output**

> Takes input and returns a value.

```java
public static int sum(int a, int b) {
    return a + b;
}

public static void main(String[] args) {
    int result = sum(5, 8);
    System.out.println(result); // 13
}
```

---

### 💛 **4️⃣ Type 4 — With Input, No Output**

> Takes input and prints inside method (no return).

```java
public static void sum(int a, int b) {
    System.out.println(a + b);
}

public static void main(String[] args) {
    sum(5, 8); // prints 13 directly
}
```

---

### 💡 **Shortcut to Remember**

> 🧠 **Think in terms of “Input” and “Return”**

```
Type 1 → No input, No return  
Type 2 → No input, Return  
Type 3 → Input, Return  
Type 4 → Input, No return
```

---


Would you like me to make a **cute one-page notes image** of this for easy screenshot revision? 📄✨
