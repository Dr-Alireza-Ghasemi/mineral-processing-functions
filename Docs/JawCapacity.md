# 🔁 JAW.CRUSHER.CAPACITY

🔹 **Description**:  
This function calculates the **volumetric capacity** of a jaw crusher in cubic meters per hour (**m³/h**).

---

## 📥 Syntax

```excel
=JAW.CRUSHER.CAPACITY(B, S, s, a, n, k)
```

---

## 🧾 Parameters

| Parameter | Type    | Description                                                                                           |
|-----------|---------|-------------------------------------------------------------------------------------------------------|
| `B`       | Double  | The inner width of the crusher in meters (e.g., 1.2).                                                |
| `S`       | Double  | The open side setting in meters (e.g., 0.15).                                                        |
| `s`       | Double  | The throw in meters (e.g., 0.02).                                                                     |
| `a`       | Double  | The angle of nip in degrees (e.g., 22).                                                              |
| `n`       | Double  | The speed of the crusher in rotations per minute (RPM) (e.g., 300).                                  |
| `k`       | Double  | A material constant, typically between **1.5** and **2**, varying with material characteristics.      |

---

## 🧮 Formula

$$
\text{Jaw Crusher Capacity} = \frac{B \cdot S \cdot s}{\tan(a \cdot \frac{\pi}{180})} \cdot k \cdot 60 \cdot n
$$

Where:  
- `B` = inner width of crusher (m)  
- `S` = open side setting (m)  
- `s` = throw (m)  
- `a` = angle of nip (degrees)  
- `n` = speed of crusher (RPM)  
- `k` = material constant  

---

## 💡 Example

Calculate the volumetric capacity of a jaw crusher with the following parameters:  
- Inner width (`B`): **1.2 m**  
- Open side setting (`S`): **0.15 m**  
- Throw (`s`): **0.02 m**  
- Angle of nip (`a`): **22°**  
- Speed of crusher (`n`): **300 RPM**  
- Material constant (`k`): **1.8**

```excel
=JAW.CRUSHER.CAPACITY(1.2, 0.15, 0.02, 22, 300, 1.8)
```

**Result**: `256.65 m³/h`

---

## 📝 Notes

- Ensure all parameters are in the correct units (meters, degrees, RPM).
- The function will return `-1` if user authentication fails.
- The material constant (`k`) should be selected based on the material's characteristics, feeding method, and liner type.

---

📌 **Related Functions**:
- N/A  

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-16