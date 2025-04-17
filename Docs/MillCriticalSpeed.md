# 🔁 MILL.CRITICAL.SPEED

🔹 **Description**:  
This function calculates the **critical speed** of a mill in **revolutions per minute (RPM)**. The critical speed is the speed at which the mill's grinding media will centrifuge and no longer fall, operating in an optimized grinding condition.

---

## 📥 Syntax

```excel
=MILL.CRITICAL.SPEED(d)
```

---

## 🧾 Parameters

| Parameter          | Type   | Description                                           |
|---------------------|--------|-------------------------------------------------------|
| `d` (Diameter)      | Double | The diameter of the mill in meters (e.g., 2.5 m).     |

---

## 🧮 Formula

The critical speed in RPM is calculated using the following formula:

$$
\text{Mill Critical Speed (RPM)} = \frac{42.3}{\sqrt{d}}
$$

Where:  
- \( d \) = diameter of the mill in meters.

---

## 💡 Example

### Example 1:
Calculate the critical speed for a mill with a diameter of **2.5 meters**.

```excel
=MILL.CRITICAL.SPEED(2.5)
```

**Result**: `26.76 RPM`

---

## 📝 Notes

- Ensure the mill diameter (`d`) is provided in meters.
- The function follows the standard formula for critical speed calculation in milling operations.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- N/A  

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17