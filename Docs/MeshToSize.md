# 🔁 MESH.TO.SIZE

🔹 **Description**:  
This function converts a **standard mesh number** to its equivalent **micrometer (µm)** value based on predefined standard values.

---

## 📥 Syntax

```excel
=MESH.TO.SIZE(c)
```

---

## 🧾 Parameters

| Parameter         | Type  | Description                              |
|--------------------|-------|------------------------------------------|
| `c` (Mesh Number) | Int   | The standard mesh number (e.g., 100).    |

---

## 🧮 Formula

The function uses a predefined **dictionary** that maps standard mesh numbers to their equivalent sizes in micrometers. For example:
- Mesh Number 4 → 4760 µm
- Mesh Number 100 → 149 µm
- Mesh Number 18000 → 0.82 µm

When provided with a valid mesh number, the function retrieves the corresponding size from the dictionary.

---

## 💡 Example

### Example 1:
Convert a standard mesh number **100** to micrometers.

```excel
=MESH.TO.SIZE(100)
```

**Result**: `149.00 µm`

### Example 2:
Convert a standard mesh number **400** to micrometers.

```excel
=MESH.TO.SIZE(400)
```

**Result**: `37.00 µm`

---

## 📝 Notes

- The function only supports standard mesh numbers included in the predefined list:
  ```
  [4, 6, 8, 10, 12, 14, 16, 20, 24, 28, 32, 35, 42, 48, 60, 65, 80, 100, 115, 150, 
   170, 200, 250, 270, 325, 400, 477, 565, 673, 800, 949, 1346, 1590, 1898, 2280, 
   2690, 3200, 3800, 4480, 5280, 6430, 7590, 9030, 10730, 12780, 18000]
  ```
- If the provided mesh number (`c`) is not in the list, the function will throw an error.
- The function returns `-1` if user authentication fails.

---

📌 **Related Functions**:
- N/A  

---

Created by: [Dr. Alireza Ghasemi](https://github.com/Dr-Alireza-Ghasemi)  
📅 Last updated: 2025-04-17