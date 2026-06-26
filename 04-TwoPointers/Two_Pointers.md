# Two Pointers

## What are Two Pointers?

Two Pointers is a technique where two variables (pointers) traverse a data structure simultaneously to solve a problem efficiently.

Depending on the problem, the pointers may move towards each other or in the same direction.

---

### Pattern Recognition

Use Two Pointers when:

- You need to compare elements from both ends.
- The input is sorted and you need to find pairs efficiently.
- You want to reduce extra space by avoiding additional arrays or strings.
- The problem involves moving through an array or string using two indices.

---

### Example

Input:

```python
s = "madam"
```

Process:

```text
m a d a m
↑       ↑
L       R
```

Compare both characters and move the pointers inward.

Output:

```text
Palindrome
```

---

### Intuition

Instead of creating a new string or array, compare elements directly using two pointers.

If the elements match, move both pointers inward. If they don't, the answer is found immediately.

---

### Python Example

```python
s = "madam"

left = 0
right = len(s) - 1

while left < right:

    # If characters don't match, it isn't a palindrome
    if s[left] != s[right]:
        print(False)
        break

    # Move both pointers towards the center
    left += 1
    right -= 1
else:
    print(True)
```

---

### Advantages

- Reduces extra space usage.
- Often eliminates the need for additional arrays or strings.
- Leads to cleaner and more efficient solutions.
- Frequently improves brute-force solutions.

---

### Time Complexity

**O(n)**

### Space Complexity

**O(1)**

---

### When to Use

- Checking Palindromes
- Reversing Strings
- Finding pairs in sorted arrays
- Removing duplicates from sorted arrays
- Merging sorted arrays
- Container problems (advanced)

---

### Common Mistakes

- Moving pointers in the wrong direction.
- Using an incorrect loop condition.
- Forgetting to move both pointers.
- Not returning immediately when a mismatch is found.

---

### Practice Questions

1. Check whether a string is a palindrome.
2. Reverse a string using two pointers.
3. Remove duplicates from a sorted array.
4. Merge two sorted arrays.

### Practice Problems

- LeetCode: https://leetcode.com/problems/reverse-string/
- LeetCode: https://leetcode.com/problems/valid-palindrome/
- LeetCode: https://leetcode.com/problems/remove-duplicates-from-sorted-array/
- LeetCode: https://leetcode.com/problems/merge-sorted-array/
- GeeksforGeeks: https://www.geeksforgeeks.org/two-pointers-technique/

---

🚀 Explore together. Learn together. Grow together.