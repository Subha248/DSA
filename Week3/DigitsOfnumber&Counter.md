### **Question 1**
Write a program that gets `n` as input and prints the number of digits in the number.

---

### **Program**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        System.out.println("Enter a number:");
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt(); // Input the number
        int count = 0; // Initialize count to 0

        // Loop to count the digits
        while (n > 0) {
            int ld = n % 10; // Extract the last digit (optional for understanding)
            count++; // Increment the count
            n = n / 10; // Remove the last digit
        }

        System.out.println("Number of digits: " + count); // Print the result
    }
}
```

---

### **Explanation**
1. **Input a Number**:
   - User enters an integer `n`.

2. **Count Digits**:
   - The program uses a `while` loop to count the digits.
   - The last digit is extracted using `n % 10`, but it is not mandatory for counting.
   - After processing the last digit, the number is reduced by dividing it by `10` (`n = n / 10`).
   - For each digit processed, `count` is incremented.

3. **Terminate the Loop**:
   - When `n` becomes `0`, the loop terminates.

4. **Output**:
   - After the loop, the program prints the total number of digits stored in `count`.

---

### **Test Cases**

#### Test Case 1:
**Input:**
```
325345
```

**Execution Steps**:
- `n = 325345`, `count = 0`
- `n = 32534`, `count = 1`
- `n = 3253`, `count = 2`
- `n = 325`, `count = 3`
- `n = 32`, `count = 4`
- `n = 3`, `count = 5`
- `n = 0`, `count = 6`

**Output:**
```
Number of digits: 6
```

---

#### Test Case 2:
**Input:**
```
9879
```

**Execution Steps**:
- `n = 9879`, `count = 0`
- `n = 987`, `count = 1`
- `n = 98`, `count = 2`
- `n = 9`, `count = 3`
- `n = 0`, `count = 4`

**Output:**
```
Number of digits: 4
```

---

### **Table for Visualization**

#### Input: `n = 325345`

| **Iteration** | **Value of `n`** | **Last Digit (`ld`)** | **Count** | **Action**        |
|---------------|-------------------|-----------------------|-----------|-------------------|
| 1             | 325345            | 5                     | 1         | `n = 32534`       |
| 2             | 32534             | 4                     | 2         | `n = 3253`        |
| 3             | 3253              | 3                     | 3         | `n = 325`         |
| 4             | 325               | 5                     | 4         | `n = 32`          |
| 5             | 32                | 2                     | 5         | `n = 3`           |
| 6             | 3                 | 3                     | 6         | `n = 0`           |

---

### **Output**
- **Test Case 1:** `Number of digits: 6`
- **Test Case 2:** `Number of digits: 4`

