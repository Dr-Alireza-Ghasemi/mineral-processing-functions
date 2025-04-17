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
