
# Problem: Find the K-th Digit of A^B from the Right

Given two numbers `A` and `B`, find the `K`-th digit from the right of the result of `A^B` (A raised to the power of B).

---

### **Solution**

The program calculates \( A^B \) and extracts the \( K \)-th digit from the right using a loop.

---

### **Code**
```java
class Solution {
    public static long kthDigit(int A, int B, int K) {
        // Step 1: Find A^B using Math.pow
        long power = (long)Math.pow(A, B); // Example: 3^3 = 27
        long i = 1; // Counter to track position of digits

        // Step 2: Extract the k-th digit
        while (power > 0) {
            long ans = power % 10; // Extract the last digit
            if (i == K) { // Check if this is the k-th digit
                return ans; // Return the digit if position matches
            }
            i++; // Move to the next digit
            power = power / 10; // Remove the last digit
        }

        return 0; // If K is larger than the number of digits, return 0
    }
}
```

---

### **Steps in the Code**

1. **Calculate the Power:**
   ```java
   long power = (long)Math.pow(A, B);
   ```
   - Finds \( A^B \) using the `Math.pow` function.
   - Converts the result to `long` to handle large numbers.

2. **Initialize a Counter:**
   ```java
   long i = 1;
   ```
   - Tracks the digit's position, starting from the rightmost digit.

3. **Extract Digits from Right to Left:**
   ```java
   while (power > 0) {
       long ans = power % 10; // Extract the last digit
   ```
   - `% 10` retrieves the last digit of `power`.

4. **Check for K-th Digit:**
   ```java
   if (i == K) {
       return ans; // Return the digit if position matches
   }
   ```
   - Compares the position counter (`i`) with `K`.

5. **Move to the Next Digit:**
   ```java
   i++;
   power = power / 10;
   ```
   - Increments the counter `i`.
   - Removes the last digit from `power` by dividing it by `10`.

6. **Handle Invalid Cases:**
   ```java
   return 0;
   ```
   - If `K` is larger than the number of digits in \( A^B \), return `0`.

---

### **Example Walkthrough**

#### Example 1:
```
Input: A = 3, B = 3, K = 1
```

#### Execution:
1. Calculate \( 3^3 = 27 \).
2. Start the loop:
   - **Iteration 1:**
     - `power = 27`, `ans = 27 % 10 = 7`
     - `i = 1`
     - `i == K`, so return `7`.

#### Output:
```
7
```

---

#### Example 2:
```
Input: A = 3, B = 3, K = 3
```

#### Execution:
1. Calculate \( 3^3 = 27 \).
2. Start the loop:
   - **Iteration 1:**
     - `power = 27`, `ans = 7`, `i = 1`
   - **Iteration 2:**
     - `power = 2`, `ans = 2`, `i = 2`
   - Loop ends because `power = 0`.

#### Output:
```
0
```

---

### **Why It Works**
- The loop processes each digit of \( A^B \) from right to left.
- The `return` statement stops execution as soon as the \( K \)-th digit is found.
- If the loop finishes without finding the \( K \)-th digit, it returns `0`.

---

