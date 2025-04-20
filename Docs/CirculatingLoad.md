# 🔁 CIRCULATINGLOAD

🔹 **Description**:  
The `CIRCULATINGLOAD` function calculates the circulating load of a grinding circuit based on the weight fractions (or percentages) in different size classes of feed, underflow, and overflow. This is essential for optimizing grinding circuit performance.

---

## 📥 Syntax

```excel
=CIRCULATINGLOAD(F, U, O)
```

---

## 🧾 Parameters

| Parameter                | Type           | Description                                                         |
|---------------------------|----------------|---------------------------------------------------------------------|
| `F` (Feed)               | Array of Doubles | Weight fraction (or %) in each size class of feed.                  |
| `U` (Underflow)          | Array of Doubles | Weight fraction (or %) in each size class of underflow.             |
| `O` (Overflow)           | Array of Doubles | Weight fraction (or %) in each size class of overflow.              |

---

## 💡 Example

### Example 1:
Calculate the circulating load for the following parameters:

| **Size Class** | **Feed (F)** | **Underflow (U)** | **Overflow (O)** |
|----------------|--------------|-------------------|------------------|
| 1             | 0.12         | 0.18             | 0.08            |
| 2             | 0.15         | 0.20             | 0.10            |
| 3             | 0.10         | 0.16             | 0.06            |

```excel
=CIRCULATINGLOAD({0.12, 0.15, 0.10}, {0.18, 0.20, 0.16}, {0.08, 0.10, 0.06})
```

**Result**: The circulating load percentage calculated from the regression slope.

---

## 📝 Notes

- Ensure that all input arrays (`F`, `U`, `O`) are of the same length.
- The function uses regression analysis to calculate the result, requiring valid numeric inputs.
- The function returns `-1` if:
  - User authentication fails.
  - Input arrays are invalid or mismatched.

---

📌 **Help Topic**:  
For more details, visit the [documentation](https://github.com/Dr-Alireza-Ghasemi/mineral-processing-functions/blob/main/Docs/CirculatingLoad.md).

---

📌 **Related Functions**:
- [`RECOVERY.GRADE`](./RecoveryGrade.md)
- [`RECOVERY.WEIGHT`](./RecoveryWeight.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-20
