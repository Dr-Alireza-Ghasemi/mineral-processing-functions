# 🔁 SOLIDPERCENT.MASS.TO.VOL

🔹 **Description**:  
This function converts **mass solid percent** to **volume solid percent** using the density of solids.

---

## 📥 Syntax

```excel
=SOLIDPERCENT.MASS.TO.VOL(sp, Rho)
```

---

## 🧾 Parameters

| Parameter            | Type    | Description                                |
|----------------------|---------|--------------------------------------------|
| `sp`                 | Double  | Solid percent by mass (e.g., 45 for 45%)   |
| `Rho`                | Double  | Solid density in **t/m³** (e.g., 2.7)      |

---

## 🧮 Formula

$$
\text{Vol\%} = \frac{\frac{sp}{\rho}}{\frac{sp}{\rho} + (100 - sp)} \times 100
$$

Where:  
- `sp` = mass solid percent  
- `ρ` = solid density in t/m³  

---

## 💡 Example

Convert **45%** mass solid percent to volume solid percent with a solid density of **2.7 t/m³**:

```excel
=SOLIDPERCENT.MASS.TO.VOL(45, 2.7)
```

**Result**: `20.12`

---

## 📝 Notes

- Make sure `sp` is between 0 and 100.
- This is useful for converting lab data to volumetric interpretations in mineral processing.
- The result is also a percentage (0–100).

---

📌 **Related Functions**:
- [`SOLIDPERCENT.VOL.TO.MASS`](./SolidPercentVol2Mass.md)
- [`PULPDENSITY.TO.VOL.SOLIDPERCENT`](./PulpDensity2SolidPercentVol.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16
