# 🔁 SAMPLE.CLASSIFICATION

🔹 **Description**:  
This function calculates the **mass of the sample (in grams)** based on particle size, shape factor, mean density, and relative standard deviation.

---

## 📥 Syntax

```excel
=SAMPLE.CLASSIFICATION(d95, f, b, σ)
```

---

## 🧾 Parameters

| Parameter         | Type   | Description                                                                 |
|--------------------|--------|-----------------------------------------------------------------------------|
| `d95`             | Double | The nominal 95% passing size of the particle in the sample (in cm).         |
| `f`               | Double | The shape factor relating volume to the diameter of the particles. Default values: <br> - For general cases: **0.5** <br> - For gold ores: **0.2**. |
| `b`               | Double | The mean density of the mineral (in g/cm³).                                 |
| `σ` (Zigma)       | Double | The relative standard deviation (in g/cm³).                                 |

---

## 🧮 Formula

The mass of the sample is calculated using the following formula:

$$
\text{Sample Mass (g)} = \frac{20.0 \cdot b \cdot f \cdot d95^3}{\sigma^2}
$$

Where:  
- \( d95 \): Nominal 95% passing size of the particle.  
- \( f \): Shape factor for the particles.  
- \( b \): Mean density of the mineral.  
- \( \sigma \): Relative standard deviation.  

---

## 💡 Example

### Example 1:
Calculate the mass of the sample with the following parameters:  
- \( d95 \): **2.5 cm**  
- \( f \): **0.5**  
- \( b \): **4.0 g/cm³**  
- \( σ \): **0.02 g/cm³**

```excel
=SAMPLE.CLASSIFICATION(2.5, 0.5, 4.0, 0.02)
```

**Result**: `625000 g` (approximate value)

---

## 📝 Notes

- Ensure that all input values are in the specified units (e.g., \( d95 \) in cm, \( b \) in g/cm³).
- Use default values for \( f \) if no specific values are provided.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`SAMPLE.ASSAY`](./SampleAssay.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17