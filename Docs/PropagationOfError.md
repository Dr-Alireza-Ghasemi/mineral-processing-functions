# ⚙️ PROPAGATION.OF.ERROR

🔍 **Description**:  
This function computes the **propagation of uncertainty** using numerical differentiation, based on measured values (`Xi`) and their associated standard deviations (`Sxi`). The propagated uncertainty is calculated for the result of a function (`F`) and returned in a specified output cell (`Out`).

---

## 📥 Syntax

```excel
=PROPAGATION.OF.ERROR(Xi, Sxi, F, Out)
```

---

## 🧾 Parameters

| Parameter   | Type    | Description                                                                 |
|-------------|---------|-----------------------------------------------------------------------------|
| `Xi`        | Range   | Range of input cells containing measured values.                           |
| `Sxi`       | Range   | Range of standard deviation values associated with `Xi`.                   |
| `F`         | Cell    | The cell containing the function result that depends on `Xi`.              |
| `Out`       | Cell    | The cell where the propagated uncertainty of the function result is stored. |

---

## 🧮 Formula

The function calculates the propagated uncertainty using the following formula:

\[
\text{Uncertainty} = \sqrt{\sum_{i=1}^{n} \left( \frac{\partial f}{\partial x_i} \cdot \sigma_{x_i} \right)^2}
\]

Where:  
- \( x_i \): Each value in `Xi`.  
- \( \sigma_{x_i} \): Standard deviation of \( x_i \) from `Sxi`.  
- \( \frac{\partial f}{\partial x_i} \): Numerical derivative of the function with respect to \( x_i \).

---

## 💡 Examples

### Example 1:
Calculate the propagated uncertainty for the following data:  
- **Measured Values (`Xi`)**: `{5, 10, 15}`  
- **Standard Deviations (`Sxi`)**: `{0.1, 0.2, 0.3}`  

The function result (`F`) is in cell `C1`, and the propagated uncertainty will be stored in cell `D1`.

```excel
=PROPAGATION.OF.ERROR(A1:A3, B1:B3, C1, D1)
```

### Example 2:
- **Measured Values (`Xi`)**: `{3, 7, 11}`  
- **Standard Deviations (`Sxi`)**: `{0.05, 0.15, 0.25}`  

```excel
=PROPAGATION.OF.ERROR(A1:A3, B1:B3, C2, D2)
```

---

## 📝 Notes

- The `Xi` and `Sxi` ranges **must have the same length**; otherwise, an error is returned.  
- The `F` cell must contain a valid formula dependent on `Xi`.  
- If inputs are not valid, the function will return `"Inputs must be cell ranges"`.  
- The function uses numerical differentiation with a small increment (\( h = 10^{-6} \)).  

---

📌 **Related Functions**:
- [`CLASSIFICATION.D50`](./ClassificationD50.md)
- [`CYCLONE.CAPACITY`](./CycloneCapacity.md)

---

🛠️ **Created by**: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 **Last updated**: 2025-05-05
