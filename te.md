# SOLIDPERCENT.MASS.TO.VOL

📌 **Description:**  
This function converts **mass solid percent** to **volume solid percent** in mineral processing calculations.

---

## 🧮 Formula:

\[
\text{Vol\%} = \frac{sp}{\rho} \div \left( \frac{sp}{\rho} + 100 - sp \right) \times 100
\]

Where:
- `sp`: Solid percent (mass-based)
- `ρ (Rho)`: Solid density in **t/m³**

---

## 📥 Parameters:

| Name                | Description                       | Type   |
|---------------------|-----------------------------------|--------|
| `sp`                | Mass solid percent                | Double |
| `Rho`               | Solid density (t/m³)              | Double |

---

## ✅ Example:

```excel
=SOLIDPERCENT.MASS.TO.VOL(40, 2.6)
```

🔁 This converts **40% mass solid** to **volume percent**, assuming solid density is **2.6 t/m³**.

---

## 📎 Notes:
- The function checks for user authentication before execution.
- Returns `-1` if authentication fails.

---

🔗 Back to [Main Documentation](../README.md)
