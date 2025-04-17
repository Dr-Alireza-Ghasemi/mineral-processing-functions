# 🔁 SIZE.TO.MESH

🔹 **Description**:  
This function converts a **standard sieve size** in micrometers (**µm**) to its equivalent **mesh number** based on predefined standard values.

---

## 📥 Syntax

```excel
=SIZE.TO.MESH(c)
```

---

## 🧾 Parameters

| Parameter         | Type  | Description                              |
|--------------------|-------|------------------------------------------|
| `c` (Size)        | Double | The standard sieve size in micrometers (**µm**) (e.g., 149.00). |

---

## 🧮 Formula

The function uses a predefined **dictionary** that maps standard sieve sizes (in micrometers) to their equivalent mesh numbers. For example:
- Sieve Size 4760 µm → Mesh Number 4
- Sieve Size 149 µm → Mesh Number 100
- Sieve Size 0.82 µm → Mesh Number 18000

When provided with a valid sieve size, the function retrieves the corresponding mesh number from the dictionary.

---

## 💡 Example

### Example 1:
Convert a standard sieve size **149 µm** to a mesh number.

```excel
=SIZE.TO.MESH(149)
```

**Result**: `100`

### Example 2:
Convert a standard sieve size **37 µm** to a mesh number.

```excel
=SIZE.TO.MESH(37)
```

**Result**: `400`

---

## 📝 Notes

- The function only supports standard sieve sizes included in the predefined list:
  ```
  [4760.00, 3360.00, 2380.00, 1680.00, 1410.00, 1190.00, 1000.00, 840.00, 
   710.00, 590.00, 500.00, 420.00, 350.00, 297.00, 250.00, 210.00, 177.00, 
   149.00, 125.00, 105.00, 88.00, 74.00, 62.00, 53.00, 44.00, 37.00, 31.00, 
   26.20, 22.00, 18.50, 15.60, 11.00, 9.30, 7.80, 6.50, 5.50, 4.60, 3.90, 
   3.30, 2.80, 2.30, 1.95, 1.65, 1.38, 1.16, 0.82]
  ```
- If the provided sieve size (`c`) is not in the list, the function will throw an error.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- [`MESH.TO.SIZE`](./MeshToSize.md)

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17