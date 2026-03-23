# 🚀 Two Pointer Technique — Complete Master Map

This file is your **complete guide to Two Pointers**:
- Types
- Patterns
- When to use
- Why it matters
- Problem roadmap

---

# 🧠 WHAT IS TWO POINTER?

Two Pointer is a technique where:
> We use two indices to traverse and reduce time complexity (usually from O(n²) → O(n))

---

# 🔥 WHY TWO POINTER IS IMPORTANT

## 🚨 Without Two Pointers:
- You try all pairs → O(n²)
- You try all subarrays → O(n²)

## ⚡ With Two Pointers:
- You eliminate unnecessary work
- You use structure (sorted / continuous)

---

## 🎯 Real Impact:
| Problem | Brute Force | Two Pointer |
|--------|------------|------------|
| Pair Sum | O(n²) | O(n) |
| Subarray | O(n²) | O(n) |
| Sliding Window | O(n²) | O(n) |

---

## 🔥 Core Idea:
> “Don’t check everything — eliminate possibilities smartly”

---

# 🟢 TYPE 1: Opposite Direction (Two Ends)

## 🎯 Use When:
- Array is sorted
- Pair problems
- Sum problems

---

## 🔧 Pattern:
left = 0
right = n - 1

while left < right:
if condition:
left++
else:
right--


---

## 🧠 Thinking:
> “Use sorted order to shrink search space”

---

## 🧪 Problems:
- 167. Two Sum II
- 15. 3Sum
- 11. Container With Most Water

---

# 🟡 TYPE 2: Sliding Window (Same Direction)

## 🎯 Use When:
- Subarray / substring
- Continuous segment
- Window size variable

---

## 🔧 Pattern:
left = 0

for right in range(n):
expand window

while condition breaks:
    shrink window
    left++


---

## 🧠 Thinking:
> “Grow → break → shrink → fix”

---

## 🧪 Problems:
- 3. Longest Substring Without Repeating Characters
- 209. Minimum Size Subarray Sum
- 1004. Max Consecutive Ones III

---

# 🔵 TYPE 3: Fast & Slow Pointer

## 🎯 Use When:
- Linked list problems
- Cycle detection
- Middle node

---

## 🔧 Pattern:
slow = head
fast = head

while fast != null and fast.next != null:
slow = slow.next
fast = fast.next.next


---

## 🧠 Thinking:
> “Different speeds reveal hidden structure”

---

## 🧪 Problems:
- 141. Linked List Cycle
- 876. Middle of Linked List
- 142. Cycle Detection II

---

# 🔴 TYPE 4: Fixed Window (Same Direction Gap)

## 🎯 Use When:
- Fixed size window
- Compare distance k

---

## 🔧 Pattern:
window_sum = 0

for i in range(n):
window_sum += arr[i]

if i >= k:
    window_sum -= arr[i-k]


---

## 🧠 Thinking:
> “Maintain exact window size”

---

## 🧪 Problems:
- 643. Maximum Average Subarray I
- Fixed window problems

---

# 🟣 TYPE 5: Partitioning (Rearrangement)

## 🎯 Use When:
- Rearranging elements
- Sorting-like problems

---

## 🔧 Pattern:
i = 0

for j in range(n):
if condition:
swap(arr[i], arr[j])
i++


---

## 🧠 Thinking:
> “Push correct elements to correct side”

---

## 🧪 Problems:
- 75. Sort Colors
- Move Zeros

---

# ⚫ TYPE 6: Advanced Sliding Window (Multiple Constraints)

## 🎯 Use When:
- Complex substring problems
- Multiple conditions

---

## 🧪 Problems:
- 76. Minimum Window Substring
- 30. Substring with Concatenation

---

## 🧠 Thinking:
> “Track multiple states while adjusting window”

---

# 🧠 DECISION TREE (VERY IMPORTANT)

## Ask yourself:

### 1️⃣ Is array sorted?
👉 YES → Opposite pointers

---

### 2️⃣ Is it subarray / substring?
👉 YES → Sliding window

---

### 3️⃣ Is it linked list?
👉 YES → Fast & slow

---

### 4️⃣ Fixed window size?
👉 YES → Fixed window

---

### 5️⃣ Rearranging elements?
👉 YES → Partitioning

---

# ⚠️ COMMON MISTAKES

- Using sliding window on non-contiguous problems ❌  
- Forgetting to shrink window ❌  
- Not sorting when needed ❌  
- Confusing prefix sum with sliding window ❌  

---

# 🔥 COMPARISON WITH OTHER TECHNIQUES

| Technique | Use Case |
|----------|--------|
| Prefix Sum | Repeated range queries |
| Kadane | Max/min subarray |
| Two Pointer | Reduce search space |
| Sliding Window | Dynamic window problems |

---

# 🚀 PRACTICE ROADMAP

## Day 1:
- 167
- 11

---

## Day 2:
- 3
- 209

---

## Day 3:
- 15 (3Sum)
- 75

---

## Day 4:
- 1004
- 643

---

## Day 5:
- 76 (Hard)

---

# ⚡ FINAL INSIGHT

> Two Pointer is not about moving indices  
> It’s about **eliminating unnecessary work using structure**

---

# 🏁 END NOTE

If you master Two Pointers:
- You solve many O(n²) problems in O(n)
- You build strong pattern recognition
- You improve interview speed significantly

---

# 🔥 NEXT STEP

Combine this with:
- Prefix Sum
- Kadane
- Sliding Window

👉 That’s 70% of array interview problems



# 🚀 Two Pointer Techniques — Types

Two Pointer is a technique used to **reduce time complexity** by using two indices instead of nested loops.

---

# 🟢 1. Opposite Direction (Two Ends)

## 📌 Structure:
- One pointer at start
- One pointer at end

## 🎯 Use When:
- Array is **sorted**
- Pair / sum problems

## 🧠 Idea:
> Use order to eliminate possibilities

---

# 🟡 2. Sliding Window (Same Direction)

## 📌 Structure:
- Both pointers move forward

## 🎯 Use When:
- Subarray / substring problems
- Continuous segments
- Variable window size

## 🧠 Idea:
> Expand → violate → shrink

---

# 🔵 3. Fast & Slow Pointer

## 📌 Structure:
- One pointer moves 1 step
- One pointer moves 2 steps

## 🎯 Use When:
- Linked list problems
- Cycle detection
- Middle node

## 🧠 Idea:
> Speed difference reveals hidden structure

---

# 🔴 4. Fixed Window (Same Direction Gap)

## 📌 Structure:
- Maintain window of size k

## 🎯 Use When:
- Fixed-size subarray problems

## 🧠 Idea:
> Slide window, don’t rebuild

---

# 🟣 5. Partitioning (Rearrangement)

## 📌 Structure:
- One pointer tracks position
- One pointer scans

## 🎯 Use When:
- Rearranging elements
- Sorting-like problems

## 🧠 Idea:
> Move elements to correct side

---

# ⚫ 6. Multi-Pointer / Advanced Window

## 📌 Structure:
- Multiple pointers or hashmap

## 🎯 Use When:
- Complex substring problems
- Multiple constraints

## 🧠 Idea:
> Track multiple conditions simultaneously

---

# 🧠 QUICK DECISION GUIDE

| Problem Type | Technique |
|-------------|----------|
| Sorted + pair | Opposite pointers |
| Subarray / substring | Sliding window |
| Linked list | Fast & slow |
| Fixed size window | Fixed window |
| Rearranging array | Partitioning |

---

# ⚡ FINAL INSIGHT

> Two Pointer = Reduce unnecessary work using smart movement


























