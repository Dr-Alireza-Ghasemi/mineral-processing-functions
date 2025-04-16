# 🔁 PLITT.P

🔹 **Description**:  
This function uses the **Plitt model** to estimate the pressure of a hydrocyclone.

---

## 📥 Syntax

```excel
=PLITT.P(Dc, Di, Do, Du, h, PS, Rhos, Q)
```

---

## 🧾 Parameters

| Parameter          | Type    | Description                                                                 |
|---------------------|---------|-----------------------------------------------------------------------------|
| `Dc` (Cyclone Diameter) | Double  | The diameter of the cyclone in **cm** (e.g., 50).                          |
| `Di` (Input Diameter)   | Double  | The input diameter of the cyclone in **cm** (e.g., 5).                     |
| `Do` (Vortex Finder)    | Double  | The vortex finder diameter of the cyclone in **cm** (e.g., 10).            |
| `Du` (Underflow Diameter) | Double | The underflow diameter of the cyclone in **cm** (e.g., 8).                 |
| `h` (Vortex Finder Height) | Double | The vortex finder height of the cyclone in **cm** (e.g., 15).             |
| `PS` (Percent Solid)     | Double | The percent solid of the cyclone feed (e.g., 45 for 45%).                  |
| `Rhos` (Solid Density)   | Double | The solid density of the cyclone feed in **g/cm³** (e.g., 2.7).            |
| `Q` (Capacity)           | Double | The capacity of the cyclone in **lit/min** (e.g., 300).                    |

---

## 🧮 Formula

This function calculates the pressure using the following formula:

$$
\Phi = \frac{\frac{PS}{Rhos}}{\frac{PS}{Rhos} + (100 - PS)} \times 100
$$

$$
P = \frac{1.88 \cdot Q^{1.78} \cdot e^{0.0055 \cdot \Phi}}{Dc^{0.37} \cdot Di^{0.94} \cdot h^{0.28} \cdot (Du^2 + Do^2)^{0.87}}
$$

Where:  
- `Φ` (`Phi`) is calculated based on the percent solid (`PS`) and solid density (`Rhos`).  
- `Dc`, `Di`, `Do`, `Du`, `h`, `Q`, and `Rhos` are parameters provided by the user.

---

## 💡 Example

Estimate the pressure of a hydrocyclone with the following parameters:  
- Cyclone diameter (`Dc`): **50 cm**  
- Input diameter (`Di`): **5 cm**  
- Vortex finder diameter (`Do`): **10 cm**  
- Underflow diameter (`Du`): **8 cm**  
- Vortex finder height (`h`): **15 cm**  
- Percent solid (`PS`): **45%**  
- Solid density (`Rhos`): **2.7 g/cm³**  
- Capacity (`Q`): **300 lit/min**

```excel
=PLITT.P(50, 5, 10, 8, 15, 45, 2.7, 300)
```

---

## 📝 Notes

- Ensure all dimensions are in **cm** and the capacity is in **lit/min**.
- The function will return `-1` if user authentication fails.
- The model assumes the solid density (`Rhos`) is greater than 1.

---

📌 **Related Functions**:
- [`PLITT.D50`](./PlittD50.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16