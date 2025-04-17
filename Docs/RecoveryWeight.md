# 🔁 RECOVERY.WEIGHT

🔹 **Description**:  
The term "**recovery**" refers to the percentage of the total mineral present in the ore that is extracted into the concentrate. This function calculates the recovery based on the weight and grade of both the concentrate and the feed.

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

The recovery percentage is calculated using the following formula:

$$
\text{Recovery (\\%)} = \frac{C \cdot c}{F \cdot f} \cdot 100
$$

Where:  
- \( C \): Weight of the concentrate.  
- \( c \): Grade of the concentrate.  
- \( F \): Weight of the feed.  
- \( f \): Grade of the feed.  

---

## 💡 Example

### Example 1:
Calculate the recovery for the following parameters:  
- Weight of concentrate (\( C \)): **50 tons**  
- Grade of concentrate (\( c \)): **30% (0.30)**  
- Weight of feed (\( F \)): **200 tons**  
- Grade of feed (\( f \)): **10% (0.10)**

```excel
=RECOVERY.WEIGHT(50, 0.30, 200, 0.10)
```

**Result**: `75%`

---

## 📝 Notes

- Ensure that the grades (`c` and `f`) are expressed as decimals (e.g., 30% as 0.30).
- The result is returned as a percentage value.
- The function returns `-1` if user authentication fails.

---

📌 **Help Topic**:  
For more details, visit the [documentation](https://github.com/Dr-Alireza-Ghasemi/mineral-processing-functions/blob/main/Docs/RecoveryWeight.md).

---

📌 **Related Functions**:
- [`RECOVERY.GRADE`](./RecoveryGrade.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17
