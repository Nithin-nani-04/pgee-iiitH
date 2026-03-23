# 🚀 Kadane’s Algorithm — LeetCode Practice List

This list is structured to take you from **basic → advanced → interview level**.

---

# 🟢 LEVEL 1: Core Kadane

## 1. Maximum Subarray ⭐
- **LeetCode 53**
- The foundation of Kadane

## 🎯 What to Learn:
- Reset when sum < 0
- Track maximum sum

---

# 🟡 LEVEL 2: Slight Variations

## 2. Maximum Sum Circular Subarray ⭐
- **LeetCode 918**

## 🎯 What to Learn:
- Normal Kadane
- Circular logic = total - min subarray

---

## 3. Maximum Absolute Sum of Any Subarray
- **LeetCode 1749**

## 🎯 What to Learn:
- Run Kadane twice (max + min)

---

# 🔵 LEVEL 3: Product Twist

## 4. Maximum Product Subarray ⭐
- **LeetCode 152**

## 🎯 What to Learn:
- Track max & min
- Handle negatives

---

# 🔴 LEVEL 4: Decision-Based Kadane

## 5. Maximum Subarray Sum With One Deletion ⭐
- **LeetCode 1186**

## 🎯 What to Learn:
- Forward + backward Kadane
- Combine results

---

# 🟣 LEVEL 5: Advanced Patterns

## 6. K Concatenation Maximum Sum
- **LeetCode 1191**

## 🎯 What to Learn:
- Extend Kadane logic
- Handle repeated arrays

---

## 7. Maximum Alternating Subsequence Sum
- **LeetCode 1911**

## 🎯 What to Learn:
- Kadane + DP thinking

---

# ⚫ LEVEL 6: 2D Kadane

## 8. Maximum Sum Rectangle (GFG / Similar Problems)

## 🎯 What to Learn:
- Convert 2D → 1D
- Apply Kadane inside loops

---

# 🧠 MUST KNOW TEMPLATE (Java)

```java
public int maxSubArray(int[] nums) {
    int current = nums[0];
    int max = nums[0];

    for(int i = 1; i < nums.length; i++) {
        current = Math.max(nums[i], current + nums[i]);
        max = Math.max(max, current);
    }

    return max;
}
