# 🚀 Two Pointer — Same Direction (Sliding Window)

This is the most powerful two pointer pattern for:
- Subarrays
- Substrings
- Continuous segments

---

# 🧠 CORE IDEA

Both pointers move in the **same direction**:
left → → → → →
right → → → → →

👉 They form a **window**

---

# 🎯 WHEN TO USE

Use when:

- Problem involves **subarray / substring**
- Elements must be **continuous**
- You need:
  - longest / shortest
  - count of valid subarrays
  - max/min length

---

# 🔥 RECOGNITION TRIGGERS

If you see:

- “substring”
- “subarray”
- “continuous segment”
- “longest / shortest window”
- “at most k”
- “exactly k”

👉 Your brain should say:Sliding Window




---

# ⚡ CORE PATTERN

```java
int left = 0;

for (int right = 0; right < n; right++) {

    // expand window

    while (condition breaks) {
        // shrink window
        left++;
    }

    // update answer
}
```

---

# 🧠 HOW TO THINK

### Step 1: Expand
👉 Include new element (right++)

---

### Step 2: Check
👉 Is window valid?

---

### Step 3: Shrink
👉 If invalid → move left++

---

### Step 4: Update
👉 Track answer

---

# 🔥 TYPES OF SLIDING WINDOW

---

## 🟢 Type 1: Fixed Window

### 🎯 Use:
- Window size = k

### Example:
- Max sum of size k

---

## 🟡 Type 2: Variable Window

### 🎯 Use:
- Condition-based window

### Example:
- Longest substring without repeating characters

---

# 🧪 IMPORTANT PROBLEMS

---

## 🟢 EASY

### 1. Maximum Average Subarray I
- LeetCode 643
- Fixed window

---

## 🟡 MEDIUM (VERY IMPORTANT)

### 2. Longest Substring Without Repeating Characters ⭐
- LeetCode 3

---

### 3. Minimum Size Subarray Sum ⭐
- LeetCode 209

---

### 4. Max Consecutive Ones III
- LeetCode 1004

---

### 5. Binary Subarrays With Sum
- LeetCode 930

---

## 🔴 HARD

### 6. Minimum Window Substring ⭐
- LeetCode 76

---

# ⚡ CORE LOGIC TYPES

---

## 🔹 Type A: At Most K

👉 Use sliding window directly

---

## 🔹 Type B: Exactly K

👉 Trick:exactly(k) = atMost(k) - atMost(k-1)


---

# ⚠️ COMMON MISTAKES

- Not shrinking window ❌  
- Infinite loop in while ❌  
- Wrong condition handling ❌  
- Confusing with prefix sum ❌  

---

# 🧠 DECISION RULE

| Situation | Use |
|----------|-----|
| Continuous subarray | Sliding window |
| Pair in sorted array | Opposite pointer |
| Range sum queries | Prefix sum |

---

# 🔥 FINAL INSIGHT

> Sliding window =  
> “Dynamically adjust window instead of recomputing”

---

# 🏁 ONE LINE MEMORY

👉 Subarray / Substring → Sliding Window


# 🚀 Sliding Window — LeetCode Question Set

This list is structured from **basic → advanced → interview level**

---

# 🟢 LEVEL 1: Fixed Window (Foundation)

## 🎯 Goal:
Understand how to maintain a window of size k

---

### 1. Maximum Average Subarray I
- **LeetCode 643**

---

### 2. Find All Anagrams in a String
- **LeetCode 438**

---

### 3. Permutation in String
- **LeetCode 567**

---

# 🟡 LEVEL 2: Variable Window (Core Pattern)

## 🎯 Goal:
Expand → break → shrink

---

### 4. Longest Substring Without Repeating Characters ⭐
- **LeetCode 3**

---

### 5. Minimum Size Subarray Sum ⭐
- **LeetCode 209**

---

### 6. Max Consecutive Ones III
- **LeetCode 1004**

---

### 7. Fruit Into Baskets
- **LeetCode 904**

---

# 🔵 LEVEL 3: Count-Based Sliding Window

## 🎯 Goal:
Count number of valid subarrays

---

### 8. Binary Subarrays With Sum ⭐
- **LeetCode 930**

---

### 9. Subarrays with K Different Integers ⭐
- **LeetCode 992**

---

### 10. Count Number of Nice Subarrays
- **LeetCode 1248**

---

# 🔴 LEVEL 4: Advanced / Interview Level

---

### 11. Minimum Window Substring ⭐ (VERY IMPORTANT)
- **LeetCode 76**

---

### 12. Longest Repeating Character Replacement
- **LeetCode 424**

---

### 13. Sliding Window Maximum ⭐
- **LeetCode 239**
- (Uses deque + sliding window)

---

# ⚫ LEVEL 5: Hybrid (Sliding Window + Other Techniques)

---

### 14. Subarray Product Less Than K
- **LeetCode 713**

---

### 15. Shortest Subarray with Sum at Least K
- **LeetCode 862**
- (Sliding + deque)

---

# 🧠 PATTERN SUMMARY

---

## 🟢 Fixed Window
- Size = k
- Slide window

---

## 🟡 Variable Window
- Expand until invalid
- Shrink to fix

---

## 🔵 Count Problems
- Use hashmap / prefix trick

---

## 🔴 Advanced
- Combine with deque / hashmap

---

# ⚠️ COMMON MISTAKES

- Forgetting to shrink window ❌  
- Wrong condition for while loop ❌  
- Not handling duplicates ❌  
- Confusing “at most k” vs “exactly k” ❌  

---

# 🔥 MOST IMPORTANT QUESTIONS

If short on time, do these:

1. 3 ⭐  
2. 209 ⭐  
3. 1004  
4. 930 ⭐  
5. 76 ⭐  

---

# 🚀 PRACTICE PLAN

## Day 1:
- 643
- 3

---

## Day 2:
- 209
- 1004

---

## Day 3:
- 930
- 992

---

## Day 4:
- 76 (deep focus)

---

# ⚡ FINAL INSIGHT

> Sliding Window =  
> “Don’t recompute subarrays — adjust boundaries dynamically”















