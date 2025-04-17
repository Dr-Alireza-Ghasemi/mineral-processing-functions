# 🔁 ROSIN.RAMMLER.DIST

🔹 **Description**:  
This function calculates the **cumulative passing percentage** for a specific sieve size using the **Rosin-Rammler distribution** model. 

---

## 📥 Syntax

```excel
=ROSIN.RAMMLER.DIST(d, d63, m)
```

---

## 🧾 Parameters

| Parameter          | Type   | Description                                                                 |
|---------------------|--------|-----------------------------------------------------------------------------|
| `d` (Size)         | Double | The sieve size for which the cumulative passing percentage is calculated.   |
| `d63`              | Double | The size at which 63% of the material passes.                               |
| `m` (Uniformity Constant) | Double | The uniformity constant that describes particle size distribution.       |

---

## 🧮 Formula

The cumulative passing percentage for a given size is calculated as follows:

$$
\text{Cumulative Passing Percent} = \left(1 - e^{-\left(\frac{d}{d63}\right)^m}\right) \times 100
$$

Where:  
- `d` = sieve size.  
- `d63` = size at which 63% of the material passes.  
- `m` = uniformity constant.  
- `e` = base of the natural logarithm.

---

## 💡 Example

### Example 1:
Calculate the cumulative passing percentage for:  
- Sieve Size (`d`): **50 µm**  
- Size at 63% Passing (`d63`): **100 µm**  
- Uniformity Constant (`m`): **2**

```excel
=ROSIN.RAMMLER.DIST(50, 100, 2)
```

**Result**: `22.14%`

### Example 2:
Calculate the cumulative passing percentage for:  
- Sieve Size (`d`): **150 µm**  
- Size at 63% Passing (`d63`): **100 µm**  
- Uniformity Constant (`m`): **1.5**

```excel
=ROSIN.RAMMLER.DIST(150, 100, 1.5)
```

**Result**: `85.95%`

---

## 📝 Notes

- Ensure `d63` and `m` are positive values.
- The function will return a percentage value between 0 and 100.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`CLASSIFICATION.D50`](./ClassificationD50.md)
- [`CLASSIFICATION.D80`](./ClassificationD80.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17