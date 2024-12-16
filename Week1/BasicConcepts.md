/*Write a program that takes an integer, then a string, then a char from the user and prints them in the screen.


Input:  2 Name y

Expected Output:

2

Name

y  */ 


``` java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

       
        int num = scan.nextInt();
        scan.nextLine(); // Consume leftover newline character

       
        String a = scan.nextLine();

       
        char y = scan.next().charAt(0);

        
        System.out.println(num);
        System.out.println(a);
        System.out.println(y);
    }
}

```

1. **Import Scanner**: Allows user input.

2. **Create Scanner Object**:
   ```java
   Scanner scan = new Scanner(System.in);
   ```

3. **Input Reading**:
   - `scan.nextInt()` → Reads an integer and stores in `num`.
   - `scan.nextLine()` → Clears leftover newline from `nextInt()`.
   - `scan.nextLine()` → Reads a full line of text into `a`.
   - `scan.next().charAt(0)` → Reads a single character into `y`.

4. **Output**:
   Prints `num`, `a`, and `y`.

---

### Example:

#### Input:
```
5
Hello
T
```

#### Output:
```
5
Hello
T
```
