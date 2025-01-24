
---

### **Problem Statement**

Write a program in Java to determine whether a given number \( n \) is a **prime number** or not.

#### **Definition of a Prime Number**:
A prime number is a number greater than 1 that has no divisors other than 1 and itself.  
Examples of prime numbers: \( 2, 3, 5, 7, 11, 13, \dots \).

---

### **Code with Line-by-Line Explanation**

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

1. **Input a Number**:  
   - The program asks the user to enter a number \( n \).
   - Example: If the user enters \( n = 7 \), the program will process it.

2. **Check if \( n \leq 1 \)**:
   - If the number is less than or equal to 1, it is **not a prime number**.
   - Example:
     - Input: \( n = 1 \).
     - Output: `"not a prime"`.

3. **Loop from \( 2 \) to \( \sqrt{n} \)**:
   - The loop runs from \( i = 2 \) up to \( i \times i \leq n \). This means we only check divisors up to the square root of \( n \) for efficiency.
   - For each \( i \), check if \( n \% i == 0 \):
     - If \( n \) is divisible by \( i \), it means \( n \) has a divisor other than 1 and itself, so it is **not prime**.

4. **Output if Prime**:
   - If the loop finishes without finding any divisors, the number \( n \) is **prime**.

---

### **Examples of Input and Output**

#### **Case 1: Input \( n = 7 \)**
- **Explanation**:
  - Loop checks:
    - \( i = 2 \): \( 2 \times 2 = 4 \leq 7 \), \( 7 \% 2 \neq 0 \).
    - \( i = 3 \): \( 3 \times 3 = 9 > 7 \), stop loop.
  - No divisors found.
- **Output**:  
  ```
  a prime
  ```

#### **Case 2: Input \( n = 10 \)**
- **Explanation**:
  - Loop checks:
    - \( i = 2 \): \( 2 \times 2 = 4 \leq 10 \), \( 10 \% 2 == 0 \), stop loop.
  - Divisor \( 2 \) found.
- **Output**:  
  ```
  not a prime
  ```

#### **Case 3: Input \( n = 1 \)**
- **Explanation**:
  - \( n \leq 1 \), so it’s not prime.
- **Output**:  
  ```
  not a prime
  ```

#### **Case 4: Input \( n = 25 \)**
- **Explanation**:
  - Loop checks:
    - \( i = 2 \): \( 2 \times 2 = 4 \leq 25 \), \( 25 \% 2 \neq 0 \).
    - \( i = 3 \): \( 3 \times 3 = 9 \leq 25 \), \( 25 \% 3 \neq 0 \).
    - \( i = 4 \): \( 4 \times 4 = 16 \leq 25 \), \( 25 \% 4 \neq 0 \).
    - \( i = 5 \): \( 5 \times 5 = 25 \leq 25 \), \( 25 \% 5 == 0 \), stop loop.
  - Divisor \( 5 \) found.
- **Output**:  
  ```
  not a prime
  ```

---

### **Why This Code Works**
1. **Efficient Prime Check**:
   - Only checks divisors up to \( \sqrt{n} \), which makes it faster for large numbers.
2. **Handles Edge Cases**:
   - Numbers \( n \leq 1 \) are directly marked as not prime.
3. **Early Exit**:
   - Stops checking as soon as it finds a divisor.

---

---

### **Code Execution Table**

#### **Case 1: \( n = 7 \) (Prime)**

| Step | \( i \) (Current Divisor) | \( i \times i \leq n \)? | \( n \% i == 0 \)? | Action                    |
|------|---------------------------|--------------------------|--------------------|---------------------------|
| 1    | Input \( n = 7 \)         | -                        | -                  | Start                    |
| 2    | \( i = 2 \)               | \( 2 \times 2 = 4 \leq 7 \) | \( 7 \% 2 \neq 0 \) | Continue Loop             |
| 3    | \( i = 3 \)               | \( 3 \times 3 = 9 > 7 \)    | -                  | Exit Loop                |
| 4    | -                         | -                        | -                  | Print `"a prime"`         |

**Output**:  
```
a prime
```

---

#### **Case 2: \( n = 10 \) (Not Prime)**

| Step | \( i \) (Current Divisor) | \( i \times i \leq n \)? | \( n \% i == 0 \)? | Action                    |
|------|---------------------------|--------------------------|--------------------|---------------------------|
| 1    | Input \( n = 10 \)        | -                        | -                  | Start                    |
| 2    | \( i = 2 \)               | \( 2 \times 2 = 4 \leq 10 \) | \( 10 \% 2 == 0 \) | Print `"not a prime"` and Exit |

**Output**:  
```
not a prime
```

---

#### **Case 3: \( n = 1 \) (Not Prime)**

| Step | \( i \) (Current Divisor) | \( i \times i \leq n \)? | \( n \% i == 0 \)? | Action                    |
|------|---------------------------|--------------------------|--------------------|---------------------------|
| 1    | Input \( n = 1 \)         | -                        | -                  | Print `"not a prime"` and Exit |

**Output**:  
```
not a prime
```

---

#### **Case 4: \( n = 25 \) (Not Prime)**

| Step | \( i \) (Current Divisor) | \( i \times i \leq n \)? | \( n \% i == 0 \)? | Action                    |
|------|---------------------------|--------------------------|--------------------|---------------------------|
| 1    | Input \( n = 25 \)        | -                        | -                  | Start                    |
| 2    | \( i = 2 \)               | \( 2 \times 2 = 4 \leq 25 \) | \( 25 \% 2 \neq 0 \) | Continue Loop             |
| 3    | \( i = 3 \)               | \( 3 \times 3 = 9 \leq 25 \) | \( 25 \% 3 \neq 0 \) | Continue Loop             |
| 4    | \( i = 4 \)               | \( 4 \times 4 = 16 \leq 25 \) | \( 25 \% 4 \neq 0 \) | Continue Loop             |
| 5    | \( i = 5 \)               | \( 5 \times 5 = 25 \leq 25 \) | \( 25 \% 5 == 0 \) | Print `"not a prime"` and Exit |

**Output**:  
```
not a prime
```

---

#### **Case 5: \( n = 2 \) (Prime)**

| Step | \( i \) (Current Divisor) | \( i \times i \leq n \)? | \( n \% i == 0 \)? | Action                    |
|------|---------------------------|--------------------------|--------------------|---------------------------|
| 1    | Input \( n = 2 \)         | -                        | -                  | Start                    |
| 2    | \( i = 2 \)               | \( 2 \times 2 = 4 > 2 \)    | -                  | Exit Loop                |
| 3    | -                         | -                        | -                  | Print `"a prime"`         |

**Output**:  
```
a prime
```

---

### **Explanation of Table Columns**

1. **Step**: Represents the sequence of operations in the program.
2. **\( i \) (Current Divisor)**: The number being checked as a possible divisor of \( n \).
3. **\( i \times i \leq n \)?**: Verifies if the loop condition holds (whether \( i \times i \) is still less than or equal to \( n \)).
4. **\( n \% i == 0 \)?**: Checks if \( n \) is divisible by \( i \).
5. **Action**: What the program does at that step (e.g., continue, print output, or exit).

---

