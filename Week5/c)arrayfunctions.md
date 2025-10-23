
---

### ✅ **Code: Taking multiple inputs into an ArrayList**

```java
import java.util.*;

public class array {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Create an ArrayList of integers
        ArrayList<Integer> list = new ArrayList<>(10);

        // Take 5 numbers as input from the user
        for (int i = 0; i < 5; i++) {
            int n = sc.nextInt(); // take a new number each time
            list.add(n);          // add it to the list
        }

        // Print the entire ArrayList
        System.out.println(list);
    }
}
```

---

### 💡 **Explanation:**

* `ArrayList<Integer>` → a resizable array that stores integers.
* `list.add(n)` → adds each number entered by the user to the list.
* The `for` loop repeats 5 times to collect 5 numbers.
* `System.out.println(list)` → prints all elements together in `[ ]` format.

---

### 🧮 **Example Input:**

```
10 20 30 40 50
```

### 📤 **Output:**

```
[10, 20, 30, 40, 50]
```

---


)? It’s nice for beginners to include both styles on GitHub.

---

### ❌ Problem in your code

In this line:

```java
System.out.print(yoo.get());
```

You didn’t specify **which index** you want to get.
`get()` method **must have an index inside parentheses**, like:

```java
yoo.get(i)
```

Because `.get(index)` means → “fetch the element at this index”.

---

### ✅ Correct (fixed) code:

```java
import java.util.*;
public class array {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ArrayList<Integer> yoo = new ArrayList<>(10);

        // Take 5 numbers from the user
        for (int i = 0; i < 5; i++) {
            int n = sc.nextInt();
            yoo.add(n);
        }

        // Print the entire ArrayList
        System.out.println("ArrayList: " + yoo);

        // Get item at each index and print one by one
        for (int i = 0; i < 5; i++) {
            System.out.println("Element at index " + i + " = " + yoo.get(i));
        }

        // Print the entire list again at the end
        System.out.println("Final list: " + yoo);
    }
}
```

---

### 💡 Explanation (super simple):

#### 1️⃣ You create the ArrayList:

```java
ArrayList<Integer> yoo = new ArrayList<>(10);
```

#### 2️⃣ You take 5 numbers as input:

Let’s say you enter:

```
10 20 30 40 50
```

Now:

```
yoo = [10, 20, 30, 40, 50]
```

#### 3️⃣ You print the whole list:

```
ArrayList: [10, 20, 30, 40, 50]
```

#### 4️⃣ You print each item using `.get(i)`:

| i | yoo.get(i) | Printed output          |
| - | ---------- | ----------------------- |
| 0 | 10         | Element at index 0 = 10 |
| 1 | 20         | Element at index 1 = 20 |
| 2 | 30         | Element at index 2 = 30 |
| 3 | 40         | Element at index 3 = 40 |
| 4 | 50         | Element at index 4 = 50 |

#### 5️⃣ Final print again:

```
Final list: [10, 20, 30, 40, 50]
```

---

### 📤 Example Output:

```
ArrayList: [10, 20, 30, 40, 50]
Element at index 0 = 10
Element at index 1 = 20
Element at index 2 = 30
Element at index 3 = 40
Element at index 4 = 50
Final list: [10, 20, 30, 40, 50]
```

---


