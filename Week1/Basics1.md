
---

## **Question**

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

