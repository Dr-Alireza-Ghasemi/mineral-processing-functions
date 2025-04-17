# 🔁 SEPARATION.EFFICIENCY

🔹 **Description**:  
Separation Efficiency combines **recovery** and **concentrate grade** into a single index, defining the metallurgical efficiency of the separation.

---

## 📥 Syntax

```excel
=SEPARATION.EFFICIENCY(c, t, f)
```

---

## 🧾 Parameters

| Parameter               | Type   | Description                                                                 |
|--------------------------|--------|-----------------------------------------------------------------------------|
| `c` (Grade of Concentrate) | Double | The grade of the concentrate.                                               |
| `t` (Grade of Tail)        | Double | The grade of the tail.                                                      |
| `f` (Grade of Feed)        | Double | The grade of the feed.                                                      |

---

## 🧮 Formula

The separation efficiency is calculated using the following formula:

$$
\text{Separation Efficiency (\\%)} = \frac{c \cdot (f - t) \cdot (c - f) \cdot (100 - t)}{f \cdot (c - t)^2 \cdot (100 - f)}
$$

Where:  
- \( c \): Grade of concentrate.  
- \( t \): Grade of tail.  
- \( f \): Grade of feed.  

---

## 💡 Example

### Example 1:
Calculate the separation efficiency for the following parameters:  
- Grade of concentrate (\( c \)): **30% (0.30)**  
- Grade of tail (\( t \)): **5% (0.05)**  
- Grade of feed (\( f \)): **10% (0.10)**

```excel
=SEPARATION.EFFICIENCY(0.30, 0.05, 0.10)
```

**Result**: `0.1875` (or 18.75% efficiency)

---

## 📝 Notes

- Ensure that the grades (`c`, `t`, and `f`) are expressed as decimals (e.g., 30% as 0.30).
- The result is a decimal value. Multiply by 100 to express it as a percentage.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`SEPARATION.EFFICIENCY.M`](./SeparationEfficiencyM.md)
- [`RECOVERY.GRADE`](./RecoveryGrade.md)
- [`RECOVERY.WEIGHT`](./RecoveryWeight.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17
