# 🔁 ROSIN.RAMMLER.M

🔹 **Description**:  
This function calculates the **uniformity constant (m)** of the **Rosin-Rammler distribution**, which describes the spread of particle sizes in a distribution.

---

## 📥 Syntax

```excel
=ROSIN.RAMMLER.M(s, m)
```

---

## 🧾 Parameters

| Parameter              | Type      | Description                                                                 |
|-------------------------|-----------|-----------------------------------------------------------------------------|
| `s` (Size Array)        | Double[]  | An array of sieve sizes (e.g., [100, 80, 60, 40, 20]).                      |
| `m` (Cumulative Passing Array) | Double[] | An array of cumulative passing percentages corresponding to the sieve sizes (e.g., [20, 40, 60, 80, 90]). |

---

## 🧮 Formula

The function calculates the **uniformity constant (m)** using a logarithmic transformation and linear regression:

1. **Logarithmic Transformations**:
   - Transform the sieve sizes (`s`) and cumulative passing percentages (`m`) as follows:
     - \( x[i] = \ln(s[i]) \)
     - \( y[i] = \ln(\ln(1 / (1 - m[i] / 100))) \)

2. **Linear Regression**:
   - Perform linear regression between \( x[i] \) and \( y[i] \):
     - \( y = \text{slope} \times x + \text{intercept} \)

3. **Uniformity Constant**:
   - The **uniformity constant (m)** is given by the slope of the regression line:
     - \( m = \text{slope} \)

---

## 💡 Example

### Example 1:
Calculate the **uniformity constant (m)** for the following size distribution:  
- Sieve Sizes: **[100, 80, 60, 40, 20]**  
- Cumulative Passing: **[20, 40, 60, 80, 90]**

```excel
=ROSIN.RAMMLER.M({100, 80, 60, 40, 20}, {20, 40, 60, 80, 90})
```

**Result**: `1.65` (approximate value)

---

## 📝 Notes

- Ensure the **cumulative passing percentages** (`m`) are provided as percentages (e.g., 60 for 60%).
- The function assumes a Rosin-Rammler model and performs regression to determine the uniformity constant.
- The function uses the `SimpleRegression.Fit` method for linear regression.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`ROSIN.RAMMLER.D63`](./RosinRammlerD63.md)
- [`ROSIN.RAMMLER.DIST`](./RosinRammlerDist.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17