## Valid Anagram 🚀

## 🧠 Problem Statement

Given two strings `s` and `t`, return `True` if `t` is an anagram of `s`, and `False` otherwise.

---

## Example 1:

**Input:** s = "anagram", t = "nagaram"

**Output:** true


## Example 2:

**Input:** s = "rat", t = "car"

**Output:** false

---

## ✅ Approach

`Counter(string)` used to compare the strings.
If they are equal, return `True`.


---

## 🧮 Complexity

**Time Complexity** :	O(n + m)

**Space Complexity** : 	O(1)(best) O(n + m)(worst)

---

## 🔍 Code (Python)
```python
class Solution:
    def isAnagram(self, s: str, t: str) -> bool:
        return Counter(s) == Counter(t)
