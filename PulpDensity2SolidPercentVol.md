# 🔁 PULPDENSITY.TO.VOL.SOLIDPERCENT

🔹 **Description**:  
This function converts **pulp density** to **volume solid percent** using the solid density.

---

## 📥 Syntax

```excel
=PULPDENSITY.TO.VOL.SOLIDPERCENT(D, S)
```

---

## 🧾 Parameters

| Parameter            | Type    | Description                                |
|----------------------|---------|--------------------------------------------|
| `D` (Pulp Density)   | Double  | The pulp density in **t/m³** (e.g., 1.5)   |
| `S` (Solid Density)  | Double  | The solid density in **t/m³** (e.g., 2.7)  |

---

## 🧮 Formula

This function internally uses two helper functions:  
1. **`PulpDensity2SolidPercent`**: Converts pulp density to mass solid percent.  
2. **`SolidPercentMass2Vol`**: Converts mass solid percent to volume solid percent.

---

## 💡 Example

Convert **1.5 t/m³** pulp density to volume solid percent with a solid density of **2.7 t/m³**:

```excel
=PULPDENSITY.TO.VOL.SOLIDPERCENT(1.5, 2.7)
```

---

## 📝 Notes

- Ensure that `D` (pulp density) is less than the solid density `S`.
- The function also internally checks for user authentication and returns `-1` if authentication fails.

---

📌 **Related Functions**:
- [`SOLIDPERCENT.MASS.TO.VOL`](./SolidPercentMass2Vol.md)
- [`PULPDENSITY.TO.MASS.SOLIDPERCENT`](./PulpDensity2SolidPercent.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16