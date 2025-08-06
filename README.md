# Build-a-Basic-Calculator
A calculator that performs addition and subtraction operations using stacks.

---

## 🔍 Basic Idea:
- We are going to perform addition of numbers with `+` and `-` signs.
- Consecutive digits following a `+` sign (or before a `-`) are added.
- Consecutive digits following a `-` sign (or before the next `+`) are subtracted.

---

## 🧠 Variables Used:
1. `stack` – Keeps track of numbers and signs inside brackets.    
2. `res` – Stores the final result/output.  
3. `num` – Temporarily stores a number (e.g., 123, 3, 45, 45688, etc.).  
4. `sign` – Tracks the sign (`+` or `-`) of the current number.

---

## 🛠️ Logic Breakdown (3 Key Steps):

### (1) Digit Detection:
- Check if a character in the string is a digit.
- If it's a digit, keep iterating until all consecutive digits are processed.
  - For example: If the string contains `'456'`, store it as `456` (not `4 + 5 + 6`).

### (2) Sign Handling (`+` / `-`):
- Multiply `num` with the current `sign` and add it to `res`.
- Reset `num = 0` for the next number.
- Update `sign` based on the current operator:
  - If `+`, set `sign = +1`
  - If `-`, set `sign = -1`

### (3) Bracket Handling:
- Use a stack to:
  - Store the current result (`res`)
  - Store the current sign (`sign`)
- Reset `res = 0` to evaluate the expression inside the bracket.
- When a closing bracket `)` is encountered:
  - Multiply the result inside the bracket with the sign popped from the stack.
  - Add the stored result from before the bracket to the current result.

---

       

    

    

