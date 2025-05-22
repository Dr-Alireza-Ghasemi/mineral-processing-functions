# 🛠️ MILL.FILLING.CONIC

### 📏 **Purpose**  
Estimates the **filling percentage** for mills with **conic end walls**. This function considers the total internal volume of the mill, including both the cylindrical body and the two conical ends, to provide an accurate calculation of filling percent.

---

## 📥 **Syntax**

```excel
=MILL.FILLING.CONIC(Diameter, H, Teta, EGL)
```

---

## 🧾 **Parameters**

| Parameter    | Type   | Description                                                                 |
|--------------|--------|-----------------------------------------------------------------------------|
| `Diameter`   | Number | Internal diameter of the mill (meters).                                     |
| `H`          | Number | Vertical distance from the charge surface to the mill ceiling (meters).      |
| `Teta`       | Number | End wall angle relative to vertical (degrees).                              |
| `EGL`        | Number | Effective Grinding Length: straight distance between the ends of the cylindrical section (meters). |

---

## 🧮 **Calculation Details**

This function divides the mill into three parts:
- **Cylindrical Body**: The main section of the mill.
- **Two Conic Ends**: Both ends of the mill are considered as cones.

The function computes:
- The total internal volume (**cylinder + 2 cones**).
- The charge (ball/material) volume within both the cylindrical and conic portions.
- The **filling percent** as the occupied volume (charge) divided by the total mill volume, multiplied by 100.

---

## 💡 **Example**

Suppose you have a mill with:
- `Diameter` = 4.0 (meters)
- `H` = 2.3 (meters)
- `Teta` = 15 (degrees)
- `EGL` = 8.0 (meters)

The formula would be:

```excel
=MILL.FILLING.CONIC(4.0, 2.3, 15, 8.0)
```

---

## 📝 **Notes**

- For mills **without conic ends** (flat/cylindrical end walls), use [`MILL.FILLING`](./MillFilling.md) instead.
- All dimensions must be in **meters** and angles in **degrees**.
- The function returns the **percentage** of the total internal volume occupied by the charge.

---

## 📚 **Related Functions**

- [`MILL.FILLING`](./MillFilling.md) – For flat endwall (cylindrical) mills.

---

🛠️ **Created by**: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 **Last updated**: 2025-05-22