# 🔁 MILLSPEED.PERCENT

🔹 **Description**:  
This function converts the actual mill speed (in RPM) to a percentage of the **critical speed** of the mill.

---

## 📥 Syntax

```excel
=MILLSPEED.PERCENT(d, RPM)
```

---

## 🧾 Parameters

| Parameter          | Type   | Description                                           |
|---------------------|--------|-------------------------------------------------------|
| `d` (Diameter)      | Double | The diameter of the mill in meters (e.g., 2.5 m).     |
| `RPM`               | Double | The actual speed of the mill in revolutions per minute (RPM). |


---

## 💡 Example

### Example 1:
Convert the mill speed to percentage when:  
- Diameter of the mill: **2.5 meters**  
- Mill speed: **20 RPM**

```excel
=MILLSPEED.PERCENT(2.5, 20)
```

**Result**: `74.76%`

---

## 📝 Notes

- Ensure the mill diameter (`d`) is provided in meters.
- The function calculates the percentage by comparing the actual mill speed to the critical speed.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`MILL.CRITICAL.SPEED`](./MillCriticalSpeed.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17
