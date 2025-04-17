# 🔁 SEPARATION.EFFICIENCY.M

🔹 **Description**:  
Separation Efficiency combines **recovery** and **concentrate grade** into a single index, defining the metallurgical efficiency of the separation.

---

## 📥 Syntax

```excel
=SEPARATION.EFFICIENCY.M(C, c, m, F, f)
```

---

## 🧾 Parameters

| Parameter               | Type   | Description                                                                 |
|--------------------------|--------|-----------------------------------------------------------------------------|
| `C` (Weight of Concentrate) | Double | The weight of the concentrate.                                              |
| `c` (Grade of Concentrate)  | Double | The grade of the concentrate.                                               |
| `m` (Grade of Mineral)      | Double | The grade of the mineral.                                                   |
| `F` (Weight of Feed)        | Double | The weight of the feed.                                                     |
| `f` (Grade of Feed)         | Double | The grade of the feed.                                                      |

---

## 🧮 Formula

The separation efficiency is calculated using the following formula:

$$
\text{Separation Efficiency (\%)} = \frac{C \cdot m \cdot (c - f)}{F \cdot f \cdot (m - f)}
$$

Where:  
- \( C \): Weight of concentrate.  
- \( c \): Grade of concentrate.  
- \( m \): Grade of mineral.  
- \( F \): Weight of feed.  
- \( f \): Grade of feed.  

---

## 💡 Example

### Example 1:
Calculate the separation efficiency for the following parameters:  
- Weight of concentrate (\( C \)): **50 tons**  
- Grade of concentrate (\( c \)): **30% (0.30)**  
- Grade of mineral (\( m \)): **70% (0.70)**  
- Weight of feed (\( F \)): **200 tons**  
- Grade of feed (\( f \)): **10% (0.10)**

```excel
=SEPARATION.EFFICIENCY.M(50, 0.30, 0.70, 200, 0.10)
```

**Result**: `0.2143` (or 21.43% efficiency)

---

## 📝 Notes

- Ensure that the grades (`c`, `m`, and `f`) are expressed as decimals (e.g., 30% as 0.30).
- The result is a decimal value. Multiply by 100 to express it as a percentage.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`RECOVERY.WEIGHT`](./RecoveryWeight.md)
- [`RECOVERY.GRADE`](./RecoveryGrade.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17