# 🔁 GYRATORY.CRUSHER.CAPACITY

🔹 **Description**:  
This function calculates the **volumetric capacity** of a gyratory crusher in cubic meters per hour (**m³/h**).

---

## 📥 Syntax

```excel
=GYRATORY.CRUSHER.CAPACITY(D, S, s, a, n, k)
```

---

## 🧾 Parameters

| Parameter | Type    | Description                                                                                           |
|-----------|---------|-------------------------------------------------------------------------------------------------------|
| `D`       | Double  | The diameter of the head mantle at the discharge point in meters (e.g., 1.5).                        |
| `S`       | Double  | The open side setting in meters (e.g., 0.2).                                                         |
| `s`       | Double  | The throw in meters (e.g., 0.05).                                                                     |
| `a`       | Double  | The angle of nip in degrees (e.g., 22).                                                              |
| `n`       | Double  | The speed of the crusher in rotations per minute (RPM) (e.g., 250).                                  |
| `k`       | Double  | A material constant, typically between **2** and **3**, varying with material characteristics.        |

---

## 🧮 Formula

$$
\text{Gyratory Crusher Capacity} = (D - S) \cdot \pi \cdot S \cdot s \cdot \frac{1}{\tan(a \cdot \frac{\pi}{180})} \cdot k \cdot 60 \cdot n
$$

Where:  
- `D` = diameter of the head mantle at the discharge point (m)  
- `S` = open side setting (m)  
- `s` = throw (m)  
- `a` = angle of nip (degrees)  
- `n` = speed of crusher (RPM)  
- `k` = material constant  

---

## 💡 Example

Calculate the volumetric capacity of a gyratory crusher with the following parameters:  
- Diameter of head mantle at discharge point (`D`): **1.5 m**  
- Open side setting (`S`): **0.2 m**  
- Throw (`s`): **0.05 m**  
- Angle of nip (`a`): **22°**  
- Speed of crusher (`n`): **250 RPM**  
- Material constant (`k`): **2.5**

```excel
=GYRATORY.CRUSHER.CAPACITY(1.5, 0.2, 0.05, 22, 250, 2.5)
```

**Result**: `221.06 m³/h`

---

## 📝 Notes

- Ensure all parameters are in the correct units (meters, degrees, RPM).
- The function will return `-1` if user authentication fails.
- The material constant (`k`) should be selected based on the material's characteristics, feeding method, and liner type.

---

📌 **Related Functions**:
- [`JAW.CRUSHER.CAPACITY`](./JawCapacity.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16