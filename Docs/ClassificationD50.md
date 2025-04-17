# 🔁 CLASSIFICATION.D50

🔹 **Description**:  
This function calculates the **D50** of a size distribution, which is the particle size at which 50% of the material passes through.

---

## 📥 Syntax

```excel
=CLASSIFICATION.D50(s, m)
```

---

## 🧾 Parameters

| Parameter              | Type      | Description                                                                 |
|-------------------------|-----------|-----------------------------------------------------------------------------|
| `s` (Size Array)        | Double[]  | An array of sieve sizes (e.g., [100, 80, 60, 40, 20]).                      |
| `m` (Cumulative Passing Array) | Double[] | An array of cumulative passing percentages corresponding to the sieve sizes (e.g., [95, 85, 65, 40, 20]). |

---

## 🧮 Formula

The function calculates the **D50** using the following logic:

### Step 1: Find the Index Where Cumulative Passing < 50%
The algorithm iterates through the cumulative passing array (`m`) to locate the first index where the value is less than 50%.  

### Step 2: Linear Interpolation
If the **D50** value falls between two sieve sizes, the function interpolates between the sizes to find the exact value:

$$
D50 = s[c - 1] - \frac{(s[c] - s[c - 1])}{(m[c] - m[c - 1])} \times (m[c - 1] - 50)
$$

Where:
- `s[c - 1]` and `s[c]` are the sieve sizes before and after the 50% cumulative passing point.
- `m[c - 1]` and `m[c]` are the corresponding cumulative passing percentages.

### Step 3: Edge Case Handling
If all cumulative passing values are above 50%, the function returns the largest sieve size in the array.

---

## 💡 Example

### Example 1:
Calculate the **D50** for the following size distribution:  
- Sieve Sizes: **[100, 80, 60, 40, 20]**  
- Cumulative Passing: **[95, 85, 65, 40, 20]**

```excel
=CLASSIFICATION.D50({100, 80, 60, 40, 20}, {95, 85, 65, 40, 20})
```

**Result**: `53.33 µm` (Interpolated value)

### Example 2:
Calculate the **D50** for the following size distribution:  
- Sieve Sizes: **[200, 150, 100, 50]**  
- Cumulative Passing: **[90, 70, 50, 30]**

```excel
=CLASSIFICATION.D50({200, 150, 100, 50}, {90, 70, 50, 30})
```

**Result**: `100 µm`

---

## 📝 Notes

- Ensure the `Size Array` is sorted in descending order.
- The `Cumulative Passing Array` must correspond to the sieve sizes in `Size Array`.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`PARTICLE.SIZE.DISTRIBUTION`](./ParticleSizeDistribution.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17