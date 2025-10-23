
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
