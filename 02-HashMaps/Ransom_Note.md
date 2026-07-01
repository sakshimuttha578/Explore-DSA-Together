# Ransom Note

## What is the Problem?

Given two strings `ransomNote` and `magazine`, return `True` if you can construct the ransom note using the letters from the magazine.

Each letter in the magazine can only be used **once**.

### Examples

Input:

```python
ransomNote = "aa"
magazine = "aab"
```

Output:

```python
True
```

Input:

```python
ransomNote = "aa"
magazine = "ab"
```

Output:

```python
False
```

---

### Intuition

Count the frequency of each character in both strings.

For every character required in the ransom note:

- It must be present in the magazine.
- The magazine must contain at least the same number of occurrences.

If any character is missing or its frequency is less than required, return `False`.

Otherwise, return `True`.

---

## Python Solution

```python
class Solution(object):
    def canConstruct(self, ransomNote, magazine):
        f1 = {}

        # Count the frequency of characters required
        for ch in ransomNote:
            if ch in f1:
                f1[ch] += 1
            else:
                f1[ch] = 1

        f2 = {}

        # Count the frequency of available characters
        for ch in magazine:
            if ch in f2:
                f2[ch] += 1
            else:
                f2[ch] = 1

        # Verify every required character is available
        for ch in f1:
            if ch not in f2 or f2[ch] < f1[ch]:
                return False

        return True
```

---

### Time Complexity

**O(n + m)**

- `n` = length of `ransomNote`
- `m` = length of `magazine`


### Space Complexity

**O(k)**

Where `k` is the number of unique characters stored in the hash maps.

---

### Common Mistakes

- Building the frequency map for the wrong string.
- Forgetting to check if a character exists in the magazine.
- Comparing frequencies incorrectly.
- Using each magazine character more than once.

---

### Practice Questions

1. Count the frequency of characters in a string.
2. Check whether one string can be formed using another.
3. Find the first non-repeating character.
4. Find the intersection of two strings.

### Practice Problems

- https://leetcode.com/problems/ransom-note/
- https://leetcode.com/problems/find-the-difference/
- https://leetcode.com/problems/first-unique-character-in-a-string/
- https://www.geeksforgeeks.org/count-frequency-of-characters-in-a-string/

---

🚀 Explore together. Learn together. Grow together.