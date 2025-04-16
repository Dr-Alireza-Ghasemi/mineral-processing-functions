# 🔁 PLITT.S

🔹 **Description**:  
This function uses the **Plitt model** to estimate the split ratio of a hydrocyclone.

---

## 📥 Syntax

```excel
=PLITT.S(Dc, Do, Du, h, PS, Rhos, P)
```

---

## 🧾 Parameters

| Parameter          | Type    | Description                                                                 |
|---------------------|---------|-----------------------------------------------------------------------------|
| `Dc` (Cyclone Diameter) | Double  | The diameter of the cyclone in **cm** (e.g., 50).                          |
| `Do` (Vortex Finder)    | Double  | The vortex finder diameter of the cyclone in **cm** (e.g., 10).            |
| `Du` (Underflow Diameter) | Double | The underflow diameter of the cyclone in **cm** (e.g., 8).                 |
| `h` (Vortex Finder Height) | Double | The vortex finder height of the cyclone in **cm** (e.g., 15).             |
| `PS` (Percent Solid)     | Double | The percent solid of the cyclone feed (e.g., 45 for 45%).                  |
| `Rhos` (Solid Density)   | Double | The solid density of the cyclone feed in **g/cm³** (e.g., 2.7).            |
| `P` (Pressure)           | Double | The pressure of the cyclone feed in **kPa** (e.g., 100).                   |

---

## 🧮 Formula

This function calculates the split ratio using the following formula:

### Step 1: Calculate Φ (Phi)
$$
\Phi = \frac{\frac{PS}{Rhos}}{\frac{PS}{Rhos} + (100 - PS)} \times 100
$$

### Step 2: Calculate ρp (Pulp Density)
$$
\rho_p = \frac{100}{\frac{PS}{Rhos} + (100 - PS)}
$$

### Step 3: Convert Pressure to m Pressure
$$
P_{mp} = \frac{P}{9.81 \cdot \rho_p}
$$

### Step 4: Calculate Split Ratio
$$
S = \frac{1.9 \cdot \left(\frac{Du}{Do}\right)^{3.31} \cdot h^{0.54} \cdot (Du^2 + Do^2)^{0.36} \cdot e^{0.0054 \cdot \Phi}}{Dc^{1.11} \cdot P_{mp}^{0.24}}
$$

---

## 💡 Example

Estimate the split ratio of a hydrocyclone with the following parameters:  
- Cyclone diameter (`Dc`): **50 cm**  
- Vortex finder diameter (`Do`): **10 cm**  
- Underflow diameter (`Du`): **8 cm**  
- Vortex finder height (`h`): **15 cm**  
- Percent solid (`PS`): **45%**  
- Solid density (`Rhos`): **2.7 g/cm³**  
- Pressure (`P`): **100 kPa**

```excel
=PLITT.S(50, 10, 8, 15, 45, 2.7, 100)
```

---

## 📝 Notes

- Ensure all dimensions are in **cm** and the pressure is in **kPa**.
- The function will return `-1` if user authentication fails.
- The model assumes the solid density (`Rhos`) is greater than 1.

---

📌 **Related Functions**:
- [`PLITT.D50`](./PlittD50.md)
- [`PLITT.P`](./PlittP.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16