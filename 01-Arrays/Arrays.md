# Arrays
---

# What are Arrays?

An array is a collection of elements stored in contiguous memory locations. Each element is accessed using its index, making retrieval fast and efficient.

Arrays are one of the most fundamental data structures and serve as the building block for many DSA concepts.

---

### 💡 Pattern Recognition

Think of Arrays when:

- ✅ You need to store multiple values.
- ✅ Fast index-based access is required.
- ✅ The order of elements matters.
- ✅ You need to traverse or process a sequence.

---

### 👀 Visual Intuition

Think of an array as a row of numbered boxes.

```text
Index:    0      1      2      3      4
        +-----+-----+-----+-----+-----+
Array:  | 10  | 20  | 30  | 40  | 50  |
        +-----+-----+-----+-----+-----+
```

Want the third element?

```python
arr[2]
```

Output:

```text
30
```

---

### 📝 Example

Input:

```python
arr = [10, 20, 30, 40, 50]
```

Accessing elements:

```python
print(arr[0])   # 10
print(arr[2])   # 30
print(arr[4])   # 50
```

---

### 🧠 Intuition

Instead of searching from the beginning every time, arrays let us directly jump to an element using its index.

Think of it like apartment numbers.

If you want Flat **203**, you don't open every door—you go directly to Flat **203**.

Arrays work the same way.

---

### 🐍 Python Example

```python
arr = [10, 20, 30, 40, 50]

# Traverse every element
for num in arr:
    print(num)

# Access an element using its index
print(arr[2])
```

---

### ⚡ Time Complexity

| Operation | Complexity |
|-----------|------------|
| Access | O(1) |
| Traversal | O(n) |
| Search | O(n) |
| Insert at End | O(1)* |
| Insert/Delete in Middle | O(n) |

> *Amortized for Python lists.*

---

### 💾 Space Complexity

**O(n)**

---

### ✅ Advantages

- Very fast index access.
- Easy to traverse.
- Beginner-friendly.
- Foundation of many DSA problems.

---

### 📌 When to Use

- Storing collections of data.
- Traversing elements.
- Processing sequences.
- Solving most beginner DSA problems.

---

### ❌ Common Mistakes

- Forgetting indexing starts from **0**.
- Confusing indexes with values.
- Accessing invalid indexes.
- Modifying an array while iterating without care.

---

### 🎯 Practice Questions

1. Traverse an array.
2. Find the maximum element.
3. Find the minimum element.
4. Calculate the sum of all elements.
5. Count even and odd numbers.

### 💻 Practice Problems

- LeetCode (Easy): https://leetcode.com/problems/find-numbers-with-even-number-of-digits/
- LeetCode (Easy): https://leetcode.com/problems/richest-customer-wealth/
- HackerRank: https://www.hackerrank.com/domains/data-structures/arrays
- GeeksforGeeks: https://www.geeksforgeeks.org/array-data-structure-guide/

---

### 🚀 Key Takeaways

✔ Arrays store elements in order.

✔ Accessing an element by index is **O(1)**.

✔ Traversing an array takes **O(n)**.

✔ Arrays are the foundation of many DSA patterns.

---

 🚀 Explore together. Learn together. Grow together.