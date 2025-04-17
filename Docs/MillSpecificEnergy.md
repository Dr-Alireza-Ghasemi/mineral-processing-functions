# 🔁 MILL.SPECIFIC.ENERGY

🔹 **Description**:  
This function calculates the **specific energy consumption** of a mill in **kWh per ton (kWh/t)**, based on the Bond Work Index and the sizes of the feed and product.

---

## 📥 Syntax

```excel
=MILL.SPECIFIC.ENERGY(wi, f80, p80)
```

---

## 🧾 Parameters

| Parameter          | Type   | Description                                                                 |
|---------------------|--------|-----------------------------------------------------------------------------|
| `wi` (Work Index)   | Double | The work index of the material measured in a laboratory mill (kWh/t).       |
| `f80` (Feed Size)   | Double | The size (in micrometers) of the 80% passing in the fresh feed.             |
| `p80` (Product Size)| Double | The size (in micrometers) of the 80% passing in the product.                |

---

## 🧮 Formula

The specific energy consumption is calculated using the Bond Work Index formula:

$$
\text{Specific Energy (kWh/t)} = Wi \cdot 10 \cdot \left(\frac{1}{\sqrt{P80}} - \frac{1}{\sqrt{F80}}\right)
$$

Where:  
- \( Wi \): Work index (kWh/t).  
- \( F80 \): Size of 80% passing in the feed (µm).  
- \( P80 \): Size of 80% passing in the product (µm).  

---

## 💡 Example

### Example 1:
Calculate the specific energy consumption of a mill with:  
- Work Index: **14 kWh/t**  
- Feed size (F80): **1000 µm**  
- Product size (P80): **75 µm**

```excel
=MILL.SPECIFIC.ENERGY(14, 1000, 75)
```

**Result**: `9.26 kWh/t` (approximate value)

---

## 📝 Notes

- Ensure the feed size (`f80`) and product size (`p80`) are provided in micrometers.
- The Bond Work Index (`wi`) should be determined experimentally using a laboratory mill.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- N/A  

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17