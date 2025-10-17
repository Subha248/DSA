
---

### Example Run:

**Input:**

```
Enter a number: 153
```

**Step-by-step inside the program:**

1. `original = 153`
2. `sum = 0`

**While loop starts:**

* Last digit: `rem = 153 % 10 = 3` → `sum = 0 + 3*3*3 = 27` → `n = 153 / 10 = 15`
* Last digit: `rem = 15 % 10 = 5` → `sum = 27 + 5*5*5 = 152` → `n = 15 / 10 = 1`
* Last digit: `rem = 1 % 10 = 1` → `sum = 152 + 1*1*1 = 153` → `n = 1 / 10 = 0`

**While loop ends** (`n = 0`)

**Check:** `sum == original` → `153 == 153` → **true** ✅

---

**Output:**

```
Is Armstrong? true
```

---

### Another Example:

**Input:**

```
Enter a number: 120
```

**Steps inside the program:**

* `rem = 0` → sum = 0
* `rem = 2` → sum = 8
* `rem = 1` → sum = 9

**Check:** `sum == original` → `9 == 120` → **false** ❌

**Output:**

```
Is Armstrong? false
```

---

