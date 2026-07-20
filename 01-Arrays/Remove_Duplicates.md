# Remove Duplicates from Sorted Array

## What is Remove Duplicates from Sorted Array?

Given a **sorted array**, remove the duplicates **in-place** such that each unique element appears only once.

Return the number of unique elements.

### Examples

Input:

```python
nums = [1,1,2]
```

Output:

```text
2

nums = [1,2,_]
```

Input:

```python
nums = [0,0,1,1,1,2,2,3,3,4]
```

Output:

```text
5

nums = [0,1,2,3,4,_,_,_,_,_]
```

---

### Intuition

Since the array is **sorted**, all duplicates are adjacent.

We use the **Two Pointers** technique.

- 👀 **Reader** checks every element.
- ✍️ **Writer** keeps track of the last unique element and writes the next unique element whenever found.

---

## Python Solution

```python
class Solution(object):
    def removeDuplicates(self, nums):
        if len(nums) == 0:
            return 0

        i = 0      # Writer
        j = 1      # Reader

        while j < len(nums):
            if nums[i] != nums[j]:
                i += 1
                nums[i] = nums[j]

            j += 1

        return i + 1
```

---

### Time Complexity

**O(n)**

### Space Complexity

**O(1)**

---

### Common Mistakes

- Using `<= len(nums)` instead of `< len(nums)`.
- Moving the writer before understanding its role.
- Returning `i` instead of `i + 1`.
- Forgetting that this works only because the array is sorted.

---

### Practice Questions

1. Remove duplicates from a sorted array.
2. Remove duplicates from a sorted linked list.
3. Remove duplicates allowing at most two occurrences.
4. Count unique elements in a sorted array.

### Practice Problems

- LeetCode: https://leetcode.com/problems/remove-duplicates-from-sorted-array/
- LeetCode: https://leetcode.com/problems/remove-duplicates-from-sorted-array-ii/
- LeetCode: https://leetcode.com/problems/remove-element/
- GeeksforGeeks: https://www.geeksforgeeks.org/remove-duplicates-sorted-array/

---

### 💡 What I Learned

- Sorted arrays have adjacent duplicates.
- Reader checks every element.
- Writer points to the last unique element.
- When a new unique element is found:
  - Move the writer.
  - Copy the reader's value.
- Return `i + 1` because `i` represents the last unique index.

---

🚀 Explore together. Learn together. Grow together.