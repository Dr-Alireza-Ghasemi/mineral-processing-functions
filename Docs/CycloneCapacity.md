# 🔁 CYCLONE.CAPACITY

🔹 **Description**:  
This function calculates the **capacity of a cyclone** in cubic meters per hour (**m³/h**) based on its pressure drop and diameter.

---

## 📥 Syntax

```excel
=CYCLONE.CAPACITY(P, D)
```

---

## 🧾 Parameters

| Parameter          | Type    | Description                                                                 |
|---------------------|---------|-----------------------------------------------------------------------------|
| `P` (Pressure Drop) | Double  | The cyclone pressure drop in **kPa** (e.g., 100).                           |
| `D` (Diameter)      | Double  | The diameter of the cyclone in **cm** (e.g., 50).                           |

---

## 🧮 Formula

The capacity is calculated using the following formula:

$$
\text{Capacity} = \frac{9.5}{1000} \cdot \sqrt{P} \cdot D^2
$$

Where:  
- `P` = cyclone pressure drop in **kPa**.  
- `D` = diameter of the cyclone in **cm**.  

---

## 💡 Example

Calculate the capacity of a cyclone with the following parameters:  
- Pressure drop (`P`): **100 kPa**  
- Diameter (`D`): **50 cm**

```excel
=CYCLONE.CAPACITY(100, 50)
```

**Result**: `23.75 m³/h`

---

## 📝 Notes

- Ensure the pressure drop (`P`) is a positive value in **kPa**.
- Ensure the diameter (`D`) is provided in **cm**.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`CYCLONE.SIZE`](./CycloneSize.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16