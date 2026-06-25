# Contains Duplicate

## What is Contains Duplicate?

Contains Duplicate means checking whether any element appears more than once in a collection.

If at least one element is repeated, return True. Otherwise, return False.

### Examples

Input:

```python
a = [1, 2, 3, 1]
```

Output:

```text
True
```

Input:

```python
b = [1, 2, 3, 4]
```

Output:

```text
False
```

---

### Intuition

Store the frequency of each element using a Hash Map (Dictionary).

If the frequency of any element becomes greater than 1, a duplicate exists.

---

## Python Solution

```python
nums = [1, 2, 3, 1]

freq = {}

for num in nums:
    # If number already exists, increase its frequency
    if num in freq:
        freq[num] += 1
    else:
        # First occurrence of the number
        freq[num] = 1

for num in freq:
    if freq[num] > 1:
        print(True)
        break
else:
    print(False)
```

---

### Time Complexity

**O(n)**

### Space Complexity

**O(n)**

---

### Common Mistakes

- Returning False before checking all elements.
- Forgetting to update the frequency count.
- Using print instead of return in coding platforms like LeetCode.
- Confusing keys and values in the dictionary.

---

### Practice Questions

1. Check whether an array contains duplicates.
2. Find all duplicate elements in an array.
3. Count the frequency of each element.
4. Find the first repeating element.

### Practice Problems

- LeetCode: https://leetcode.com/problems/contains-duplicate/
- LeetCode: https://leetcode.com/problems/contains-duplicate-ii/
- LeetCode: https://leetcode.com/problems/intersection-of-two-arrays/
- HackerRank: https://www.hackerrank.com/domains/data-structures
- GeeksforGeeks: https://www.geeksforgeeks.org/find-duplicates-in-on-time-and-constant-extra-space/

---

🚀 Explore together. Learn together. Grow together.