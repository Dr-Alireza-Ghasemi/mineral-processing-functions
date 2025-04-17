# 🔁 MILL.BALL.SIZE

🔹 **Description**:  
This function calculates the **top size of grinding media (balls)** in millimeters, based on the **Fred C. Bond Method**.

---

## 📥 Syntax

```excel
=MILL.BALL.SIZE(F80, Wi, Vcr, Density, Diameter)
```

---

## 🧾 Parameters

| Parameter          | Type   | Description                                                                 |
|---------------------|--------|-----------------------------------------------------------------------------|
| `F80` (Feed Size)   | Double | The size (in millimeters) of the 80% passing in the fresh feed.             |
| `Wi` (Work Index)   | Double | The Bond Work Index of the material (kWh/t).                                |
| `Vcr` (Critical Speed Percent) | Double | The percentage of the critical speed of the mill.                         |
| `Density`           | Double | The specific gravity of the feed material in t/m³.                         |
| `Diameter`          | Double | The diameter of the mill (in meters) inside the liners.                    |

---

## 🧮 Formula

The top size of the grinding media (balls) is calculated using the following formula:

$$
\text{Ball Size (mm)} = \sqrt{\frac{F80 \cdot 1000 \cdot Wi \cdot 0.9072}{200 \cdot Vcr} \cdot \sqrt{\frac{\rho}{\sqrt{\frac{Diameter}{0.305}}}}} \cdot 25.4
$$

Where:  
- \( F80 \): Feed size (mm).  
- \( Wi \): Work index (kWh/t).  
- \( Vcr \): Percentage of the critical speed (\%).  
- \( \rho \): Specific gravity of the feed material (t/m³).  
- \( Diameter \): Mill diameter (m).  

---

## 💡 Example

### Example 1:
Calculate the top size of grinding media for the following parameters:  
- Feed size (F80): **10 mm**  
- Work Index (Wi): **14 kWh/t**  
- Critical speed percent (Vcr): **75%**  
- Feed density: **2.6 t/m³**  
- Mill diameter: **3.5 m**

```excel
=MILL.BALL.SIZE(10, 14, 75, 2.6, 3.5)
```

**Result**: `99.732 mm` (approximate value)

---

## 📝 Notes

- Ensure that the feed size (`F80`) is provided in millimeters.
- The critical speed percent (`Vcr`) should be entered as a whole number (e.g., 75 for 75%).
- The function assumes the Bond method for grinding media size calculation.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`MILL.SPECIFIC.ENERGY`](./MillSpecificEnergy.md)
- [`MILL.CRITICAL.SPEED`](./MillCriticalSpeed.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17