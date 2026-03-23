# Journey Towards IRAM
### Sequential 2x2 Matrix Multiplier — Logisim Evolution

© 2026 ZayenCompiler — Original Work  
github.com/ZayenCompiler

---

## What This Is

A 2x2 matrix multiplier built from scratch in Logisim Evolution.  
Built progressively across three stages:

| Circuit | Description |
|---|---|
| Core_2x2 | Raw combinational multiply core |
| ROM_Matrix_Multiplication_2x2 | Core + ROM controlled signals |
| IRAM_Matrix_Multiplication_2x2 | Core + Instruction RAM + Program Counter |

---

## How To Use

1. Download and install Logisim Evolution
2. Clone this repo
3. Open `circuits/Journey_Towards_IRAM.circ`
4. Select the circuit you want from the left panel
5. Load RAM values from `/excel/` folder into RAM A and RAM B
6. Load instruction set values into Instruction RAM
7. Run simulation

---

## Instruction Set

16-bit instruction word.

| Bits | Purpose |
|---|---|
| 15 | COMPUTE flag |
| 14 | STORE flag |
| 13-4 | Direct WE control signals |
| 3-0 | Spare / future use |

Full instruction set documented in `/docs/instruction_set.md`

---

## Repo Structure
```
/circuits   → Logisim .circ files
/excel      → RAM input templates and instruction set
/docs       → Instruction set reference
```

---

## Requirements

- Logisim Evolution 4.x
- Java 11 or higher

---

Built as a personal learning project.  
Part of a larger series building toward a full sequential matrix multiplier.