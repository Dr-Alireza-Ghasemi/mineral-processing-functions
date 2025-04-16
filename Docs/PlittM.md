# 🔁 PLITT.M

🔹 **Description**:  
This function uses the **Plitt model** to estimate the **sharpness of separation** of a hydrocyclone.

---

## 📥 Syntax

```excel
=PLITT.M(Dc, h, S, Q)
```

---

## 🧾 Parameters

| Parameter          | Type    | Description                                                                 |
|---------------------|---------|-----------------------------------------------------------------------------|
| `Dc` (Cyclone Diameter) | Double  | The diameter of the cyclone in **cm** (e.g., 50).                          |
| `h` (Vortex Finder Height) | Double | The vortex finder height of the cyclone in **cm** (e.g., 15).             |
| `S` (Split Ratio)        | Double | The split ratio of the cyclone underflow to overflow (e.g., 0.5).          |
| `Q` (Capacity)           | Double | The capacity of the cyclone in **lit/min** (e.g., 300).                    |

---

## 🧮 Formula

This function calculates the sharpness of separation using the following formula:

### Step 1: Calculate Rv (Underflow-to-Overflow Ratio)
$$
Rv = \frac{S}{S + 1}
$$

### Step 2: Calculate Sharpness of Separation (M)
$$
M = 1.94 \cdot e^{-1.58 \cdot Rv} \cdot \left( \frac{Dc^2 \cdot h}{Q} \right)^{0.15}
$$

Where:  
- `Rv` is the underflow-to-overflow ratio.  
- `Dc`, `h`, `S`, and `Q` are parameters provided by the user.

---

## 💡 Example

Estimate the sharpness of separation of a hydrocyclone with the following parameters:  
- Cyclone diameter (`Dc`): **50 cm**  
- Vortex finder height (`h`): **15 cm**  
- Split ratio (`S`): **0.5**  
- Capacity (`Q`): **300 lit/min**

```excel
=PLITT.M(50, 15, 0.5, 300)
```

---

## 📝 Notes

- Ensure all dimensions are in **cm** and the capacity is in **lit/min**.
- The function will return `-1` if user authentication fails.
- The split ratio (`S`) should be a positive value.

---

📌 **Related Functions**:
- [`PLITT.D50`](./PlittD50.md)
- [`PLITT.S`](./PlittS.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16