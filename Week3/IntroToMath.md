
---

## **Sample 1**

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

---

