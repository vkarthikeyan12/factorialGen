# ALGOL Programming Examples

This repository contains classic **ALGOL programs** demonstrating fundamental programming concepts such as recursion, iteration, and basic algorithmic calculations. The examples include **Factorial Calculators** and **Fibonacci sequences** implemented in both **ALGOL 60** and **ALGOL 68**.

---

## Contents

- **Factorial Calculator (Recursive & Iterative)**
  - Computes factorials of a non-negative integer.
  - Demonstrates both recursive and iterative approaches.
  - Versions:
    - ALGOL 60 (`factorial_algol60.alg`)
    - ALGOL 68 (`factorial_algol68.a68`)

- **Fibonacci Sequence**
  - Generates Fibonacci numbers up to a specified term.
  - Versions:
    - ALGOL 60 (`fibonacci_algol60.alg`)
    - ALGOL 68 (`fibonacci_algol68.a68`)

---

## Features

- Recursive procedure examples
- Iterative loop examples
- Input/output using standard ALGOL procedures
- Educational exploration of ALGOL 60 vs ALGOL 68 syntax

---

## Example Output

### Factorial Calculator (n = 5)

```
Factorial using recursion: 120
Factorial using iteration: 120
```

### Fibonacci Sequence (n = 10)

```
0 1 1 2 3 5 8 13 21 34
```

---

## Getting Started

### Prerequisites

- **ALGOL 60** or **ALGOL 68** interpreter/compiler
  - Online options:
    - [TIO – ALGOL 60](https://tio.run/#algol60)
    - [TIO – ALGOL 68](https://tio.run/)
  - Local option:
    - [Algol 68 Genie](https://jmvdveer.github.io/algol68toc/)

### Running the Programs

#### ALGOL 60

1. Save the code with `.alg` extension, e.g., `factorial_algol60.alg`.
2. Run using an ALGOL 60 interpreter or online TIO.
3. Input the required number when prompted.

#### ALGOL 68

1. Save the code with `.a68` extension, e.g., `factorial_algol68.a68`.
2. Run using Algol 68 Genie:
   ```bash
   a68g factorial_algol68.a68
   ```
3. Enter the input when prompted.

---

## Example Code Snippet (ALGOL 68 – Factorial)

```algol
print("Enter a non-negative integer: ");
INT n;
read(n);

PROC fact_rec = (INT x)INT:
    IF x = 0 THEN 1 ELSE x * fact_rec(x - 1) FI;

PROC fact_iter = (INT x)INT:
(
    INT result := 1;
    FOR i FROM 1 TO x DO
        result := result * i
    OD;
    result
);

INT factorial_rec := fact_rec(n);
INT factorial_iter := fact_iter(n);

print("Factorial using recursion: "); print(factorial_rec); newline;
print("Factorial using iteration: "); print(factorial_iter); newline;
```

---

## Notes

- **ALGOL 60 vs ALGOL 68**
  - ALGOL 60 uses `comment ... ;`, `integer procedure`, and `for ... step ... until`.
  - ALGOL 68 uses `# comment #`, `PROC name = (args) type:`, and `FOR ... FROM ... TO ... DO ... OD`.
- **Print/Output**
  - ALGOL 68’s `print` only takes a single argument, so multiple `print` statements are needed for combined output.

---

## File Extensions

| Version    | Recommended Extension |
|------------|---------------------|
| ALGOL 60   | `.alg`              |
| ALGOL 68   | `.a68`              |

---

## License

This repository is for **educational purposes**. You may freely use, modify, and share the code.

---

## References

- [ALGOL 68 Genie Documentation](https://jmvdveer.github.io/algol68toc/)  
- [Try It Online – ALGOL 60](https://tio.run/#algol60)  
- [Try It Online – ALGOL 68](https://tio.run/)
