# 20. Valid Parentheses

### Problem Summary (Rephrased)
You're given a string that contains only brackets: `()`, `{}`, and `[]`.  
Your task is to check if the bracket sequence is properly balanced.

A string is valid when:
- Every opening bracket has a matching closing bracket of the same type.
- Brackets close in the correct order (the most recent open must close first).
- There are no unmatched or wrongly ordered brackets.

---

### Approach and Reasoning
This problem uses a stack to track brackets that still need to be closed.

Steps:
1. Loop through each character in the string.
2. If it's an opening bracket, push it onto the stack.
3. If it's a closing bracket:
   - Check if the stack is not empty and the top matches the correct opening bracket.
   - If it matches -> pop from the stack.
   - If it does not match -> the string is invalid.
4. At the end, the string is valid only if the stack is empty.

Early optimization:
- If the string length is odd, it cannot be valid because brackets always come in pairs.

---

### Time and Space Complexity
- Time: O(n) - each character is processed once
- Space: O(n) - in the worst case when all characters are opening brackets
