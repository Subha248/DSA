
---

## **Example 1**

Write a program in Java to find the **last digit** of a given number.

### Explanation:
The last digit of a number can be obtained by performing the modulus operation with `10`:
- For example:
  - \( 345 \% 10 = 5 \)
  - \( 9876 \% 10 = 6 \)

---

## **Program**

```java
public class Main {
    public static void main(String[] args) {
        int number = 345345; // Input number
        int lastDigit = number % 10; // Find the last digit
        System.out.println("The last digit is: " + lastDigit); // Output the result
    }
}
```

---

## **Output**

### Input:
```
345345
```

### Output:
```
The last digit is: 5
```

---

## **Explanation**

1. **Input Number:** 
   - The number `345345` is stored in the variable `number`.

2. **Finding the Last Digit:**
   - Using `number % 10`, we calculate the remainder when the number is divided by 10. This remainder is the last digit of the number.
   - For `345345`, \( 345345 \% 10 = 5 \).

3. **Output the Result:**
   - `System.out.println("The last digit is: " + lastDigit);` prints the last digit to the console.

## **Working Table**

| **Input (n)** | **`n % 10` (Last Digit)** | **Output** |
|---------------|---------------------------|------------|
| 1234          | 4                         | 4          |
| 98765         | 5                         | 5          |
| 1000          | 0                         | 0          |
| 7             | 7                         | 7          |

---
---


## **Question 2**

Write a program in Java to reverse the digits of a given number using a `while` loop. For example, if the input is `1234`, the program should output `4321`.

---

## **Program**

```java
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

        System.out.println("Enter a number:");
        int n = scan.nextInt(); // Read the input number

        while (n > 0) { // Loop to reverse the digits
            int l = n % 10; // Get the last digit
            System.out.print(l); // Print the digit
            n = n / 10; // Remove the last digit from the number
        }
    }
}
```

---

## **Output**

### Example 1:
**Input:**
```
1234
```

**Output:**
```
4321
```

---

### Example 2:
**Input:**
```
98765
```

**Output:**
```
56789
```

---

## **Explanation**

1. **Input Handling:**
   - The program reads an integer `n` from the user using `Scanner`.

2. **Reversing Logic:**
   - Inside the `while` loop:
     - **`n % 10`**:
       - Extracts the last digit of the number.
       - Example: For `1234`, `1234 % 10 = 4`.
     - **`System.out.print(l)`**:
       - Prints the extracted digit.
     - **`n = n / 10`**:
       - Removes the last digit of the number by dividing it by `10`.
       - Example: For `1234`, `1234 / 10 = 123`.

3. **Loop Execution:**
   - The loop continues until `n` becomes `0`.

4. **Output:**
   - The digits are printed in reverse order because the last digit is extracted and printed first, followed by the remaining digits.

---

## **Working Table**

| **Input (n)** | **`n % 10` (Last Digit)** | **Print** | **`n / 10` (Remaining Number)** |
|---------------|---------------------------|-----------|----------------------------------|
| 1234          | 4                         | 4         | 123                              |
| 123           | 3                         | 3         | 12                               |
| 12            | 2                         | 2         | 1                                |
| 1             | 1                         | 1         | 0                                |

---

## **Key Points**

1. **Logic for Reversal:**
   - By repeatedly extracting the last digit and removing it from the number, the digits are printed in reverse order.

2. **Termination Condition:**
   - The loop stops when `n` becomes `0`, as there are no more digits to process.

3. **Scalability:**
   - This program works for any positive integer input.

---



