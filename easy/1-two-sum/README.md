# 1. Two Sum

### Problem Summary (Rephrased)
Given a list of integers and a target value, find the indices of the two numbers that add up exactly to that target.  
You can assume there is exactly one valid pair, and you may not use the same element twice.

---

### Approach and Reasoning

We can solve this efficiently using a hash map (dictionary in Python) to store numbers we have already seen and their indices.

- As we iterate through the list:
  1. Compute the **complement** (this is the number needed to reach the target value).
  2. Check if we have already seen that complement.
  3. If yes -> we have found the pair -> return their indices.
  4. If not -> store the current **num** and its index.

---

### Time and Space Complexity
- **Time** O(n) - each number is checked once
- **Space** O(n) - to store numbers in the dictionary