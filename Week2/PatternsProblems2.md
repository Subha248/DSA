### Question 1:

**Print a Diamond Pattern**

Write a program that takes an integer input \( n \) and prints a diamond pattern of stars (\(*\)). The diamond should have \( n - 1 \) rows in the upper part and \( n \) rows in the lower part. The stars should be aligned symmetrically.

---

### Input:
An integer \( n \) representing the number of rows for the lower part of the diamond, plus one for the middle row.

### Output:
A diamond pattern of stars.

---

### Example:

**Input:**
```
5
```

**Output:**
```
    * 
   *** 
  ***** 
 ******* 
********* 
 ******* 
  ***** 
   *** 
    * 
```

---

### Code:

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();

        // Upper part of the diamond
        for (int i = 1; i <= n - 1; i++) {
            for (int j = 1; j <= n - i; j++) {
                System.out.print(" ");
            }
            for (int j = 1; j <= 2 * i - 1; j++) {
                System.out.print("*");
            }
            System.out.println(" ");
        }

        // Lower part of the diamond
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i - 1; j++) {
                System.out.print(" ");
            }
            for (int j = 1; j <= (2 * n) - (2 * i - 1); j++) {
                System.out.print("*");
            }
            System.out.println(" ");
        }
    }
}
```

---

### Explanation:

1. **Input**: 
   - The user enters \( n \), which defines the number of rows in the lower part of the diamond and one additional row for the middle.

2. **Upper Part of the Diamond**:
   - Controlled by the first loop (`i` from 1 to \( n - 1 \)).
   - For each row:
     - Spaces: \( n - i \) spaces are printed at the beginning.
     - Stars: \( 2 \times i - 1 \) stars are printed to form the increasing triangle.

3. **Lower Part of the Diamond**:
   - Controlled by the second loop (`i` from 1 to \( n \)).
   - For each row:
     - Spaces: \( i - 1 \) spaces are printed at the beginning.
     - Stars: \( (2 \times n) - (2 \times i - 1) \) stars are printed to form the decreasing triangle.

---

### Walkthrough for \( n = 5 \):

**Upper Part**:
- Row 1: \( n - 1 = 4 \) spaces, \( 1 \) star → `    *`
- Row 2: \( n - 2 = 3 \) spaces, \( 3 \) stars → `   ***`
- Row 3: \( n - 3 = 2 \) spaces, \( 5 \) stars → `  *****`
- Row 4: \( n - 4 = 1 \) space, \( 7 \) stars → ` *******`

**Lower Part**:
- Row 1: \( 0 \) spaces, \( 9 \) stars → `*********`
- Row 2: \( 1 \) space, \( 7 \) stars → ` *******`
- Row 3: \( 2 \) spaces, \( 5 \) stars → `  *****`
- Row 4: \( 3 \) spaces, \( 3 \) stars → `   ***`
- Row 5: \( 4 \) spaces, \( 1 \) star → `    *`

---

### Output for \( n = 5 \):

```
    * 
   *** 
  ***** 
 ******* 
********* 
 ******* 
  ***** 
   *** 
    * 
```

