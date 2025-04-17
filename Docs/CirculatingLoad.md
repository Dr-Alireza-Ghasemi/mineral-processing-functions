# 🔁 CIRCULATINGLOAD

🔹 **Description**:  
This function calculates the **circulating load** of a grinding circuit using linear regression analysis of size class weight fractions in feed, underflow, and overflow streams.

---

## 📥 Syntax

```excel
=CIRCULATINGLOAD(f, u, o)
```

---

## 🧾 Parameters

| Parameter          | Type      | Description                                                                 |
|---------------------|-----------|-----------------------------------------------------------------------------|
| `f` (Feed Weight Fraction) | Double[]  | An array of weight fractions (or percentages) in each size class of the feed stream. |
| `u` (Underflow Weight Fraction) | Double[]  | An array of weight fractions (or percentages) in each size class of the underflow stream. |
| `o` (Overflow Weight Fraction) | Double[]  | An array of weight fractions (or percentages) in each size class of the overflow stream. |

---

## 🧮 Formula

The circulating load is calculated using the following steps:

1. **Determine Differences for Each Size Class**:
   - \( y[i] = f[i] - o[i] \)
   - \( x[i] = u[i] - f[i] \)

2. **Perform Linear Regression**:
   - Fit a linear regression line to the data points \( (x[i], y[i]) \):
     - \( y = \text{slope} \cdot x + \text{intercept} \)

3. **Circulating Load**:
   - The **circulating load** is the slope of the regression line:
     - \( \text{Circulating Load} = \text{slope} \)

---

## 💡 Example

### Example 1:
Calculate the circulating load for the following weight fractions:  
- Feed: **[0.4, 0.6, 0.8]**  
- Underflow: **[0.5, 0.7, 0.9]**  
- Overflow: **[0.3, 0.4, 0.5]**

```excel
=CIRCULATINGLOAD({0.4, 0.6, 0.8}, {0.5, 0.7, 0.9}, {0.3, 0.4, 0.5})
```

**Result**: `1.25` (approximate value)

---

## 📝 Notes

- Ensure the arrays `f`, `u`, and `o` have the same length.
- The function uses the `SimpleRegression.Fit` method to compute the regression line.
- The circulating load is expressed as a ratio or percentage.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- N/A  

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17