# 🔁 DILUTION.RATIO

🔹 **Description**:  
This function calculates the **dilution ratio** based on the mass of water and the mass of solid.

---

## 📥 Syntax

```excel
=DILUTION.RATIO(w, s)
```

---

## 🧾 Parameters

| Parameter     | Type    | Description                            |
|---------------|---------|----------------------------------------|
| `w` (Water)   | Double  | The mass of water (e.g., in kilograms) |
| `s` (Solid)   | Double  | The mass of solid (e.g., in kilograms) |

---

## 🧮 Formula

$$
\text{Dilution Ratio} = \frac{w}{s}
$$

Where:  
- `w` = mass of water  
- `s` = mass of solid  

---

## 💡 Example

Calculate the dilution ratio if the mass of water is **900 kg** and the mass of solid is **300 kg**:

```excel
=DILUTION.RATIO(900, 300)
```

**Result**: `3.0`

---

## 📝 Notes

- Ensure that `s` (mass of solid) is greater than 0 to avoid division by zero.
- The function will return `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`SOLIDPERCENT.TO.DILUTION.RATIO`](./SolidPercent2DilutionRatio.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16