
### Question:
Write a Java program to print a series of asterisks (`*`) in increasing order, separated by spaces. Each term contains as many asterisks as its position.  

**Example:**
- Input: `N = 3`  
- Output: `* ** ***`

---

### Code:
```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner scan = new Scanner(System.in);
    int N = scan.nextInt();

    for (int i = 1; i <= N; i++) {
      for (int j = 1; j <= i; j++) {
        System.out.print("*");
      }
      System.out.print(" ");
    }
  }
}
```
### Explanation:

1. **Input:**  
   - Read `N`, which is the number of terms to print.

2. **Outer Loop (`i`):**  
   - Runs from `1` to `N`.  
   - Controls the number of groups of asterisks to print.

3. **Inner Loop (`j`):**  
   - Runs from `1` to `i`.  
   - Prints `i` asterisks in each group.

4. **Space:**  
   - After printing each group of asterisks, a space is added to separate the groups.

---

**Example Walkthrough (N = 3):**  
- For `i = 1`, print `*`.  
- For `i = 2`, print `**`.  
- For `i = 3`, print `***`.  
- Add a space after each group.  

**Output:**  
```
* ** ***
```


### Question 2: Print a Right-Angled Number Triangle

**Problem Statement**:  
Write a program to print a right-angled number triangle pattern. For a given input \(N\), the first row should contain numbers from 1 to \(N\), the second row from 1 to \(N-1\), and so on until the last row contains only the number 1.

---

### Code:
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        int N = 4; // You can change N to any desired value
        for (int i = 1; i <= N; i++) {
            for (int j = 1; j <= N - i + 1; j++) {
                System.out.print(j);
            }
            System.out.println(""); // Move to the next line after each row
        }
    }
}
```

---

### Output (For N = 4):
```
1234
123
12
1
```

---

### Explanation:
1. **Outer Loop** (`for (int i = 1; i <= N; i++)`): Controls the number of rows. The value of \(i\) starts at 1 and increments up to \(N\).
2. **Inner Loop** (`for (int j = 1; j <= N - i + 1; j++)`): Prints numbers from 1 to \(N - i + 1\) for each row. As \(i\) increases, the number of columns decreases.
3. **Line Break** (`System.out.println("")`): Moves to the next line after printing each row.


