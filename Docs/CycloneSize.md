# 🔁 CYCLONE.SIZE

🔹 **Description**:  
This function calculates the **hydrocyclone diameter** in centimeters (**cm**) based on various parameters, including pressure drop, particle density, feed solid percent, particle size, and passing percent.

---

## 📥 Syntax

```excel
=CYCLONE.SIZE(P, Rho, sp, S, Q)
```

---

## 🧾 Parameters

| Parameter          | Type    | Description                                                                 |
|---------------------|---------|-----------------------------------------------------------------------------|
| `P` (Pressure Drop) | Double  | The assumed pressure drop in **kPa** (e.g., 100).                           |
| `Rho` (Solid Density) | Double | The particle density in **t/m³** (e.g., 2.7).                               |
| `sp` (Feed Solid Percent) | Double | The cyclone feed solid percent (e.g., 45 for 45%).                       |
| `S` (Particle Size) | Double | The assumed particle size in **µm** (e.g., 50).                             |
| `Q` (Passing Percent) | Double | The required percent that should pass from the particle size (`S`) (e.g., 80). |

---

## 🧮 Formula

This function calculates the cyclone diameter using the following formula:

$$
D = \exp\left(\frac{\ln\left(P^{0.28} \cdot (Rho - 1)^{0.5} \cdot (53 - \text{SolidPercentMass2Vol}(sp, Rho))^{1.43} \cdot S \cdot (-3.162 \cdot \ln(Q) + 15.1)\right)}{0.66} - 12.358\right)
$$

Where:  
- `SolidPercentMass2Vol(sp, Rho)` converts feed solid percent (`sp`) to volume percent based on particle density (`Rho`).
- `P` = pressure drop in **kPa**.
- `Rho` = particle density in **t/m³**.
- `sp` = feed solid percent.
- `S` = particle size in **µm**.
- `Q` = required passing percent.

---

## 💡 Example

Calculate the hydrocyclone diameter with the following parameters:  
- Pressure drop (`P`): **100 kPa**  
- Solid density (`Rho`): **2.7 t/m³**  
- Feed solid percent (`sp`): **45%**  
- Particle size (`S`): **50 µm**  
- Passing percent (`Q`): **80%**

```excel
=CYCLONE.SIZE(100, 2.7, 45, 50, 80)
```

---

## 📝 Notes

- Ensure that `sp` is between 0 and 100, and `Q` is expressed as a percentage (e.g., 80 for 80%).
- The function depends on the helper function `SolidPercentMass2Vol` for intermediate calculations.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`SOLIDPERCENT.VOL.TO.MASS`](./SolidPercentVol2Mass.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16