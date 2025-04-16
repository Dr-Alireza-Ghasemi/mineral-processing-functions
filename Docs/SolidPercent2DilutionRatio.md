# 🔁 SOLIDPERCENT.TO.DILUTION.RATIO

🔹 **Description**:  
This function converts **mass solid percent** to **dilution ratio**.

---

## 📥 Syntax

```excel
=SOLIDPERCENT.TO.DILUTION.RATIO(sp)
```

---

## 🧾 Parameters

| Parameter            | Type    | Description                                |
|----------------------|---------|--------------------------------------------|
| `sp` (Solid Percent) | Double  | The mass solid percent (e.g., 45 for 45%)  |

---

## 🧮 Formula

$$
\text{Dilution Ratio} = \frac{100.0 - sp}{sp}
$$

Where:  
- `sp` = mass solid percent  

---

## 💡 Example

Convert **45%** mass solid percent to dilution ratio:

```excel
=SOLIDPERCENT.TO.DILUTION.RATIO(45)
```

**Result**: `1.22`

---

## 📝 Notes

- Ensure `sp` is between 0 and 100.
- The function will return `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`SOLIDPERCENT.MASS.TO.VOL`](./SolidPercentMass2Vol.md)
- [`SOLIDPERCENT.MASS.TO.PULPDENSITY`](./SolidPercent2PulpDensity.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16