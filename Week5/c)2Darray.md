
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

✅ Done! Every cell of the 2D array is filled.

---


Do you want me to do that?
