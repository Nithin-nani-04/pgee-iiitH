# 🚀 Prefix Sum & Related Patterns — LeetCode Mastery Roadmap

This roadmap is designed to help you **master Prefix Sum step-by-step**, not just solve problems randomly.

---

# 🟢 LEVEL 1: Pure Prefix Sum (Foundation)

## 🎯 Goal:
Understand range sum and cumulative thinking.

### Problems:
- **1480. Running Sum of 1D Array**
- **303. Range Sum Query - Immutable**
- **724. Find Pivot Index**

## 🧠 Key Learning:
- Build prefix array
- Use prefix to answer queries in O(1)
- Understand left sum vs right sum

---

# 🟡 LEVEL 2: Prefix + Subarray Logic

## 🎯 Goal:
Move from range queries → subarray thinking

### Problems:
- **560. Subarray Sum Equals K ⭐**
- **523. Continuous Subarray Sum**
- **325. Maximum Size Subarray Sum Equals K**

## 🧠 Key Learning:
- Prefix + HashMap
- Store previous sums
- Detect patterns instead of brute force

---

# 🔵 LEVEL 3: Prefix + Counting Patterns

## 🎯 Goal:
Recognize repeating patterns in disguise

### Problems:
- **974. Subarrays Divisible by K**
- **930. Binary Subarrays With Sum**
- **1248. Count Number of Nice Subarrays**

## 🧠 Key Learning:
- Use modulo with prefix
- Convert problem into known pattern
- Count using frequency map

---

# 🔴 LEVEL 4: Prefix + Advanced Adaptation

## 🎯 Goal:
Handle variations and transformations

### Problems:
- **525. Contiguous Array**
- **209. Minimum Size Subarray Sum**
- **304. Range Sum Query 2D**

## 🧠 Key Learning:
- Transform values (0 → -1)
- Combine prefix with other techniques
- Work with 2D prefix arrays

---

# ⚫ LEVEL 5: Hard (Interview Level Edge)

## 🎯 Goal:
Handle complex prefix-based logic

### Problems:
- **327. Count of Range Sum**
- **862. Shortest Subarray with Sum at Least K**

## 🧠 Key Learning:
- Prefix + Merge Sort
- Prefix + Monotonic Queue
- Optimization beyond HashMap

---

# 🧠 CORE PATTERNS SUMMARY

## 🧩 Pattern 1: Range Query
- Use prefix array
- Formula: prefix[R] - prefix[L-1]

---

## 🧩 Pattern 2: Subarray Sum = K
- Use prefix + HashMap
- Check: currentSum - K

---

## 🧩 Pattern 3: Divisible by K
- Use prefix % K
- Store remainder frequency

---

## 🧩 Pattern 4: Equal Counts
- Transform values (e.g., 0 → -1)
- Apply prefix sum

---

# 📅 PRACTICE PLAN (5 DAYS)

## Day 1:
- 1480
- 303
- 724

---

## Day 2:
- 560 ⭐
- 930

---

## Day 3:
- 974
- 1248
- 525

---

## Day 4:
- 523
- 325

---

## Day 5:
- 304
- 209

---

# ⚠️ COMMON MISTAKES

- Forgetting prefix initialization
- Missing edge case (sum = 0)
- Not storing frequency properly
- Confusing prefix with sliding window

---

# 🔥 FINAL INSIGHT

> Don’t recompute subarrays.  
> Use previous work to answer instantly.

---

# 🚀 NEXT STEP

Start with:

👉 **560. Subarray Sum Equals K**

Master this → unlock most prefix sum problems.
