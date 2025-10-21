

---

### 💫 Final Simple Explanation:

* In Java, **arrays of objects** are stored in the **heap memory**.
* **Heap memory** is used for **dynamic memory allocation** — meaning objects can be created and placed anywhere there’s free space.
* Because of that, **heap memory is not continuous**, so the **objects** inside an array are **not stored side by side**.
* The array itself only stores **references (addresses)** that point to those scattered objects.

---

### 🌸 In one short line:

> Array of objects in Java are not stored continuously because they are stored in heap memory, where objects are dynamically allocated.

---


---

### ✅ Correct For-Each Version

```java
import java.util.*;

public class Demo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] arr = new int[n];

        // Input array elements
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        // Print array using for-each loop
        for (int num : arr) {
            System.out.print(num + " "); // num is the current element
        }
    }
}
```

---

### 🌸 Key Points:

1. `for(int num : arr)` → loops through **each element** of the array directly.
2. Inside the loop, `num` is **the current element**, not the index.
3. You **cannot use `arr[i]`** inside a for-each because there is no `i` index here.

---

### 🔹 Example Input & Output

**Input:**

```
4
5 10 15 20
```

**Output:**

```
5 10 15 20 
```

---


