# 🔁 RECOVERY.GRADE

🔹 **Description**:  
The term "**recovery**" refers to the percentage of the total mineral present in the ore that is extracted into the concentrate. This function calculates the recovery based on the grades of the concentrate, tail, and feed.

---

## 📥 Syntax

```excel
=RECOVERY.GRADE(c, t, f)
```

---

## 🧾 Parameters

| Parameter                | Type   | Description                                                                 |
|---------------------------|--------|-----------------------------------------------------------------------------|
| `c` (Grade of Concentrate) | Double | The grade of the concentrate.                                               |
| `t` (Grade of Tail)        | Double | The grade of the tail.                                                      |
| `f` (Grade of Feed)        | Double | The grade of the feed.                                                      |

---

## 🧮 Formula

The recovery percentage is calculated using the following formula:

$$
\text{Recovery (\%)} = \frac{c \cdot (f - t)}{f \cdot (c - t)}
$$

Where:  
- \( c \): Grade of the concentrate.  
- \( t \): Grade of the tail.  
- \( f \): Grade of the feed.  

---

## 💡 Example

### Example 1:
Calculate the recovery for the following parameters:  
- Grade of concentrate (\( c \)): **30% (0.30)**  
- Grade of tail (\( t \)): **5% (0.05)**  
- Grade of feed (\( f \)): **10% (0.10)**

```excel
=RECOVERY.GRADE(0.30, 0.05, 0.10)
```

**Result**: `0.75` (or 75% recovery)

---

## 📝 Notes

- Ensure that the grades (`c`, `t`, and `f`) are expressed as decimals (e.g., 30% as 0.30).
- The result is a decimal value. Multiply by 100 to express it as a percentage.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`RECOVERY.WEIGHT`](./RecoveryWeight.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17