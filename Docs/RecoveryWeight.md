# 🔁 RECOVERY.WEIGHT

🔹 **Description**:  
The term "**recovery**" refers to the percentage of the total mineral present in the ore that is extracted into the concentrate. This function calculates the recovery using the grade and weight of both the **concentrate** and the **feed**.

---

## 📥 Syntax

```excel
=RECOVERY.WEIGHT(C, c, F, f)
```

---

## 🧾 Parameters

| Parameter                | Type   | Description                                                                 |
|---------------------------|--------|-----------------------------------------------------------------------------|
| `C` (Weight of Concentrate) | Double | The total mass of the concentrate.                                          |
| `c` (Grade of Concentrate)  | Double | The average grade of the concentrate.                                       |
| `F` (Weight of Feed)        | Double | The total mass of the feed.                                                 |
| `f` (Grade of Feed)         | Double | The average grade of the feed.                                              |

---

## 🧮 Formula

The recovery is calculated using the following formula:

$$
\text{Recovery (\%)} = \frac{C \cdot c}{F \cdot f}
$$

Where:  
- \( C \): Total mass of the concentrate.  
- \( c \): Average grade of the concentrate.  
- \( F \): Total mass of the feed.  
- \( f \): Average grade of the feed.  

---

## 💡 Example

### Example 1:
Calculate the recovery for the following parameters:  
- Weight of concentrate: **50 tons**  
- Grade of concentrate: **30% (0.30)**  
- Weight of feed: **200 tons**  
- Grade of feed: **10% (0.10)**

```excel
=RECOVERY.WEIGHT(50, 0.30, 200, 0.10)
```

**Result**: `0.75` (or 75% recovery)

---

## 📝 Notes

- Ensure that the grades (`c` and `f`) are expressed as decimals (e.g., 30% as 0.30).
- The result is a decimal value. Multiply by 100 to express it as a percentage.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- N/A  

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17