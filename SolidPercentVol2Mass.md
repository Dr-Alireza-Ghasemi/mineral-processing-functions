# 🔁 SOLIDPERCENT.VOL.TO.MASS

🔹 **Description**:  
This function converts **volume solid percent** to **mass solid percent** using the density of solids.

---

## 📥 Syntax

```excel
=SOLIDPERCENT.VOL.TO.MASS(sp, Rho)
```

---

## 🧾 Parameters

| Parameter            | Type    | Description                                |
|----------------------|---------|--------------------------------------------|
| `sp`                 | Double  | Solid percent by volume (e.g., 20 for 20%) |
| `Rho`                | Double  | Solid density in **t/m³** (e.g., 2.7)      |

---

## 🧮 Formula

\[
\text{Mass\%} = \frac{sp \times \rho}{sp \times \rho + (100 - sp)} \times 100
\]

Where:  
- `sp` = volume solid percent  
- `ρ` = solid density in t/m³  

---

## 💡 Example

Convert **20%** volume solid percent to mass solid percent with a solid density of **2.7 t/m³**:

```excel
=SOLIDPERCENT.VOL.TO.MASS(20, 2.7)
```

**Result**: `38.96`

---

## 📝 Notes

- Ensure `sp` is between 0 and 100.
- This is useful when working with slurry compositions and converting between volume and weight-based measurements.

---

📌 **Related Functions**:
- [`SOLIDPERCENT.MASS.TO.VOL`](./SolidPercentMass2Vol.md)
- [`SOLIDPERCENT.VOL.TO.PULPDENSITY`](./SolidPercentVol2PulpDensity.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16