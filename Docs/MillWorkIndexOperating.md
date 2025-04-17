# 🔁 MILL.WORK.INDEX.OPERATING

🔹 **Description**:  
This function calculates the **Bond Work Index (kWh/t)** for a milling operation based on energy consumption, ground material mass, and the sizes of the feed and product.

---

## 📥 Syntax

```excel
=MILL.WORK.INDEX.OPERATING(W, Mass, F80, P80)
```

---

## 🧾 Parameters

| Parameter          | Type   | Description                                                                 |
|---------------------|--------|-----------------------------------------------------------------------------|
| `W` (Energy Consumption) | Double | The total energy consumption of the mill in kilowatt-hours (kWh).         |
| `Mass` (Material Mass)    | Double | The total ground mass of the material in kilograms (kg).                  |
| `F80` (Feed Size)         | Double | The size (in micrometers) of the 80% passing in the fresh feed.           |
| `P80` (Product Size)      | Double | The size (in micrometers) of the 80% passing in the product.              |

---

## 💡 Example

### Example 1:
Calculate the operating Bond Work Index for:  
- Energy consumption: **500 kWh**  
- Ground material mass: **10000 kg**  
- Feed size (F80): **1000 µm**  
- Product size (P80): **75 µm**

```excel
=MILL.WORK.INDEX.OPERATING(500, 10000, 1000, 75)
```

**Result**: `14.44 kWh/t` (approximate value)

---

## 📝 Notes

- Ensure the feed size (`F80`) and product size (`P80`) are provided in micrometers.
- Energy consumption (`W`) should be in kilowatt-hours, and material mass (`Mass`) should be in kilograms for accurate results.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`MILL.SPECIFIC.ENERGY`](./MillSpecificEnergy.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17
