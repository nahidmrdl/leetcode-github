# 2. Reverse String

### Problem Summary (Rephrased)
You are given an array of characters that represents a string.  
Modify the array **in-place** so that the characters appear in reverse order.  
You must perform this operation using only **O(1)** extra memory.

---

### Approach and Reasoning

We can reverse the string by **swapping characters from both ends toward the center**.

- Use two pointers:
  - One (`left`) starts at the beginning of the array.
  - Another (`right`) starts at the end.
- While `left < right`:
  1. Swap `s[left]` and `s[right]`.
  2. Move both pointers closer to the center (`left += 1`, `right -= 1`).
- All characters are reversed in-place without using extra space.

---

### Time and Space Complexity
- **Time:** O(n) - each character is visited once.  
- **Space:** O(1) - only a few variables are used regardless of input size.