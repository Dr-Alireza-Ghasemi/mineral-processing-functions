# 🔁 CYCLONE.COUNT

🔹 **Description**:  
This function calculates the **required number of cyclones** based on the feed rate, particle density, feed solid percent, pressure drop, and cyclone diameter.

---

## 📥 Syntax

```excel
=CYCLONE.COUNT(P, F, Rho, sp, D)
```

---

## 🧾 Parameters

| Parameter          | Type    | Description                                                                 |
|---------------------|---------|-----------------------------------------------------------------------------|
| `P` (Pressure Drop) | Double  | The cyclone pressure drop in **kPa** (e.g., 100).                           |
| `F` (Feed Rate)     | Double  | The mass solid feed rate in **t/h** (e.g., 50).                             |
| `Rho` (Solid Density) | Double | The particle density in **t/m³** (e.g., 2.7).                               |
| `sp` (Feed Solid Percent) | Double | The mass solid percent of the feed (e.g., 45 for 45%).                  |
| `D` (Diameter)      | Double  | The diameter of the cyclone in **cm** (e.g., 50).                           |

---

## 🧮 Formula

The required number of cyclones is calculated using the following formula:

$$
\text{Cyclone Count} = \frac{\frac{F}{Rho} + \text{SolidPercent2DilutionRatio}(sp) \cdot F}{\text{CycloneCapacity}(P, D)}
$$

Where:  
- `SolidPercent2DilutionRatio(sp)` converts the feed solid percent to a dilution ratio.  
- `CycloneCapacity(P, D)` calculates the capacity of a single cyclone in **m³/h**.  

---

## 💡 Example

Calculate the required number of cyclones with the following parameters:  
- Pressure drop (`P`): **100 kPa**  
- Feed rate (`F`): **50 t/h**  
- Solid density (`Rho`): **2.7 t/m³**  
- Feed solid percent (`sp`): **45%**  
- Diameter (`D`): **50 cm**

```excel
=CYCLONE.COUNT(100, 50, 2.7, 45, 50)
```

---

## 📝 Notes

- Ensure that the feed solid percent (`sp`) is between 0 and 100.
- The function depends on two helper functions: `SolidPercent2DilutionRatio` and `CycloneCapacity`.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`CYCLONE.CAPACITY`](./CycloneCapacity.md)
- [`SOLIDPERCENT.TO.DILUTION.RATIO`](./SolidPercent2DilutionRatio.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16