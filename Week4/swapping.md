
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

