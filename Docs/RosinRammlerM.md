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
