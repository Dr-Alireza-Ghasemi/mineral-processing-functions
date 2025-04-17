# 🔁 ENRICHMENT.RATIO

🔹 **Description**:  
This function calculates the **enrichment ratio**, which is the ratio of the grade of the concentrate to the grade of the feed.

---

## 📥 Syntax

```excel
=ENRICHMENT.RATIO(c, f)
```

---

## 🧾 Parameters

| Parameter                | Type   | Description                                                                 |
|---------------------------|--------|-----------------------------------------------------------------------------|
| `c` (Grade of Concentrate) | Double | The grade of the concentrate.                                               |
| `f` (Grade of Feed)        | Double | The grade of the feed.                                                      |

---

## 🧮 Formula

The enrichment ratio is calculated using the following formula:

$$
\text{Enrichment Ratio} = \frac{c}{f}
$$

Where:  
- \( c \): Grade of the concentrate.  
- \( f \): Grade of the feed.  

---

## 💡 Example

### Example 1:
Calculate the enrichment ratio for the following parameters:  
- Grade of concentrate (\( c \)): **30% (0.30)**  
- Grade of feed (\( f \)): **10% (0.10)**

```excel
=ENRICHMENT.RATIO(0.30, 0.10)
```

**Result**: `3`

---

## 📝 Notes

- Ensure that the grades (`c` and `f`) are expressed as decimals (e.g., 30% as 0.30).
- The result is a decimal value. Multiply by 100 to express it as a percentage if needed.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`CONCENTRATION.RATIO`](./ConcentrationRatio.md)
- [`RECOVERY.GRADE`](./RecoveryGrade.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17