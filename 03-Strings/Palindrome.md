# Palindrome

## What is a Palindrome?

A palindrome is a word, phrase, or sequence that reads the same forwards and backwards.

Examples:
- madam
- racecar
- level

## Intuition

If the reversed string is equal to the original string, it is a palindrome.

## Python Solution

```python
s = "madam"

rev = ""

for ch in s:
    rev = ch + rev

if s == rev:
    print("Palindrome")
else:
    print("Not a Palindrome")
```

## Practice Resources

### LeetCode

- [Valid Palindrome (Easy)](https://leetcode.com/problems/valid-palindrome/)
- [Palindrome Number (Easy)](https://leetcode.com/problems/palindrome-number/)
- [Valid Palindrome II (Medium)](https://leetcode.com/problems/valid-palindrome-ii/)

### GeeksforGeeks

- [Palindrome String](https://www.geeksforgeeks.org/check-if-a-string-is-palindrome-or-not/)
- [Palindrome Number](https://www.geeksforgeeks.org/check-if-a-number-is-palindrome/)

### HackerRank

- Search: "Palindrome" in the Strings Practice section
- Search: "Palindrome Index"

### Additional Practice

- Create your own palindrome checker.
- Check palindromes ignoring spaces.
- Check palindromes ignoring special characters.

## Time Complexity

O(n)

## Space Complexity

O(n)

---

🚀 Explore together. Learn together. Grow together.