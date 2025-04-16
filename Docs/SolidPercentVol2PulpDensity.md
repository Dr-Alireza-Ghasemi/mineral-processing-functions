# 🔁 SOLIDPERCENT.VOL.TO.PULPDENSITY

🔹 **Description**:  
This function converts **volume solid percent** to **pulp density** using the solid density.

---

## 📥 Syntax

```excel
=SOLIDPERCENT.VOL.TO.PULPDENSITY(sp, S)
```

---

## 🧾 Parameters

| Parameter            | Type    | Description                                |
|----------------------|---------|--------------------------------------------|
| `sp` (Solid Percent) | Double  | The volume solid percent (e.g., 20 for 20%)|
| `S` (Solid Density)  | Double  | The solid density in **t/m³** (e.g., 2.7)  |

---

## 🧮 Formula

This function internally performs the following steps:
1. Converts volume solid percent (`sp`) to mass solid percent (`msp`) using **`SolidPercentVol2Mass`**.
2. Calculates the pulp density using:

$$
\text{Pulp Density} = \frac{100.0}{\frac{msp}{S} + (100.0 - msp)}
$$

Where:  
- `sp` = volume solid percent  
- `msp` = mass solid percent derived from `sp`  
- `S` = solid density in t/m³  

---

## 💡 Example

Convert **20%** volume solid percent to pulp density with a solid density of **2.7 t/m³**:

```excel
=SOLIDPERCENT.VOL.TO.PULPDENSITY(20, 2.7)
```

---

## 📝 Notes

- Ensure `sp` is between 0 and 100.
- The function will return `-1` if user authentication fails.
- This function relies on the helper function **`SolidPercentVol2Mass`** for intermediate calculations.

---

📌 **Related Functions**:
- [`SOLIDPERCENT.MASS.TO.PULPDENSITY`](./SolidPercent2PulpDensity.md)
- [`PULPDENSITY.TO.VOL.SOLIDPERCENT`](./PulpDensity2SolidPercentVol.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16