
---

### 2D Array Loops Explained Easily

Imagine a **table**:

```
row\col | 0  1
--------+-----
0       | ?  ?
1       | ?  ?
2       | ?  ?
```

We want to fill every `?` with a number.

---

### Step 1 — Outer Loop (rows)

```java
for (int row = 0; row < 3; row++) { ... }
```

* Goes **from top to bottom**
* `row = 0 → 2`
* Each time, we move to a **new row**

---

### Step 2 — Inner Loop (columns)

```java
for (int col = 0; col < 2; col++) { ... }
```

* Goes **from left to right** inside the current row
* `col = 0 → 1`
* Each time, we move to the **next column in that row**

---

### Step 3 — Fill the value

```java
arr[row][col] = sc.nextInt();
```

* Takes input and stores it in **current row and column**

---

### Step 4 — How loops work together

Think like this:

1. `row = 0`

   * `col = 0` → fill arr[0][0]
   * `col = 1` → fill arr[0][1]
2. `row = 1`

   * `col = 0` → fill arr[1][0]
   * `col = 1` → fill arr[1][1]
3. `row = 2`

   * `col = 0` → fill arr[2][0]
   * `col = 1` → fill arr[2][1]

---

---

```java
import java.util.*;  // Import Scanner for input

public class Array2D {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in); // Create Scanner object

        // Step 1: Take array size from user
        System.out.print("Enter number of rows: ");
        int rows = in.nextInt();  // Number of rows
        System.out.print("Enter number of columns: ");
        int cols = in.nextInt();  // Number of columns

        // Step 2: Create 2D array
        int[][] arr = new int[rows][cols];

        // Step 3: Input elements
        System.out.println("Enter array elements:");
        for (int row = 0; row < rows; row++) {
            for (int col = 0; col < cols; col++) {
                arr[row][col] = in.nextInt(); // Fill each cell
            }
        }

        // Step 4: Output the array
        System.out.println("Your 2D array:");
        for (int row = 0; row < rows; row++) {
            for (int col = 0; col < cols; col++) {
                System.out.print(arr[row][col] + " "); // Print element
            }
            System.out.println(); // Move to next row
        }
    }
}
```

---

### 💡 **Explanation**

1. `rows` → number of rows
2. `cols` → number of columns
3. `arr[row][col]` → each cell in the 2D array
4. **First nested loop** → takes input row by row
5. **Second nested loop** → prints the array like a table

---

### ✅ **Example**

**Input:**

```
Enter number of rows: 2
Enter number of columns: 3
Enter array elements:
1 2 3
4 5 6
```

**Output:**

```
Your 2D array:
1 2 3
4 5 6
```

---


