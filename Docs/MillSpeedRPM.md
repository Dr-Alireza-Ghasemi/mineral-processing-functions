# 🔁 MILLSPEED.RPM

🔹 **Description**:  
This function converts the mill speed, expressed as a percentage of the **critical speed**, into **revolutions per minute (RPM)**.

---

## 📥 Syntax

```excel
=MILLSPEED.RPM(d, SpeedPercent)
```

---

## 🧾 Parameters

| Parameter          | Type   | Description                                           |
|---------------------|--------|-------------------------------------------------------|
| `d` (Diameter)      | Double | The diameter of the mill in meters (e.g., 2.5 m).     |
| `SpeedPercent`      | Double | The speed of the mill as a percentage of its critical speed (e.g., 75 for 75%). |

---

## 🧮 Formula

The mill speed in RPM is calculated using the following formula:

$$
\text{Mill Speed (RPM)} = \frac{\text{SpeedPercent}}{100} \times \frac{42.3}{\sqrt{d}}
$$

Where:  
- \( d \): Diameter of the mill in meters.  
- \( \text{SpeedPercent} \): Speed of the mill as a percentage of its critical speed.  
- \( \frac{42.3}{\sqrt{d}} \): Critical speed of the mill in RPM.

---

## 💡 Example

### Example 1:
Convert the mill speed to RPM when:  
- Diameter of the mill: **2.5 meters**  
- Mill speed: **75% of critical speed**

```excel
=MILLSPEED.RPM(2.5, 75)
```

**Result**: `20.07 RPM`

---

## 📝 Notes

- Ensure the mill diameter (`d`) is provided in meters.
- This function is the reverse of the `MILLSPEED.PERCENT` function.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`MILL.CRITICAL.SPEED`](./MillCriticalSpeed.md)
- [`MILLSPEED.PERCENT`](./MillSpeedPercent.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17