# 🔁 PULPDENSITY.TO.MASS.SOLIDPERCENT

### 🔹 Description:
This function converts **pulp density** to **mass solid percent**, using the known **solid density**.

---

## 📥 Syntax

=PULPDENSITY.TO.MASS.SOLIDPERCENT(D, S)

---

## 📌 Parameters

| Parameter | Type   | Description                      |
|-----------|--------|----------------------------------|
| `D`       | Double | Pulp density in **t/m³**         |
| `S`       | Double | Solid density in **t/m³**        |

---

## 🧮 Formula

$$
\text{Mass \%} = \frac{100 \times S \times (D - 1)}{D \times (S - 1)}
$$

- `D`: pulp density (t/m³)
- `S`: solid density (t/m³)

---

## 💡 Example

If the pulp density is **1.35 t/m³** and the solid density is **2.7 t/m³**, then:

=PULPDENSITY.TO.MASS.SOLIDPERCENT(1.35, 2.7)

**Result**: 45.00

---

## 📝 Notes

- This formula is commonly used in mineral processing and slurry calculations.
- Ensure `D > 1` and `S > D` for valid physical conditions.
- Output is expressed in **% (percent by mass)**.

---

## 🔗 Related Functions

- [SOLIDPERCENT.MASS.TO.PULPDENSITY](./SolidPercent2PulpDensity.md)
- [PULPDENSITY.TO.VOL.SOLIDPERCENT](./PulpDensity2SolidPercentVol.md)

---

👤 Author: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16
