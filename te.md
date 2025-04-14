# SOLIDPERCENT.MASS.TO.VOL

📌 **Description:**  
This function converts **mass solid percent** to **volume solid percent** in mineral processing calculations.

---

## Formula:

`Volume% = (sp / Rho) / (sp / Rho + 100 - sp) * 100`

Where:
- `sp`: Solid percent (mass-based)
- `Rho`: Solid density in t/m³

---

## Parameters:

| Name  | Description            | Type   |
|-------|------------------------|--------|
| `sp`  | Mass solid percent     | Double |
| `Rho` | Solid density (t/m³)   | Double |

---

## Example:

```excel
=SOLIDPERCENT.MASS.TO.VOL(40, 2.6)
