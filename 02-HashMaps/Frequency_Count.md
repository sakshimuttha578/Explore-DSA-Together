# Frequency Counting

## What is Frequency Counting?

Frequency counting is the process of counting how many times each element appears in a string, array, or collection.

### Examples

#### String

Input:

```python
s = "success"
```

Output:

```text
s → 3
u → 1
c → 2
e → 1
```

#### Array

Input:

```python
arr = [1, 2, 2, 3, 1]
```

Output:

```text
1 → 2
2 → 2
3 → 1
```

---

### Intuition

Use a Hash Map (Dictionary) to store the frequency of each element.

- If the element already exists, increase its count.
- Otherwise, add it with a count of 1.

---

## Python Solution

```python
s = "success"

freq = {}

for ch in s:
    # If character already exists, increase its count
    if ch in freq:
        freq[ch] += 1
    else:
        # First occurrence of the character
        freq[ch] = 1

print(freq)
```

---

### Time Complexity

**O(n)**

### Space Complexity

**O(n)**

---

### Common Mistakes

- Forgetting to initialize the dictionary.
- Updating frequency before checking if the key exists.
- Confusing keys and values.

---

### Practice Questions

1. Count character frequencies in a string.
2. Count frequencies in an array.
3. Find the most frequent character.
4. Find the first non-repeating character.

### Practice Problems

- LeetCode: https://leetcode.com/problems/valid-anagram/
- LeetCode: https://leetcode.com/problems/top-k-frequent-elements/
- GeeksforGeeks: https://www.geeksforgeeks.org/frequency-of-each-character-in-a-string-using-unordered_map-in-c/

---

🚀 Explore together. Learn together. Grow together.