# Reverse String

## What is Reverse String?

Reverse String is a problem where you reverse the given array of characters **in-place**, meaning you modify the original array without creating another one.

### Examples

Input:

```python
["h","e","l","l","o"]
```

Output:

```python
["o","l","l","e","h"]
```

Input:

```python
["H","a","n","n","a","h"]
```

Output:

```python
["h","a","n","n","a","H"]
```

---

### Intuition

Use two pointers:

- One pointer starts from the beginning.
- The other pointer starts from the end.

Swap both characters and move the pointers towards the center until they meet.

This allows us to reverse the array using **constant extra space**.

---

## Python Solution

```python
class Solution(object):
    def reverseString(self, s):
        left = 0
        right = len(s) - 1

        while left < right:

            # Swap the characters at both pointers
            temp = s[left]
            s[left] = s[right]
            s[right] = temp

            # Move both pointers towards the center
            left += 1
            right -= 1
```

---

### Time Complexity

**O(n)**

### Space Complexity

**O(1)**

---

### Common Mistakes

- Creating another array instead of modifying the given one.
- Forgetting to move both pointers after swapping.
- Using the wrong loop condition.
- Returning or printing the array instead of modifying it in-place.

---

### Practice Questions

1. Reverse an array.
2. Reverse a string.
3. Reverse only vowels in a string.
4. Reverse words in a sentence.

### Practice Problems

- https://leetcode.com/problems/reverse-string/
- https://leetcode.com/problems/reverse-vowels-of-a-string/
- https://leetcode.com/problems/reverse-words-in-a-string/
- https://www.geeksforgeeks.org/dsa/reverse-an-array/

---

🚀 Explore together. Learn together. Grow together.