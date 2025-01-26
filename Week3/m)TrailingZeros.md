
---

### **Problem Statement**

**Find the number of trailing zeroes in \( N! \).**

- \( N! \) (factorial of \( N \)) is the product of all integers from 1 to \( N \).  
- Trailing zeroes in \( N! \) are caused by factors of \( 10 = 2 \times 5 \).  
- Since there are always more factors of \( 2 \) than \( 5 \), the number of trailing zeroes is determined by the number of factors of \( 5 \).

---

### **Program**

Here’s the complete program:

```java
class Solution {
    public int trailingZeroes(int N) {
        int count = 0; // Initialize the count of trailing zeroes

        // Count factors of 5, 25, 125, ...
        for (int i = 5; i <= N; i *= 5) {
            count += N / i; // Add the number of multiples of i (current power of 5)
        }

        return count; // Return the total trailing zeroes
    }
}
```

---

### **Explanation of the Code**

1. **Initialization:**
   - We initialize `count = 0` to store the number of trailing zeroes.
   
2. **Iterative Loop:**
   - The loop starts with `i = 5` (the first power of 5) and multiplies \( i \) by 5 in each step to check higher powers of \( 5 \) (e.g., \( 5, 25, 125, \dots \)).
   - In each iteration:
     - \( N / i \): Counts how many numbers in \( 1 \) to \( N \) are divisible by \( i \).
     - Add this to `count`.

3. **Stopping Condition:**
   - The loop stops when \( i > N \) because there are no more multiples of \( i \) within \( N \).

4. **Return the Result:**
   - Finally, the function returns `count`, which holds the total number of trailing zeroes in \( N! \).

---

### **How It Works**

Let’s go through an example.

#### Example: \( N = 100 \)

1. **First Power of 5 (\( i = 5 \)):**
   - \( 100 / 5 = 20 \): There are 20 numbers divisible by \( 5 \) (e.g., \( 5, 10, 15, ..., 100 \)).
   - These contribute 20 factors of \( 5 \).

2. **Second Power of 5 (\( i = 25 \)):**
   - \( 100 / 25 = 4 \): There are 4 numbers divisible by \( 25 \) (e.g., \( 25, 50, 75, 100 \)).
   - These contribute 4 extra factors of \( 5 \).

3. **Third Power of 5 (\( i = 125 \)):**
   - \( 100 / 125 = 0 \): There are no numbers divisible by \( 125 \) in \( 1 \) to \( 100 \).

#### Total Trailing Zeroes:
- \( 20 + 4 + 0 = 24 \).

So, \( 100! \) has **24 trailing zeroes**.

---

### **Output for Different Inputs**

| **Input \( N \)** | **Calculation**                 | **Trailing Zeroes** |
|--------------------|---------------------------------|---------------------|
| \( N = 10 \)       | \( 10/5 = 2 \)                 | \( 2 \)             |
| \( N = 25 \)       | \( 25/5 = 5, 25/25 = 1 \)      | \( 6 \)             |
| \( N = 50 \)       | \( 50/5 = 10, 50/25 = 2 \)     | \( 12 \)            |
| \( N = 100 \)      | \( 100/5 = 20, 100/25 = 4 \)   | \( 24 \)            |

---

### **Complexity Analysis**

1. **Time Complexity: \( O(\log_5 N) \):**
   - The loop runs for each power of \( 5 \) (e.g., \( 5, 25, 125 \)), which grows logarithmically.
   
2. **Space Complexity: \( O(1) \):**
   - Only a single variable `count` is used.

---

### **Table Visualization**

Here’s how the program processes \( N = 100 \):

| **Step** | **Power of 5 (\( i \))** | **Numbers Divisible by \( i \)** | **Count Added** | **Cumulative Total** |
|----------|---------------------------|----------------------------------|-----------------|-----------------------|
| 1        | \( 5 \)                  | \( 5, 10, 15, ..., 100 \)       | \( 100 / 5 = 20 \) | \( 20 \)             |
| 2        | \( 25 \)                 | \( 25, 50, 75, 100 \)           | \( 100 / 25 = 4 \) | \( 24 \)             |
| 3        | \( 125 \)                | None                            | \( 100 / 125 = 0 \) | \( 24 \)             |

**Final Output:** \( 24 \)

---

### **Key Points**

1. Trailing zeroes come from factors of \( 10 = 2 \times 5 \).
2. Factors of \( 2 \) are abundant in \( N! \), so we only count factors of \( 5 \).
3. The total number of trailing zeroes is calculated as \( N/5 + N/25 + N/125 + \dots \).

---

