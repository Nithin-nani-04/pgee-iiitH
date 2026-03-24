# 🚀 Fast & Slow Pointer — LeetCode Problems

This pattern is used to detect:
- Cycles
- Middle points
- Repeating structures

---

# 🧠 WHEN TO USE

Use Fast & Slow Pointer when:

- Linked list problems
- Cycle detection
- “Find middle” type questions
- Repeating sequence / loop detection

---

# 🟢 LEVEL 1: FOUNDATION

## 1. Linked List Cycle ⭐
- **LeetCode 141**

### 🎯 Goal:
Detect if a cycle exists

### 💡 Idea:
- slow = 1 step
- fast = 2 steps
- if they meet → cycle

---

## 2. Middle of the Linked List ⭐
- **LeetCode 876**

### 🎯 Goal:
Find middle node

### 💡 Idea:
- fast moves twice
- slow ends at middle

---

# 🟡 LEVEL 2: CORE APPLICATION

## 3. Linked List Cycle II ⭐ (VERY IMPORTANT)
- **LeetCode 142**

### 🎯 Goal:
Find start of cycle

### 💡 Idea:
- detect meeting point
- reset one pointer
- move both → meet at start

---

## 4. Happy Number ⭐
- **LeetCode 202**

### 🎯 Goal:
Detect cycle in numbers

### 💡 Idea:
- treat transformation as linked list

---

# 🔵 LEVEL 3: ADVANCED

## 5. Find the Duplicate Number ⭐
- **LeetCode 287**

### 🎯 Goal:
Find duplicate without modifying array

### 💡 Idea:
- treat array as linked list
- use cycle detection

---

## 6. Remove Nth Node From End of List
- **LeetCode 19**

### 🎯 Goal:
Remove nth node from end

### 💡 Idea:
- maintain gap between fast & slow

---

# 🔴 LEVEL 4: HARD THINKING

## 7. Palindrome Linked List
- **LeetCode 234**

### 🎯 Goal:
Check if linked list is palindrome

### 💡 Idea:
- find middle using fast/slow
- reverse second half

---

## 8. Reorder List
- **LeetCode 143**

### 🎯 Goal:
Reorder nodes

### 💡 Idea:
- find middle
- reverse + merge

---

# 🧠 PATTERN SUMMARY

| Problem Type | Use |
|-------------|-----|
| Detect cycle | Fast & slow |
| Find middle | Fast & slow |
| Find cycle start | Reset trick |
| Duplicate number | Treat as cycle |
| Remove nth node | Gap technique |

---

# ⚠️ COMMON MISTAKES

- Not checking fast.next ❌  
- Infinite loop ❌  
- Forgetting reset step ❌  
- Not understanding why it works ❌  

---

# 🚀 PRACTICE ORDER

1. 141 ⭐  
2. 876  
3. 142 ⭐  
4. 202  
5. 287 ⭐  
6. 19  
7. 234  

---

# 🔥 MOST IMPORTANT QUESTIONS

If short on time:

- 141  
- 142  
- 287  

---

# ⚡ FINAL INSIGHT

> Fast & Slow Pointer =  
> “Use speed difference to detect hidden cycles”
