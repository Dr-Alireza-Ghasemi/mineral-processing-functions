# 🔁 CLASSIFICATION.D80

🔹 **Description**:  
This function calculates the **D80** of a size distribution, which is the particle size at which 80% of the material passes through.

---

## 📥 Syntax

```excel
=CLASSIFICATION.D80(s, m)
```

---

## 🧾 Parameters

| Parameter              | Type      | Description                                                                 |
|-------------------------|-----------|-----------------------------------------------------------------------------|
| `s` (Size Array)        | Double[]  | An array of sieve sizes (e.g., [100, 80, 60, 40, 20]).                      |
| `m` (Cumulative Passing Array) | Double[] | An array of cumulative passing percentages corresponding to the sieve sizes (e.g., [95, 85, 65, 40, 20]). |

---

## 💡 Example

### Example 1:
Calculate the **D80** for the following size distribution:  
- Sieve Sizes: **[100, 80, 60, 40, 20]**  
- Cumulative Passing: **[95, 85, 65, 40, 20]**

```excel
=CLASSIFICATION.D80({100, 80, 60, 40, 20}, {95, 85, 65, 40, 20})
```

**Result**: `68.00 µm` (Interpolated value)

### Example 2:
Calculate the **D80** for the following size distribution:  
- Sieve Sizes: **[200, 150, 100, 50]**  
- Cumulative Passing: **[90, 85, 80, 75]**

```excel
=CLASSIFICATION.D80({200, 150, 100, 50}, {90, 85, 80, 75})
```

**Result**: `100 µm`

---

## 📝 Notes

- Ensure the `Size Array` is sorted in descending order.
- The `Cumulative Passing Array` must correspond to the sieve sizes in `Size Array`.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`CLASSIFICATION.D50`](./ClassificationD50.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17
