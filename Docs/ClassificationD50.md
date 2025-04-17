# 🔁 CLASSIFICATION.D50

🔹 **Description**:  
This function calculates the **D50** of a size distribution, which is the particle size at which 50% of the material passes through.

---

## 📥 Syntax

```excel
=CLASSIFICATION.D50(s, m)
```

---

## 🧾 Parameters

| Parameter              | Type      | Description                                                                 |
|-------------------------|-----------|-----------------------------------------------------------------------------|
| `s` (Size Array)        | Double[]  | An array of sieve sizes (e.g., [100, 80, 60, 40, 20]).                      |
| `m` (Cumulative Passing Array) | Double[] | An array of cumulative passing percentages corresponding to the sieve sizes (e.g., [95, 85, 65, 40, 20]). |


---

## 💡 Example

### Example 1:
Calculate the **D50** for the following size distribution:  
- Sieve Sizes: **[100, 80, 60, 40, 20]**  
- Cumulative Passing: **[95, 85, 65, 40, 20]**

```excel
=CLASSIFICATION.D50({100, 80, 60, 40, 20}, {95, 85, 65, 40, 20})
```

**Result**: `53.33 µm` (Interpolated value)

### Example 2:
Calculate the **D50** for the following size distribution:  
- Sieve Sizes: **[200, 150, 100, 50]**  
- Cumulative Passing: **[90, 70, 50, 30]**

```excel
=CLASSIFICATION.D50({200, 150, 100, 50}, {90, 70, 50, 30})
```

**Result**: `100 µm`

---

## 📝 Notes

- Ensure the `Size Array` is sorted in descending order.
- The `Cumulative Passing Array` must correspond to the sieve sizes in `Size Array`.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`PARTICLE.SIZE.DISTRIBUTION`](./ParticleSizeDistribution.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17
