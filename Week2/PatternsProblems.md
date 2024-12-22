
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

---

### Example:
**Input:**  
```
N = 4
```

**Output:**  
```
* ** *** ****
```
