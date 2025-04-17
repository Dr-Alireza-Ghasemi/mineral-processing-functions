# 🔁 PARTICLE.SIZE.DISTRIBUTION

🔹 **Description**:  
This function calculates the **Cumulative Passing Size Distribution** from the raw data provided from sieving. The input array should be sorted from the largest to smallest sieve size.

---

## 📥 Syntax

```excel
=PARTICLE.SIZE.DISTRIBUTION(c)
```

---

## 🧾 Parameters

| Parameter              | Type      | Description                                                                 |
|-------------------------|-----------|-----------------------------------------------------------------------------|
| `c` (On-Sieves Weight Array) | Double[] | The raw weight data from sieves. This array must be sorted from largest to smallest sieve size. |

---

## 🧮 Formula

The cumulative passing distribution is calculated as follows:

### Step 1: Determine Total Weight
$$
\text{Total Weight} = \sum c[i]
$$

### Step 2: Calculate Cumulative Percent Passing
For each sieve, calculate the cumulative percent passing as:

$$
\text{Cumulative Percent Passing}[i] = 100 - \left( \frac{c[i]}{\text{Total Weight}} \times 100 \right)
$$

Where:  
- `c[i]` is the weight retained on the sieve at index `i`.

### Step 3: Store Results
The results are rounded to 4 decimal places and returned as a 2D array.

---

## 💡 Example

Calculate the cumulative passing size distribution for the following weights retained on sieves (in grams):  
- Input Array: **[40, 30, 20, 10]**

```excel
=PARTICLE.SIZE.DISTRIBUTION({40, 30, 20, 10})
```

**Result**:  
| Cumulative Percent Passing (%) |
|--------------------------------|
| 60.0000                        |
| 90.0000                        |
| 96.6667                        |
| 100.0000                       |

---

## 📝 Notes

- Ensure the input array is sorted in descending order (largest to smallest sieve size).
- The function will return a 2D array representing cumulative passing percentages.
- The function will return `null` if user authentication fails.

---

📌 **Related Functions**:
- N/A  

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17