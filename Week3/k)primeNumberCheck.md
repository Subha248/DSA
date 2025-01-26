
---

### **Prime Number Checker in Java**

**Problem Statement:**

Write a program in Java to determine whether a given number \( n \) is a prime number or not.

#### **Definition of a Prime Number:**
- A prime number is a number greater than 1 that has no divisors other than 1 and itself.
- Examples: \( 2, 3, 5, 7, 11, 13, \dots \)

---

### **Code Implementation**

```java
import java.util.*; // Importing the Scanner class for user input

public class Main { 
    public static void main(String[] args) { 
        Scanner scan = new Scanner(System.in); // Creating a scanner object to read input
        
        int n = scan.nextInt(); // Reading an integer input from the user
        
        // Step 1: Check if the number is less than or equal to 1
        if (n <= 1) { 
            System.out.println("not a prime"); // If n is less than or equal to 1, it's not prime
            return; // Exit the program since we already know the result
        }
        
        // Step 2: Loop from 2 up to the square root of n
        for (int i = 2; i * i <= n; i++) { 
            // Check if n is divisible by i
            if (n % i == 0) { 
                System.out.println("not a prime"); // If n is divisible by i, it's not a prime number
                return; // Exit the program since we found a divisor
            }
        }
        
        // Step 3: If no divisors were found, n is a prime number
        System.out.println("a prime"); // Output that the number is prime
    }
}
```

---

### **How the Code Works**

The program uses a loop to check for divisors of \( n \). If any divisor other than \( 1 \) or \( n \) is found, it concludes that \( n \) is not a prime number. For efficiency, the loop runs only up to \( \sqrt{n} \), as any divisor greater than \( \sqrt{n} \) would have a corresponding divisor smaller than \( \sqrt{n} \).

---

### **Code Execution Table**

#### **Case 1: \( n = 7 \) (Prime)**

| **Step** | **Value of \( i \)** | **Check \( i \times i \leq n \)** | **Check \( n \% i == 0 \)** | **Action**               |
|----------|----------------------|----------------------------------|----------------------------|--------------------------|
| 1        | Input \( n = 7 \)    | -                                | -                          | Start                   |
| 2        | \( i = 2 \)          | \( 2 \times 2 = 4 \leq 7 \)      | \( 7 \% 2 \neq 0 \)        | Continue Loop           |
| 3        | \( i = 3 \)          | \( 3 \times 3 = 9 > 7 \)         | -                          | Exit Loop               |
| 4        | -                    | -                                | -                          | Print "a prime"         |

**Output:**
```
a prime
```

---

#### **Case 2: \( n = 10 \) (Not Prime)**

| **Step** | **Value of \( i \)** | **Check \( i \times i \leq n \)** | **Check \( n \% i == 0 \)** | **Action**               |
|----------|----------------------|----------------------------------|----------------------------|--------------------------|
| 1        | Input \( n = 10 \)   | -                                | -                          | Start                   |
| 2        | \( i = 2 \)          | \( 2 \times 2 = 4 \leq 10 \)     | \( 10 \% 2 == 0 \)         | Print "not a prime"     |

**Output:**
```
not a prime
```

---

#### **Case 3: \( n = 1 \) (Not Prime)**

| **Step** | **Value of \( i \)** | **Check \( i \times i \leq n \)** | **Check \( n \% i == 0 \)** | **Action**               |
|----------|----------------------|----------------------------------|----------------------------|--------------------------|
| 1        | Input \( n = 1 \)    | -                                | -                          | Print "not a prime"     |

**Output:**
```
not a prime
```

---

#### **Case 4: \( n = 25 \) (Not Prime)**

| **Step** | **Value of \( i \)** | **Check \( i \times i \leq n \)** | **Check \( n \% i == 0 \)** | **Action**               |
|----------|----------------------|----------------------------------|----------------------------|--------------------------|
| 1        | Input \( n = 25 \)   | -                                | -                          | Start                   |
| 2        | \( i = 2 \)          | \( 2 \times 2 = 4 \leq 25 \)     | \( 25 \% 2 \neq 0 \)       | Continue Loop           |
| 3        | \( i = 3 \)          | \( 3 \times 3 = 9 \leq 25 \)     | \( 25 \% 3 \neq 0 \)       | Continue Loop           |
| 4        | \( i = 4 \)          | \( 4 \times 4 = 16 \leq 25 \)    | \( 25 \% 4 \neq 0 \)       | Continue Loop           |
| 5        | \( i = 5 \)          | \( 5 \times 5 = 25 \leq 25 \)    | \( 25 \% 5 == 0 \)         | Print "not a prime"     |

**Output:**
```
not a prime
```

---

### **Why This Code Works**

1. **Efficient Prime Check:**
   - The loop runs up to \( \sqrt{n} \), making it faster for larger numbers.
   
2. **Handles Edge Cases:**
   - Directly marks \( n \leq 1 \) as not prime.
   
3. **Early Exit:**
   - Stops checking as soon as a divisor is found, avoiding unnecessary calculations.

---

### **Summary of the Table Columns**

| **Column**             | **Description**                                                                 |
|-------------------------|---------------------------------------------------------------------------------|
| **Step**               | Sequence of operations in the program.                                         |
| **Value of \( i \)**    | The number currently being checked as a divisor.                              |
| **Check \( i \times i \leq n \)** | Verifies if the loop condition is satisfied.                              |
| **Check \( n \% i == 0 \)** | Checks if \( n \) is divisible by \( i \).                                    |
| **Action**              | Describes what the program does at each step (e.g., continue, exit, print).   |

---

