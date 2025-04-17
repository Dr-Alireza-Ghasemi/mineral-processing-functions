# 🔁 ROSIN.RAMMLER.D63

🔹 **Description**:  
This function calculates the **D63** (the particle size at which 63% of the material passes) for a size distribution based on the **Rosin-Rammler distribution model** using regression analysis.

---

## 📥 Syntax

```excel
=ROSIN.RAMMLER.D63(s, m)
```

---

## 🧾 Parameters

| Parameter              | Type      | Description                                                                 |
|-------------------------|-----------|-----------------------------------------------------------------------------|
| `s` (Size Array)        | Double[]  | An array of sieve sizes (e.g., [100, 80, 60, 40, 20]).                      |
| `m` (Cumulative Passing Array) | Double[] | An array of cumulative passing percentages corresponding to the sieve sizes (e.g., [0.2, 0.4, 0.6, 0.8, 0.9]). Note that these values should be fractions (e.g., 0.6 for 60%). |

---

## 🧮 Formula

The **D63** is calculated using a logarithmic transformation of the Rosin-Rammler distribution equation and linear regression:

1. **Logarithmic Transformations**:
   - Transform the sieve sizes (`s`) and cumulative passing percentages (`m`) as follows:
     - \( x[i] = \ln(s[i]) \)
     - \( y[i] = \ln(\ln(1 / (1 - m[i]))) \)

2. **Linear Regression**:
   - Perform a linear regression between \( x[i] \) and \( y[i] \):
     - \( y = \text{slope} \times x + \text{intercept} \)

3. **Calculate D63**:
   - Using the regression coefficients:
     - \( D63 = e^{-\text{intercept} / \text{slope}} \)

---

## 💡 Example

### Example 1:
Calculate the **D63** for the following size distribution:  
- Sieve Sizes: **[100, 80, 60, 40, 20]**  
- Cumulative Passing: **[0.2, 0.4, 0.6, 0.8, 0.9]**

```excel
=ROSIN.RAMMLER.D63({100, 80, 60, 40, 20}, {0.2, 0.4, 0.6, 0.8, 0.9})
```

**Result**: `63.00 µm` (approximate value)

---

## 📝 Notes

- Ensure the **cumulative passing percentages** (`m`) are provided as fractions (e.g., 0.6 for 60%).
- The function assumes a Rosin-Rammler model and performs regression to determine the distribution parameters.
- The function uses the `SimpleRegression.Fit` method for linear regression.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`ROSIN.RAMMLER.DIST`](./RosinRammlerDist.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17