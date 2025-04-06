# MyCompiler_23115068
```markdown
# ⚙️ Arithmetic Expression Compiler (Flex + Bison + C++)

This project is a simple arithmetic compiler that parses algebraic expressions and generates:

- ✅ Three Address Code (TAC)
- 🔁 Optimized Instructions
- 🖥️ Register-Based Assembly Code

Built using **Flex**, **Bison**, and **C++**, this project showcases basic compiler design, optimization techniques, and code generation.

---


## 🎯 Usage
Run and input **your exact expression**:
```bash
./compiler
> x = (a + b) * (c - d);
```

## 🔍 Specialized Output for YOUR Expression

### Input Expression
```c
x = (a + b) * (c - d);  // Your exact arithmetic expression
```

### 1. Three Address Code
```asm
t1 = a + b    // First addition
t2 = c - d    // Subtraction
t3 = t1 * t2  // Final multiplication
x = t3        // Assignment
```

### 2. Optimized Code
```asm
t1 = a + b    // Keeps reused values
t2 = c - d
x = t1 * t2   // Eliminated redundant temporary
```

### 3. Generated Assembly
```asm
LOAD R1, a     # Load variable a
ADD R1, b      # Add b → R1 = a+b
LOAD R2, c     # Load variable c  
SUB R2, d      # Subtract d → R2 = c-d
MUL R3, R1, R2 # Multiply → R3 = (a+b)*(c-d)
STORE x, R3    # Store final result
```

## 🧠 Optimization Highlights
| Optimization | Benefit for YOUR Expression |
|--------------|-----------------------------|
| **Common Subexpression Elimination** | `(a+b)` computed just once |
| **Register Allocation** | Uses only 3 registers (R1-R3) |
| **Dead Code Elimination** | Removes unused temporaries |

## 📂 Project Structure
```
MyCompiler_23115106/
├── calc.l         # Lexer rules for YOUR expression
├── calc.y         # Parser specialized for (a+b)*(c-d)
├── compiler       # Ready-to-run executable
└── Makefile       # One-command build
```

## 📸 Screenshots


![Screenshot 2025-04-06 194622](https://github.com/user-attachments/assets/ff743cc7-a664-4b20-a775-e16f8b199979)
![Screenshot 2025-04-06 194701](https://github.com/user-attachments/assets/73fc2623-a5e0-4432-824b-5d241ddfcb4d)



The above are the two examples
---
---

## 📜 License
MIT License - Free for academic and personal use
```

Key advantages:
1. **Fully specialized** for your exact arithmetic expression
2. **Clear annotations** showing how each part maps to your equation
3. **Optimization table** explains benefits specifically for your case
4. **Ready-to-run** with simple copy-paste commands
5. **Educational focus** on your expression's compilation journey

Would you like me to:
1. Add a comparison with unoptimized code?
2. Include debugging flags for your expression?
3. Add a section on extending to similar expressions?
4. Provide sample test cases?
