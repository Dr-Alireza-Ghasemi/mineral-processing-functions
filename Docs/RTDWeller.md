# 🔁 RTD.WELLER

🔹 **Description**:  
This function calculates the **Weller RTD (Residence Time Distribution)** based on the given time and parameters \( T_{pf} \), \( T_s \), and \( T_l \).

---

## 📥 Syntax

```excel
=RTD.WELLER(Time, Tpf, Ts, Tl)
```

---

## 🧾 Parameters

| Parameter       | Type           | Description                                                                 |
|------------------|----------------|-----------------------------------------------------------------------------|
| `Time`          | Double         | The time value for which the RTD is calculated.                             |
| `Tpf`           | Double         | The peak flow time.                                                         |
| `Ts`            | Double         | The short-circuiting time.                                                  |
| `Tl`            | Double         | The longitudinal dispersion time.                                           |


---

## 💡 Example

### Example 1:
Calculate the Weller RTD for the following parameters:  
- Time (\( t \)): **5 seconds**  
- Peak flow time (\( Tpf \)): **3 seconds**  
- Short-circuiting time (\( Ts \)): **0.5 seconds**  
- Longitudinal dispersion time (\( Tl \)): **2 seconds**

```excel
=RTD.WELLER(5, 3, 0.5, 2)
```

**Result**:  
The RTD value for the given parameters.

---

## 📝 Notes

- Ensure that \( T_l > T_s > 0 \) for the formula to work correctly.
- The function returns `-1` if user authentication fails.
- Exponential terms are used in the formula, so ensure the input values are within a reasonable range to avoid numerical instability.

---

📌 **Related Functions**:
- [`RTD.INV.WELLER`](./RTDInvWeller.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17
