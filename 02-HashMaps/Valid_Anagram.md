# Valid Anagram

## What is Valid Anagram?

Two strings are anagrams if they contain the same characters with the same frequencies, regardless of their order.

### Examples

Input:

```python
s = "anagram"
t = "nagaram"
```

Output:

```text
True
```

Input:

```python
s = "rat"
t = "car"
```

Output:

```text
False
```

---

### Intuition

Store the frequency of characters from both strings using Hash Maps (Dictionaries).

If both frequency maps are equal, the strings are anagrams.

---

## Python Solution

```python
s = "anagram"
t = "nagaram"

# If lengths are different, they cannot be anagrams
if len(s) != len(t):
    print(False)

else:
    f1 = {}

    # Store frequencies of characters in first string
    for ch in s:
        if ch in f1:
            f1[ch] += 1
        else:
            f1[ch] = 1

    f2 = {}

    # Store frequencies of characters in second string
    for ch in t:
        if ch in f2:
            f2[ch] += 1
        else:
            f2[ch] = 1

    # Compare both frequency maps
    print(f1 == f2)
```

---

### Time Complexity

**O(n)**

### Space Complexity

**O(n)**

---

### Common Mistakes

- Forgetting to check if the string lengths are equal.
- Comparing strings directly instead of their frequencies.
- Updating frequencies incorrectly.
- Confusing keys and values in the dictionary.

---

### Practice Questions

1. Check whether two strings are anagrams.
2. Group anagrams from a list of strings.
3. Find all anagrams of a pattern in a string.
4. Check whether two arrays contain the same frequencies.

### Practice Problems

- LeetCode: https://leetcode.com/problems/valid-anagram/
- LeetCode: https://leetcode.com/problems/group-anagrams/
- HackerRank: https://www.hackerrank.com/challenges/making-anagrams/problem
- GeeksforGeeks: https://www.geeksforgeeks.org/check-whether-two-strings-are-anagram-of-each-other/

---

🚀 Explore together. Learn together. Grow together.