# 🔁 RTD.INV.WELLER

🔹 **Description**:  
This function estimates the **Weller RTD (Residence Time Distribution) Parameters** based on experimental concentration data and corresponding time values.

---

## 📥 Syntax

```excel
=RTD.INV.WELLER(Time, Conc.)
```

---

## 🧾 Parameters

| Parameter       | Type           | Description                                                                 |
|------------------|----------------|-----------------------------------------------------------------------------|
| `Time`          | Array of Doubles | The array of time values (e.g., experimental time points).                   |
| `Conc.`         | Array of Doubles | The array of experimental concentration values corresponding to the time points. |

---

## 🧮 Functionality

The function uses numerical optimization to calculate the following **Weller RTD Parameters**:  
- \( T_l \): **Longitudinal dispersion time**  
- \( T_s \): **Short-circuiting time**  
- \( T_{pf} \): **Peak flow time**

### Key Steps:
1. **Preprocessing**:  
   The concentration values are normalized, and the area under the curve is calculated using the trapezoidal rule.

2. **Model Definition**:  
   The following model is used for fitting:  
   $$
   \text{Model}(t) = \left(B \cdot e^B - A \cdot e^B + A \cdot e^{B \cdot \frac{T_s}{T_l}}\right) \cdot \frac{A}{T_l}
   $$
   Where:  
   - \( A = \frac{T_l}{T_l - T_s} \)  
   - \( B = \frac{-(t - T_{pf})}{T_s} \)

3. **Objective Function**:  
   The sum of squared errors between the experimental and model data is minimized:  
   $$
   \text{Error} = \sum \left[ y_i - \text{Model}(t_i) \cdot \text{Area} \right]^2
   $$

4. **Optimization**:  
   - Nelder-Mead Simplex optimization is used to find the best parameters \( T_l \), \( T_s \), and \( T_{pf} \) by minimizing the objective function.
   - Constraints ensure valid parameter values (e.g., \( T_l > T_s > 0 \)).

5. **Output**:  
   The optimized values of \( T_l \), \( T_s \), and \( T_{pf} \) are returned.

---

## 💡 Example

### Example 1:
Estimate the Weller RTD Parameters for the following data:  
- **Time**: `{1, 2, 3, 4, 5, 6, 7, 8}`  
- **Concentration**: `{0.2, 0.5, 0.8, 0.9, 0.7, 0.4, 0.1, 0.05}`

```excel
=RTD.INV.WELLER({1, 2, 3, 4, 5, 6, 7, 8}, {0.2, 0.5, 0.8, 0.9, 0.7, 0.4, 0.1, 0.05})
```

**Result**:  
```
Tl=   2.5  
Ts=   0.5  
Tpf=  3.0
```

---

## 📝 Notes

- Ensure that the `Time` and `Conc.` arrays have equal lengths.
- The function returns the optimized parameters \( T_l \), \( T_s \), and \( T_{pf} \) as a 2D Excel array.
- The optimization process may not converge if the experimental data is insufficient or noisy.

---

📌 **Related Functions**:
- N/A  

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17