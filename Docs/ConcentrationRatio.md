# 🔁 CONCENTRATION.RATIO

🔹 **Description**:  
The function calculates the **ratio of concentration**, which is the ratio between the weight of the concentrate and the weight of the feed.

---

## 📥 Syntax

```excel
=CONCENTRATION.RATIO(C, F)
```

---

## 🧾 Parameters

| Parameter                | Type   | Description                                                                 |
|---------------------------|--------|-----------------------------------------------------------------------------|
| `C` (Weight of Concentrate) | Double | The weight of the concentrate.                                              |
| `F` (Weight of Feed)        | Double | The weight of the feed.                                                     |

---

## 🧮 Formula

The ratio of concentration is calculated using the following formula:

$$
\text{Concentration Ratio} = \frac{C}{F}
$$

Where:  
- \( C \): Weight of the concentrate.  
- \( F \): Weight of the feed.  

---

## 💡 Example

### Example 1:
Calculate the concentration ratio for the following parameters:  
- Weight of concentrate (\( C \)): **50 tons**  
- Weight of feed (\( F \)): **200 tons**

```excel
=CONCENTRATION.RATIO(50, 200)
```

**Result**: `0.25`

---

## 📝 Notes

- The result is a decimal value. Multiply by 100 to express it as a percentage if needed.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`RECOVERY.WEIGHT`](./RecoveryWeight.md)
- [`RECOVERY.GRADE`](./RecoveryGrade.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17