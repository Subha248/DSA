

### **Program to Calculate Factorial of a Number**

**Question:**
Write a program to calculate the factorial of a given number \( n \).

**Testcase 1:**

Input:
```
n = 5
```

Output:
```
120
```

Explanation:
- The factorial of 5 is calculated as \( 5! = 5 \times 4 \times 3 \times 2 \times 1 = 120 \).

---

**Code:**

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        int n = 5; // Input number for factorial
        int fact = 1; // Variable to store factorial, initialized to 1
        
        // Loop to calculate factorial
        for (int i = 1; i <= n; i++) {
            fact = fact * i; // Multiply fact by current value of i
        }
        
        // Print the final factorial value
        System.out.println(fact);
    }
}
```

---

**Explanation of the Code:**

1. **Initialize `n` and `fact`:**
   - `n = 5`: Input number for which we calculate the factorial.
   - `fact = 1`: Variable to store the factorial result, initially set to 1.

2. **For Loop:**
   - The loop runs from `i = 1` to `i = n` (inclusive).
   - In each iteration:
     - Multiply the current value of `fact` by `i` and store the result back in `fact`.

3. **Final Result:**
   - After the loop ends, `fact` contains the final factorial of `n`.
   - Print the value of `fact` to display the result.

---

**Testcase Walkthrough:**

| **Iteration** | **Value of `i`** | **Value of `fact` (Before)** | **Value of `fact` (After)** | **Calculation**     |
|---------------|-------------------|-----------------------------|----------------------------|---------------------|
| 1             | 1                 | 1                           | 1                          | \( 1 \times 1 = 1 \) |
| 2             | 2                 | 1                           | 2                          | \( 1 \times 2 = 2 \) |
| 3             | 3                 | 2                           | 6                          | \( 2 \times 3 = 6 \) |
| 4             | 4                 | 6                           | 24                         | \( 6 \times 4 = 24 \) |
| 5             | 5                 | 24                          | 120                        | \( 24 \times 5 = 120 \) |

---

**Output:**
```
120
```

---

