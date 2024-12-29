
---

## **Question 1**

Write a program in Java to check if a person is eligible based on their age.  
- If the age is **greater than or equal to 18**, the program should:
  - Print `"eligible"`.
  - Increment the age by 1.
- Otherwise, the program should print `"Not eligible"`.

Finally, the program will print the updated age.

---

## **Program**

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        System.out.println("Enter age:");
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt(); // Input the age
        
        if (n >= 18) { // Check if the age is 18 or older
            n++; // Increment the age
            System.out.println("eligible");
        } else { // If the age is less than 18
            System.out.println("Not eligible");
        }
        
        System.out.println(n); // Print the (possibly updated) age
    }
}
```

---

## **Output**

### Example 1:
**Input:**
```
Enter age:
18
```

**Output:**
```
Enter age:
eligible
19
```

---

### Example 2:
**Input:**
```
Enter age:
30
```

**Output:**
```
Enter age:
eligible
31
```

---

### Example 3:
**Input:**
```
Enter age:
17
```

**Output:**
```
Enter age:
Not eligible
17
```

---

## **Explanation**

1. **Input Handling:**
   - The user enters an integer value for their age (`n`).

2. **Eligibility Check (`if`):**
   - If `n >= 18`:
     - The program prints `"eligible"`.
     - The age is incremented by 1 (`n++`).
   - If `n < 18`:
     - The program prints `"Not eligible"`, and the age remains unchanged.

3. **Final Output:**
   - The program prints the updated or unchanged age based on the conditions.

---

## **Working Table**

The following table shows how the program works step by step:

| **Input (Age)** | **Condition (`n >= 18`)** | **Output**           | **Updated Age (`n`)** |
|------------------|---------------------------|-----------------------|------------------------|
| 18               | `true`                   | `"eligible"`          | 19                     |
| 30               | `true`                   | `"eligible"`          | 31                     |
| 17               | `false`                  | `"Not eligible"`      | 17                     |
| 50               | `true`                   | `"eligible"`          | 51                     |
| 16               | `false`                  | `"Not eligible"`      | 16                     |

---

## **How to Use:**

1. **Input:**
   - Enter your age when prompted by the program.

2. **Output:**
   - The program will print whether you are `"eligible"` or `"Not eligible"`.
   - It will also print the updated or unchanged age.

---
Here’s the full content formatted for your GitHub repository, including the **question**, **program**, **output**, **explanation**, and a **table to visualize the working**.

---

## **Question 2**

Write a program in Java to find the largest number among three numbers entered by the user.  
The program should:
- Compare the numbers and determine which one is the largest.
- Ensure only one output is displayed using `if-else if-else`.

---

## **Program**

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        System.out.println("Enter three numbers:");
        Scanner scan = new Scanner(System.in);

        // Input three numbers
        int a = scan.nextInt();
        int b = scan.nextInt();
        int c = scan.nextInt();

        // Check the largest number
        if (a >= b && a >= c) {
            System.out.println("a is largest");
        } else if (b >= a && b >= c) {
            System.out.println("b is largest");
        } else {
            System.out.println("c is largest");
        }
    }
}
```

---

## **Output**

### Example 1:
**Input:**
```
Enter three numbers:
10
20
30
```

**Output:**
```
c is largest
```

---

### Example 2:
**Input:**
```
Enter three numbers:
50
30
40
```

**Output:**
```
a is largest
```

---

### Example 3:
**Input:**
```
Enter three numbers:
20
50
50
```

**Output:**
```
b is largest
```

---

## **Explanation**

1. **Input Handling:**
   - The user is prompted to input three integers, which are stored in variables `a`, `b`, and `c`.

2. **Comparison Logic (`if-else if-else`):**
   - **Case 1:** If `a` is greater than or equal to both `b` and `c`, the program prints `"a is largest"`.
   - **Case 2:** If `b` is greater than or equal to both `a` and `c`, the program prints `"b is largest"`.
   - **Case 3:** If neither of the above conditions is true, `c` must be the largest, and the program prints `"c is largest"`.

3. **Output:**
   - The program outputs the largest number based on the conditions.

---

## **Working Table**

The following table shows the logic applied to different inputs:

| **a** | **b** | **c** | **Condition Checked**          | **Output**        |
|-------|-------|-------|-------------------------------|-------------------|
| 10    | 20    | 30    | `c >= a && c >= b`            | `c is largest`    |
| 50    | 30    | 40    | `a >= b && a >= c`            | `a is largest`    |
| 20    | 50    | 50    | `b >= a && b >= c`            | `b is largest`    |
| 30    | 30    | 10    | `a >= b && a >= c`            | `a is largest`    |
| 40    | 40    | 40    | Any condition (all are equal) | `a is largest`    |

---

## **Why Use `if-else if-else`?**

### **Advantages:**
1. **Mutual Exclusivity:**
   - Only one condition is evaluated once the correct one is found.
   - This prevents redundant evaluations and multiple outputs for overlapping conditions.

2. **Efficiency:**
   - The program stops checking further conditions as soon as one is true.

3. **Cleaner Logic:**
   - Ensures a single, logical flow with no ambiguity.

### Example:
For input `10, 10, 5`:
- Using `if-else if-else`:
  - Output: `a is largest`
- Using independent `if` statements:
  - Output: 
    ```
    a is largest
    b is largest
    ```

---

## **How to Use:**

1. Input three integers when prompted.
2. The program will determine the largest number among the three and print the result.

---

This content ensures clarity and ease of understanding for future reference. Let me know if you need further assistance! 🚀

