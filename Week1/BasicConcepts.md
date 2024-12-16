
### Problem 1

Write a program that takes an integer, then a string, then a char from the user and prints them in the screen.

``` plaintext
Input:  2 Name y

Expected Output:

2

Name

y
```


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

### Prob 2: Write a program to check whether a triangle can be formed with the given values for the angles.
``` plaintext
If sum of angles is equal to 180, then triangle can be formed, else it can't be formed.

Input: 45 45 45

Expected Output: 

Triangle cannot be formed

Explanation -> We are getting 3 inputs, that is three angles of triangle, but here the sum of three angles that is 45+45+45 is not equal to 180 so Triangle cannot be formed is the output
```

Here’s the program to check whether a triangle can be formed based on the given angles:

```java
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int angle1 = scan.nextInt();
        int angle2 = scan.nextInt();
        int angle3 = scan.nextInt();

        if (angle1 + angle2 + angle3 == 180) {
            System.out.println("Triangle can be formed");
        } else {
            System.out.println("Triangle cannot be formed");
        }
    }
}
```

---

### Explanation:

1. **Input**:
   - The program takes three integers as input (angles of a triangle).

2. **Condition**:
   - It checks whether the sum of the three angles is equal to `180`.

3. **Output**:
   - If the sum is `180`, the program prints `"Triangle can be formed"`.
   - Otherwise, it prints `"Triangle cannot be formed"`.

---

### Input/Output Example:

#### Input:
```
45 45 45
```

#### Output:
```
Triangle cannot be formed
```

---

#### Input:
```
60 60 60
```

#### Output:
```
Triangle can be formed
```

This code meets the requirements for the problem. Let me know if you have any further questions! 😊

