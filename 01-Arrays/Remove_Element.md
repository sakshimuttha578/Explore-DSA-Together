# Remove Element

## What is Remove Element?

Given an array `nums` and a value `val`, remove all occurrences of `val` **in-place** and return the number of remaining elements.

The relative order of the remaining elements does not matter.

### Examples

Input:

```python
nums = [3,2,2,3]
val = 3
```

Output:

```text
2

nums = [2,2,_,_]
```

Input:

```python
nums = [0,1,2,2,3,0,4,2]
val = 2
```

Output:

```text
5

nums = [0,1,3,0,4,_,_,_]
```

---

### Intuition

We use the **Two Pointers** technique.

- 👀 **Reader** checks every element.
- ✍️ **Writer** writes only the elements that are **not equal to `val`**.

This allows us to modify the array **in-place** without using extra space.

---

## Python Solution

```python
class Solution(object):
    def removeElement(self, nums, val):
        i = 0      # Writer
        j = 0      # Reader

        while j < len(nums):
            if nums[j] != val:
                nums[i] = nums[j]
                i += 1

            j += 1

        return i
```

---

### Time Complexity

**O(n)**

### Space Complexity

**O(1)**

---

### Common Mistakes

- Using `j <= len(nums)` instead of `j < len(nums)`.
- Incrementing the reader twice.
- Returning `i + 1` instead of `i`.
- Forgetting that the writer only moves after writing a valid element.

---

### Practice Questions

1. Remove all occurrences of a given value from an array.
2. Remove all negative numbers from an array.
3. Move all even numbers to the beginning of an array.
4. Remove all occurrences of a character from a string.

### Practice Problems

- LeetCode: https://leetcode.com/problems/remove-element/
- LeetCode: https://leetcode.com/problems/remove-duplicates-from-sorted-array/
- LeetCode: https://leetcode.com/problems/move-zeroes/
- GeeksforGeeks: https://www.geeksforgeeks.org/remove-array-elements-equal-to-a-given-value/

---

### 💡 What I Learned

- Reader checks every element.
- Writer writes only valid elements.
- Reader always moves.
- Writer moves only after writing.
- `i` represents the **next position to write**.
- Always use `j < len(nums)` to avoid index out of range errors.

---

🚀 Explore together. Learn together. Grow together.