
# 🧵 Python Strings Cheatsheet for Leetcode

## 📌 Basics

```python
s = "leetcode"
len(s)        # Length of string
s[0]          # First character -> 'l'
s[-1]         # Last character -> 'e'
s[1:4]        # Substring -> 'eet'
s[::-1]       # Reverse -> 'edocteel'
```

---

## 🛠️ Common String Methods

### 🔤 Case
```python
s.lower(), s.upper(), s.title(), s.capitalize()
```

### ✂️ Trim Whitespace
```python
s.strip(), s.lstrip(), s.rstrip()
```

### 🔍 Search
```python
s.find("abc")      # Returns index or -1
s.index("abc")     # Returns index or throws error
"abc" in s         # Boolean check
```

### 🔄 Replace & Split
```python
s.replace("a", "b")
s.split(" ")         # Split on space
" ".join(list)       # Join with space
```

---

## 🧪 Checks

### ✅ Palindrome
```python
s == s[::-1]
```

### ✅ Starts / Ends
```python
s.startswith("abc")
s.endswith("xyz")
```

### ✅ Is X?
```python
s.isalpha(), s.isdigit(), s.isalnum(), s.isspace()
```

---

## 🔄 Loops & Conversions

```python
for c in s: print(c)        # Character loop
list(s)                     # ['l', 'e', ...]
"".join(list)               # Convert list to string
```

---

## 🔢 Frequency Count

### ✅ Manual
```python
freq = {}
for c in s:
    freq[c] = freq.get(c, 0) + 1
```

### ✅ Pythonic
```python
from collections import Counter
Counter(s)
```

---

## 🎯 String Tricks for Leetcode

### 🔁 Reverse Words
```python
" ".join(s.split()[::-1])
```

### 🔢 First Unique Character
```python
from collections import Counter
count = Counter(s)
for i, c in enumerate(s):
    if count[c] == 1:
        return i
```

### 🔀 Anagram Check
```python
sorted(s1) == sorted(s2)
Counter(s1) == Counter(s2)
```

### 🧹 Remove Non-Alphanumeric
```python
import re
re.sub(r'[^a-zA-Z0-9]', '', s)
```

---

## 🧩 Tips

- Strings are **immutable** — operations return new strings.
- Use `s[::-1]` for reversing strings/palindromes.
- Use `Counter` or sorting for anagram problems.
- `''.join()` is **faster** than `+=` in loops.

---

## ✅ Practice (Leetcode Easy)
- 344. Reverse String
- 125. Valid Palindrome
- 387. First Unique Character in a String
- 242. Valid Anagram
- 14. Longest Common Prefix
- 28. Find the Index of the First Occurrence
