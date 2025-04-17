# 🔁 CLASSIFICATION.Dx

🔹 **Description**:  
This function calculates the **Dx**, which is the particle size corresponding to a custom cumulative passing percentage in a size distribution.

---

## 📥 Syntax

```excel
=CLASSIFICATION.Dx(xx, s, m)
```

---

## 🧾 Parameters

| Parameter              | Type      | Description                                                                 |
|-------------------------|-----------|-----------------------------------------------------------------------------|
| `xx` (Custom Passing Percentage) | Double   | The custom cumulative passing percentage (e.g., 75 for D75).                |
| `s` (Size Array)        | Double[]  | An array of sieve sizes (e.g., [100, 80, 60, 40, 20]).                      |
| `m` (Cumulative Passing Array) | Double[] | An array of cumulative passing percentages corresponding to the sieve sizes (e.g., [95, 85, 65, 40, 20]). |

---

## 🧮 Formula

The function calculates the **Dx** using the following logic:

### Step 1: Find the Index Where Cumulative Passing < `xx`
The algorithm iterates through the cumulative passing array (`m`) to locate the first index where the value is less than the custom passing percentage `xx`.  

### Step 2: Linear Interpolation
If the **Dx** value falls between two sieve sizes, the function interpolates between the sizes to find the exact value:

$$
Dx = s[c - 1] - \frac{(s[c] - s[c - 1])}{(m[c] - m[c - 1])} \times (m[c - 1] - xx)
$$

Where:
- `s[c - 1]` and `s[c]` are the sieve sizes before and after the custom passing percentage point.
- `m[c - 1]` and `m[c]` are the corresponding cumulative passing percentages.

### Step 3: Edge Case Handling
If all cumulative passing values are above `xx`, the function returns the largest sieve size in the array.

---

## 💡 Example

### Example 1:
Calculate the **D75** (75% passing size) for the following size distribution:  
- Sieve Sizes: **[100, 80, 60, 40, 20]**  
- Cumulative Passing: **[95, 85, 65, 40, 20]**

```excel
=CLASSIFICATION.Dx(75, {100, 80, 60, 40, 20}, {95, 85, 65, 40, 20})
```

**Result**: `70.00 µm` (Interpolated value)

### Example 2:
Calculate the **D10** (10% passing size) for the following size distribution:  
- Sieve Sizes: **[200, 150, 100, 50]**  
- Cumulative Passing: **[90, 85, 80, 75]**

```excel
=CLASSIFICATION.Dx(10, {200, 150, 100, 50}, {90, 85, 80, 75})
```

**Result**: `200 µm`

---

## 📝 Notes

- Ensure the `Size Array` is sorted in descending order.
- The `Cumulative Passing Array` must correspond to the sieve sizes in `Size Array`.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`CLASSIFICATION.D50`](./ClassificationD50.md)
- [`CLASSIFICATION.D80`](./ClassificationD80.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17