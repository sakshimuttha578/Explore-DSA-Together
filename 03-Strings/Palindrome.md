# Palindrome

## What is a Palindrome?

A palindrome is a word, phrase, number, or sequence that reads the same forwards and backwards.

### Examples

- madam
- racecar
- level
- 121

---

### Intuition

If the reversed string is equal to the original string, it is a palindrome.

---

## Python Solution

```python
s = "madam"

rev = ""

for ch in s:
    rev = ch + rev   
    # rev = rev + ch is wrong, it will the return the string as it is

if s == rev:
    print("Palindrome")
else:
    print("Not a Palindrome")
```

---

### Time Complexity

**O(n)**

### Space Complexity

**O(n)**

---

### Common Mistakes

- Using the character as an index (`s[ch]`)
- Reversing incorrectly (`rev = rev + ch`)
- Ignoring case sensitivity

---

### Practice Questions

1. Check whether a string is a palindrome.
2. Check whether a number is a palindrome.
3. Check palindrome without creating a reversed string.

### Practice Problems

- LeetCode: https://leetcode.com/problems/valid-palindrome/
- LeetCode: https://leetcode.com/problems/palindrome-number/
- GeeksforGeeks: https://www.geeksforgeeks.org/check-if-a-string-is-palindrome-or-not/

---

🚀 Explore together. Learn together. Grow together.