# EXPERIMENT-01: BUILDING LOGICAL CIRCUITS

## 1. Aim

To design, implement, simplify, and verify combinational logic circuits using Boolean algebra and digital logic gates.

## 2. Boolean Notation

Use the following notation throughout this experiment:

| Symbol | Meaning | Example |
|---|---|---|
| `!A` | NOT A | `!A` |
| `A & B` | AND | `A & B` |
| `A \| B` | OR | `A \| B` |
| `A ^ B` | XOR | `A ^ B` |
| `A XNOR B` | XNOR | `A XNOR B` |

**Important:** In these equations, `!` means NOT, `&` means AND, `|` means OR, and `^` means XOR. Parentheses determine the order of operations.

## 3. Advanced Boolean Equations

### Equation 1: Four-Input Sum-of-Products

```text
F1 = (!A & B & C)
   | (A & B & !D)
   | (!B & C & D)
   | (A & !C & D)
```

**Inputs:** A, B, C, D  
**Output:** F1  
**Challenge:** Simplify the expression and compare gate counts.

### Equation 2: Product-of-Sums Circuit

```text
F2 = (A | !B | C)
   & (!A | B | D)
   & (B | !C | !D)
```

**Inputs:** A, B, C, D  
**Output:** F2  
**Challenge:** Implement the circuit using NAND gates and verify functional equivalence.

### Equation 3: Nested Complement Logic

```text
F3 = !(
       ((! (A | B)) | (C & D))
       &
       (A | (!(B | C)))
     )
```

**Inputs:** A, B, C, D  
**Output:** F3  
**Challenge:** Apply De Morgan's theorems and implement the circuit using NAND and NOR gates.

### Equation 4: XOR-XNOR Combinational Circuit

```text
F4 = ((A XOR B) & (C XNOR D))
   | (!A & B & (C XOR D))
```

**Inputs:** A, B, C, D  
**Output:** F4  
**Challenge:** Compare an XOR/XNOR implementation with a basic-gate implementation.

### Equation 5: Five-Input Logic Function

```text
F5 = (A & B & !C)
   | (!A & D & E)
   | (B & C & !E)
   | (!B & C & D)
```

**Inputs:** A, B, C, D, E  
**Output:** F5  
**Challenge:** Generate and verify all 32 input combinations.

### Equation 6: Six-Input Mixed Logic

```text
F6 = ((A | B) & !(C | D))
   | ((C XOR E) & (D | G))
   | (!A & B & E)
```

**Inputs:** A, B, C, D, E, G  
**Output:** F6  
**Challenge:** Calculate gate count and logic depth. Verify all 64 input combinations.

### Equation 7: NAND-NOR Hybrid Logic

```text
F7 = (! (A & B) & !(C | D))
   | (!(A | C) & B & D)
```

**Inputs:** A, B, C, D  
**Output:** F7  
**Challenge:** Implement the function using NAND and NOR gates with any required input inversions.

### Equation 8: Six-Input Advanced Combinational Logic

```text
F8 = ((A XOR B) & (C XNOR D))
   | (!(A | B) & C & E)
   | (A & B & !(D | F))
```

**Inputs:** A, B, C, D, E, F  
**Output:** F8  
**Challenge:** Simplify the expression, design the circuit, and verify all 64 input combinations.

## 4. Experimental Procedure

1. Identify all input variables and the output.
2. Draw the logic circuit for each equation.
3. Implement the circuit in Logisim Evolution, Proteus, or a digital logic trainer kit.
4. Apply all possible input combinations.
5. Record the expected and observed outputs.
6. Simplify the Boolean expression using Boolean algebra.
7. Build the simplified circuit and compare gate counts.
8. Save the circuit diagrams, truth tables, and verification screenshots.

## 5. Truth Table Requirements

| Number of inputs | Required combinations |
|---:|---:|
| 4 | 16 |
| 5 | 32 |
| 6 | 64 |

Use this format to record the results:

| Inputs | Expected output | Observed output | Status |
|---|---|---|---|
| 0000 |  |  |  |
| 0001 |  |  |  |
| 0010 |  |  |  |
| ... |  |  |  |

Extend the table to include every input combination required by each equation.

## 6. Performance Analysis

For each circuit, record:

- Number of AND gates
- Number of OR gates
- Number of NOT gates
- Number of XOR/XNOR gates
- Total gate count
- Logic depth
- Functional equivalence before and after simplification

## 7. Expected Results (drop the screenshots of each equations circuit )
Equation 1: F1 F1 = (!A & B & C) | (A & B & !D) | (!B & C & D) | (A & !C & D) Shown with inputs A=0, B=0, C=1, D=1  ->  F1 = 1
<img width="1200" height="610" alt="image" src="https://github.com/user-attachments/assets/6b37862c-e1ac-411c-9404-de8c20015af7" />

Equation 2: F2 F2 = (A | !B | C) & (!A | B | D) & (B | !C | !D) Shown with inputs A=0, B=0, C=0, D=0  ->  F2 = 1
<img width="1174" height="591" alt="image" src="https://github.com/user-attachments/assets/d1af81c5-b897-4a2c-b064-c106e4de5dc7" />

Equation 3: F3 F3 = !( ((!(A | B)) | (C & D)) & (A | (!(B | C))) ) Shown with inputs A=0, B=0, C=1, D=0  ->  F3 = 1

<img width="1168" height="526" alt="image" src="https://github.com/user-attachments/assets/2da8ab8a-a349-4734-877d-4ce184245458" />

Equation 4: F4 F4 = ((A XOR B) & (C XNOR D)) | (!A & B & (C XOR D)) Shown with inputs A=0, B=1, C=0, D=0  ->  F4 = 1
<img width="1166" height="574" alt="image" src="https://github.com/user-attachments/assets/dd550db0-72a8-4ca2-aa53-610d99afc3c6" />

Equation 5: F5 F5 = (A & B & !C) | (!A & D & E) | (B & C & !E) | (!B & C & D) Shown with inputs A=0, B=0, C=0, D=1, E=1  ->  F5 = 1
<img width="1181" height="581" alt="image" src="https://github.com/user-attachments/assets/6670f4bc-212e-4450-ae4e-036f47af1ec9" />

Equation 6: F6 F6 = ((A | B) & !(C | D)) | ((C XOR E) & (D | G)) | (!A & B & E) Shown with inputs A=0, B=0, C=0, D=0, E=1, G=1  ->  F6 = 1
<img width="1162" height="634" alt="image" src="https://github.com/user-attachments/assets/3edd2f41-c145-454b-b963-b3957b2ef1ab" />

Equation 7: F7 F7 = (!(A & B) & !(C | D)) | (!(A | C) & B & D) Shown with inputs A=0, B=0, C=0, D=0  ->  F7 = 1
 <img width="1191" height="632" alt="image" src="https://github.com/user-attachments/assets/608bd83a-56d1-422c-8307-407dda15fa0d" />

Equation 8: F8 F8 = ((A XOR B) & (C XNOR D)) | (!(A | B) & C & E) | (A & B & !(D | F)) Shown with inputs A=0, B=0, C=1, D=0, E=1, F=0  ->  F8 = 1
<img width="1188" height="590" alt="image" src="https://github.com/user-attachments/assets/cf7c75b3-7120-4b13-a60d-669acadb0d10" />


 
## 8. Result

The logic circuits are designed, implemented, and verified using Boolean algebra and digital logic gates. The original and simplified circuits are compared based on gate count and logic depth.
 
 
