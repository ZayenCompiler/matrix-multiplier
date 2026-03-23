# Instruction Set — IRAM Matrix Multiplier 2x2

## Instruction Word Format (16-bit)
Each column group represents one hex nibble.

| Bits 15-12 | Bits 11-8 | Bits 7-4 | Bits 3-0 |
|------------|-----------|----------|----------|
| Control    | WE RAM B  | WE RAM A | Spare    |

## Instructions

| Addr | Hex  | Operation                    |
|------|------|------------------------------|
| 0    | 0110 | LOAD — activate bit 8 + 4    |
| 1    | 0220 | LOAD — activate bit 9 + 5    |
| 2    | 0440 | LOAD — activate bit 10 + 6   |
| 3    | 0880 | LOAD — activate bit 11 + 7   |
| 4    | 1000 | signal — bit 12              |
| 5    | 0000 | NOP                          |
| 6    | 2000 | signal — bit 13              |
| 7    | 0000 | NOP                          |
| 8    | 4000 | signal — bit 14              |
| 9    | 0000 | NOP                          |
| 10   | 8000 | COMPUTE — bit 15             |

## Notes
- RAM C has constant 1 on WE — values write automatically
- No dedicated STORE instruction needed
- Control buffer activates on bit 0 of respective group