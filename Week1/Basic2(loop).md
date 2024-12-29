
---

## **Question 1**

Write a program in Java to print numbers from `10` to `0` in reverse order using a `for` loop.

---

## **Program**

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        int n = 10; // Starting number

        // Loop to print numbers from 10 to 0 in reverse order
        for (int i = n; i >= 0; i--) {
            System.out.println(i);
        }
    }
}
```

---

## **Output**

### Example Output:
```
10
9
8
7
6
5
4
3
2
1
0
```

---

## **Explanation**

1. **Initialization:**
   - The variable `n` is set to `10`, which is the starting point for the countdown.

2. **For Loop:**
   ```java
   for (int i = n; i >= 0; i--) {
   ```
   - **`int i = n;`**: The loop starts with `i` equal to `10`.
   - **`i >= 0;`**: The loop continues as long as `i` is greater than or equal to `0`.
   - **`i--`**: After each iteration, the value of `i` decreases by `1`.

3. **Output:**
   - Inside the loop, the program prints the value of `i` on a new line.

---

## **How the Program Works**

| **Iteration** | **Value of `i`** | **Condition (`i >= 0`)** | **Output** |
|---------------|-------------------|--------------------------|------------|
| 1             | 10                | True                     | 10         |
| 2             | 9                 | True                     | 9          |
| 3             | 8                 | True                     | 8          |
| 4             | 7                 | True                     | 7          |
| 5             | 6                 | True                     | 6          |
| 6             | 5                 | True                     | 5          |
| 7             | 4                 | True                     | 4          |
| 8             | 3                 | True                     | 3          |
| 9             | 2                 | True                     | 2          |
| 10            | 1                 | True                     | 1          |
| 11            | 0                 | True                     | 0          |
| 12            | -1                | False                    | Loop ends  |

---

## **Key Points**

1. **Loop Control:**
   - The `for` loop structure ensures the countdown starts at `10` and stops at `0`.
   - The condition `i >= 0` ensures the loop runs until `i` becomes negative.

2. **Decrementing `i`:**
   - `i--` decreases the value of `i` by `1` in each iteration, creating the countdown effect.

3. **Scalability:**
   - You can modify the starting value of `n` to any other positive integer to print a countdown from that number.

---

