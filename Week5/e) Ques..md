*SWAPPING ARRAY ELEMENTS*

```java
import java.util.*;

public class array {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read size of array
        int n = sc.nextInt();
        int[] arr = new int[n];

        // Get array elements from user
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        // Print original array
        System.out.println("Original array: " + Arrays.toString(arr));

        // Swap elements at index 1 and 2
        swap(arr, 1, 2);

        // Print array after swap
        System.out.println("After swap: " + Arrays.toString(arr));
    }

    // Method to swap two elements in the array
    static void swap(int[] arr, int index1, int index2) {
        int temp = arr[index1];
        arr[index1] = arr[index2];
        arr[index2] = temp;
    }
}
```

---

### 1️⃣ Example of what you’re suggesting

```java
int[] index1 = {1};
int[] index2 = {4};

int temp = index1[0];
index1[0] = index2[0];
index2[0] = temp;
```

* ✅ This will swap the **values inside the temporary `index1` and `index2` arrays**.
* ❌ It **does NOT swap elements in your original array** `arr` unless you then use these indices to modify `arr`:

```java
arr[index1[0]] = ...  // you’d still need to access arr
```

---

### 2️⃣ Why your original idea doesn’t work directly

In your original swap attempt:

```java
static void swap(int[] arr, int index1, int index2){
    int temp = index1;
    index1 = index2;
    index2 = temp;
}
```

* `index1` and `index2` are just integers — not arrays.
* Swapping `index1` and `index2` **only changes the numbers in those variables**, nothing in `arr`.

Even if you made them arrays:

```java
int[] index1 = {1}, index2 = {2};
```

* Swapping `index1[0]` and `index2[0]` **only swaps the values in these small arrays**, still **doesn’t touch `arr`**.
* You’d still need:

```java
int temp = arr[index1[0]];
arr[index1[0]] = arr[index2[0]];
arr[index2[0]] = temp;
```

---

### ✅ TL;DR

* You **can** use `index1[0]` if `index1` is an array of length 1.
* But it **does not automatically swap elements in `arr`** — you still have to use `arr[index1[0]]` and `arr[index2[0]]` to modify the original array.
* Swapping just the indices themselves never affects the array.

---

---

### 🧾 **File name:** `MaxValueInArray.java`

```java
/*
 * Program: Find Maximum Value in an Array
 * Description:
 *   This Java program takes the size of an array and its elements as input,
 *   then finds and prints the maximum value from the array.
 *
 * Steps:
 *   1. Take input for array size (n).
 *   2. Store n elements in the array.
 *   3. Print the array using Arrays.toString().
 *   4. Call the 'max()' method to find and return the largest value.
 *   5. Display the maximum value.
 */

import java.util.*;

public class MaxValueInArray {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Input array size
        int n = sc.nextInt();
        int[] arr = new int[n];

        // Input array elements
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        // Print array elements
        System.out.println("Array: " + Arrays.toString(arr));

        // Call method and print maximum value
        System.out.println("Maximum value: " + max(arr));
    }

    // Method to find the maximum value in the array
    static int max(int[] arr) {
        int maxvalue = arr[0]; // Assume first element is max

        for (int i = 0; i < arr.length; i++) {
            if (arr[i] > maxvalue) {
                maxvalue = arr[i];
            }
        }

        return maxvalue; // Return the largest element
    }
}
```

---

### ✅ **Example Input**

```
5
1 3 23 9 18
```

### 🖥️ **Output**

```
Array: [1, 3, 23, 9, 18]
Maximum value: 23
```

---

### 💡 **Explanation (Concise for README)**

* The program reads `n` elements from the user and stores them in an array.
* It then iterates through the array to compare each element with the current maximum.
* If a larger value is found, it updates `maxvalue`.
* Finally, it returns and prints the maximum number.

---

