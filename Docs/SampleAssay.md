# 🔁 SAMPLE.ASSAY

🔹 **Description**:  
This function calculates the **mass of the sample (in grams)** based on various parameters, including particle size, shape factor, mineral content, and relative standard deviation.

---

## 📥 Syntax

```excel
=SAMPLE.ASSAY(d95, f, g, L, a, r, t, σ)
```

---

## 🧾 Parameters

| Parameter         | Type   | Description                                                                 |
|--------------------|--------|-----------------------------------------------------------------------------|
| `d95`             | Double | The nominal 95% passing size of the particle in the sample (in cm).         |
| `f`               | Double | The shape factor relating volume to the diameter of the particles. Default values: <br> - For general cases: **0.5** <br> - For gold ores: **0.2**. |
| `g`               | Double | The particle size distribution factor. Choose based on \( \frac{d95}{d5} \): <br> - **0.25** for \( \frac{d95}{d5} > 4 \) <br> - **0.5** for \( 4 > \frac{d95}{d5} > 2 \) <br> - **0.75** for \( 2 > \frac{d95}{d5} > 1 \) <br> - **1.0** for \( \frac{d95}{d5} = 1 \). |
| `L`               | Double | The liberation size (in cm).                                                |
| `a`               | Double | The fractional average mineral content of the material being sampled.       |
| `r`               | Double | The mean density of the valuable mineral (in g/cm³).                        |
| `t`               | Double | The mean density of the gangue mineral (in g/cm³).                          |
| `σ` (Zigma)       | Double | The relative standard deviation (in g/cm³).                                 |

---

## 🧮 Formula

The mass of the sample is calculated using the following formula:

$$
l = \sqrt{\frac{L}{d95}}
$$

$$
m = \frac{(1 - a)}{a} \cdot \left[(1 - a) \cdot r + a \cdot t \right]
$$

$$
\text{Sample Mass (g)} = \frac{f \cdot g \cdot l \cdot m \cdot d95^3}{\sigma^2}
$$

Where:  
- \( l \): Liberation size factor.  
- \( m \): Density factor for valuable and gangue minerals.  

---

## 💡 Example

### Example 1:
Calculate the mass of the sample with the following parameters:  
- \( d95 \): **2.5 cm**  
- \( f \): **0.5**  
- \( g \): **0.25**  
- \( L \): **1.0 cm**  
- \( a \): **0.3**  
- \( r \): **4.0 g/cm³**  
- \( t \): **2.5 g/cm³**  
- \( σ \): **0.02 g/cm³**

```excel
=SAMPLE.ASSAY(2.5, 0.5, 0.25, 1.0, 0.3, 4.0, 2.5, 0.02)
```

**Result**: `23437.5 g` (approximate value)

---

## 📝 Notes

- Ensure that all input values are in the specified units (e.g., \( d95 \) in cm, \( r \) in g/cm³).
- Use default values for \( f \) and \( g \) if no specific values are provided.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- N/A  

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17