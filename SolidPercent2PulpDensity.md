# 🔁 SOLIDPERCENT.MASS.TO.PULPDENSITY

🔹 **Description**:  
This function converts **mass solid percent** to **pulp density** using the solid density.

---

## 📥 Syntax

```excel
=SOLIDPERCENT.MASS.TO.PULPDENSITY(sp, S)
```

---

## 🧾 Parameters

| Parameter            | Type    | Description                                |
|----------------------|---------|--------------------------------------------|
| `sp` (Solid Percent) | Double  | The mass solid percent (e.g., 45 for 45%)  |
| `S` (Solid Density)  | Double  | The solid density in **t/m³** (e.g., 2.7)  |

---

## 🧮 Formula

$$
\text{Pulp Density} = \frac{100.0}{\frac{sp}{S} + (100.0 - sp)}
$$

Where:  
- `sp` = mass solid percent  
- `S` = solid density in t/m³  

---

## 💡 Example

Convert **45%** mass solid percent to pulp density with a solid density of **2.7 t/m³**:

```excel
=SOLIDPERCENT.MASS.TO.PULPDENSITY(45, 2.7)
```

**Result**: `1.56`

---

## 📝 Notes

- Ensure `sp` is between 0 and 100.
- The function will return `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`SOLIDPERCENT.MASS.TO.VOL`](./SolidPercentMass2Vol.md)
- [`PULPDENSITY.TO.VOL.SOLIDPERCENT`](./PulpDensity2SolidPercentVol.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16