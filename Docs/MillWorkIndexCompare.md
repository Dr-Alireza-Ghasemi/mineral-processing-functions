# 🔁 MILL.WORK.INDEX.COMPARE

🔹 **Description**:  
This function calculates the **Bond Work Index (kWh/t)** for an ore, based on a comparison with a reference ore of known work index, using the Bond Work Index formula.

---

## 📥 Syntax

```excel
=MILL.WORK.INDEX.COMPARE(Wir, F80r, P80r, F80, P80)
```

---

## 🧾 Parameters

| Parameter          | Type   | Description                                                                 |
|---------------------|--------|-----------------------------------------------------------------------------|
| `Wir` (Reference Work Index) | Double | The reference work index measured in a laboratory mill (kWh/t).           |
| `F80r` (Reference Feed Size) | Double | The size (in micrometers) of the 80% passing in the reference feed.       |
| `P80r` (Reference Product Size) | Double | The size (in micrometers) of the 80% passing in the reference product.    |
| `F80` (Feed Size)            | Double | The size (in micrometers) of the 80% passing in the ore's fresh feed.     |
| `P80` (Product Size)         | Double | The size (in micrometers) of the 80% passing in the ore's product.        |

---

## 🧮 Formula

The Bond Work Index for an ore is calculated using the following formula:

$$
\text{Work Index} = Wir \cdot \frac{\left(\frac{1}{\sqrt{P80r}} - \frac{1}{\sqrt{F80r}}\right)}{\left(\frac{1}{\sqrt{P80}} - \frac{1}{\sqrt{F80}}\right)}
$$

Where:  
- \( Wir \): Reference work index (kWh/t).  
- \( F80r \): Size of 80% passing in the reference feed (µm).  
- \( P80r \): Size of 80% passing in the reference product (µm).  
- \( F80 \): Size of 80% passing in the ore's feed (µm).  
- \( P80 \): Size of 80% passing in the ore's product (µm).  

---

## 💡 Example

### Example 1:
Calculate the Bond Work Index for an ore with the following parameters:  
- Reference work index: **15.0 kWh/t**  
- Reference feed size (F80r): **1000 µm**  
- Reference product size (P80r): **75 µm**  
- Feed size (F80): **1200 µm**  
- Product size (P80): **100 µm**

```excel
=MILL.WORK.INDEX.COMPARE(15, 1000, 75, 1200, 100)
```

**Result**: `13.47 kWh/t` (approximate value)

---

## 📝 Notes

- Ensure all feed and product sizes (`F80`, `P80`, `F80r`, `P80r`) are provided in micrometers.
- The reference work index (`Wir`) must be determined experimentally using a laboratory mill.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`MILL.WORK.INDEX.OPERATING`](./MillWorkIndexOperating.md)
- [`MILL.SPECIFIC.ENERGY`](./MillSpecificEnergy.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17