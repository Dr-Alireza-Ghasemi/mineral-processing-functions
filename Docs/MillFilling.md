# 🔁 MILL.FILLING

🔹 **Description**:  
This function estimates the **mill filling percentage**, which indicates the volume of the mill occupied by the charge (e.g., grinding media and material).

---

## 📥 Syntax

```excel
=MILL.FILLING(d, h)
```

---

## 🧾 Parameters

| Parameter          | Type   | Description                                                                 |
|---------------------|--------|-----------------------------------------------------------------------------|
| `d` (Diameter)      | Double | The diameter of the mill in meters (e.g., 3.5 m).                           |
| `h` (Charge Height) | Double | The distance between the charge surface and the ceiling of the mill, in meters. |

---

## 🧮 Formula

The mill filling percentage is calculated using the following formula:

1. Calculate the angle \( \beta \) in radians:
   $$
   \beta = \pi - 2 \cdot \arcsin\left(\frac{h - d / 2}{d / 2}\right)
   $$

2. Calculate the filling percentage:
   $$
   \text{Filling Percent} = \frac{1}{2} \cdot \frac{\beta - \sin(\beta)}{\pi} \cdot 100
   $$

Where:  
- \( d \) = diameter of the mill in meters.  
- \( h \) = distance between the charge surface and the ceiling of the mill in meters.  
- \( \beta \) = angle of the charge arc in radians.

---

## 💡 Example

### Example 1:
Estimate the mill filling percentage for the following parameters:  
- Diameter of the mill: **3.5 meters**  
- Distance from charge surface to ceiling: **1.0 meter**

```excel
=MILL.FILLING(3.5, 1.0)
```

**Result**: `35.15%` (approximate value)

---

## 📝 Notes

- Ensure the mill diameter (`d`) and charge height (`h`) are provided in meters.
- The function assumes a cylindrical mill geometry.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- N/A  

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17