
```java
public class Even {
    public static void main(String[] args) {
        // Step 1: Declare and initialize the array of numbers
        int nums[] = {12, 345, 2, 6, 7896};

        // Step 2: Call findNumbers method to count numbers with even digits
        int evencount = findNumbers(nums);

        // Step 3: Print the result
        System.out.println(evencount); // Output: 3
    }

    // Method to count how many numbers have even number of digits
    public static int findNumbers(int[] nums) {
        int count = 0; // Initialize counter

        // Loop through each number in the array
        for (int no : nums) {
            // Check if the number has even digits
            if (isEven(no)) {
                count++; // If yes, increment the counter
            }
        }

        return count; // Return total count of numbers with even digits
    }

    // Method to check if a number has an even number of digits
    public static boolean isEven(int no) {
        int ans = counts(no); // Count digits of the number

        // Check if the number of digits is even
        if (ans % 2 == 0) {
            return true;
        }
        return false;
    }

    // Method to count the number of digits in a number
    public static int counts(int no) {
        // Handle negative numbers
        if (no < 0) {
            no = -no; // Make it positive
        }

        // Special case: 0 has 1 digit
        if (no == 0) {
            return 1;
        }

        int count = 0; // Initialize digit counter

        // Count digits by dividing the number by 10 repeatedly
        while (no > 0) {
            count++;
            no = no / 10; // Remove last digit
        }

        return count; // Return the total number of digits
    }
}
```

---

### Step-by-step flow:

1. **Main method**

   * `nums` array has `{12, 345, 2, 6, 7896}`.
   * `findNumbers(nums)` is called to count numbers with **even digits**.

2. **`findNumbers` method**

   * Loops through each number in `nums`.
   * Calls `isEven(no)` to check if the number of digits is even.
   * Increments `count` for every number that passes the check.

3. **`isEven` method**

   * Calls `counts(no)` to get the number of digits.
   * Returns `true` if the number of digits is even.

4. **`counts` method**

   * Converts negative numbers to positive.
   * Special case for 0 (1 digit).
   * Loops and divides by 10 to count digits.

5. **Back in `main`**

   * The returned `evencount` is printed → `3` (numbers with even digits: `12`, `2`, `7896`).

---

