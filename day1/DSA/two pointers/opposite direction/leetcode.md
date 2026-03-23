# 🚀 LeetCode — Opposite Direction Two Pointers

This file focuses on **problems where Opposite Direction Two Pointers is the best approach**.

---

# 🧠 WHEN TO USE THIS TECHNIQUE

Use when:

- Array is **sorted**
- You need to find **pairs / triplets**
- Brute force is O(n²) and can be optimized
- Movement can **increase or decrease value predictably**

---

# 🔥 CORE TEMPLATE

```java
int left = 0;
int right = nums.length - 1;

while (left < right) {
    int sum = nums[left] + nums[right];

    if (sum == target) {
        return new int[]{left, right};
    } else if (sum < target) {
        left++;
    } else {
        right--;
    }
}
```

---

# 🟢 EASY LEVEL

## 1. Two Sum II — Input Array is Sorted ⭐
- **LeetCode 167**

### 💡 Idea:
- Direct opposite pointer usage

---

## 2. Valid Palindrome
- **LeetCode 125**

### 💡 Idea:
- Compare left & right characters

---

# 🟡 MEDIUM LEVEL

## 3. Container With Most Water ⭐
- **LeetCode 11**

### 💡 Idea:
- Move smaller height pointer

---

## 4. 3Sum ⭐ (VERY IMPORTANT)
- **LeetCode 15**

### 💡 Idea:
- Fix one index
- Apply two pointers on remaining

---

## 5. 3Sum Closest
- **LeetCode 16**

### 💡 Idea:
- Same as 3Sum, but track closest sum

---

## 6. 4Sum
- **LeetCode 18**

### 💡 Idea:
- Extend 3Sum logic

---

# 🔴 ADVANCED LEVEL

## 7. Trapping Rain Water
- **LeetCode 42**

### 💡 Idea:
- Two pointers + max tracking

---

## 8. Boats to Save People
- **LeetCode 881**

### 💡 Idea:
- Pair lightest with heaviest

---

# 🧠 PATTERN SUMMARY

| Problem Type | Approach |
|-------------|---------|
| Pair sum | Two pointers |
| Triplet sum | Fix one + two pointers |
| Closest sum | Track min difference |
| Max area | Move limiting factor |

---

# ⚠️ COMMON MISTAKES

- Forgetting to sort (for 3Sum/4Sum) ❌  
- Moving wrong pointer ❌  
- Not handling duplicates ❌  

---

# 🔥 INTERVIEW STRATEGY

When you see:

- “Find pair with sum”
- “Triplets that sum to zero”
- “Closest sum”

👉 Think: Sort+two Points

---

# 🚀 PRACTICE ORDER

1. 167  
2. 11  
3. 15 ⭐  
4. 16  
5. 42  

---

# ⚡ FINAL INSIGHT

> Opposite Two Pointers =  
> “Shrink search space using sorted order”
