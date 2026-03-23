# 🚀 Kadane’s Algorithm — Complete Variants Guide

This file covers all important Kadane-based problems you need for interviews.

---

# 🟢 1. Standard Kadane (Maximum Subarray Sum)

## Problem:
Find maximum sum of a contiguous subarray.

## LeetCode:
- 53. Maximum Subarray

## Idea:
- Keep adding
- If sum < 0 → reset

---

# 🟡 2. Print the Subarray (Important Extension)

## Problem:
Return the actual subarray, not just sum

## Trick:
- Track start index
- Update when resetting

---

# 🔵 3. Minimum Subarray Sum

## Problem:
Find minimum sum subarray

## Idea:
- Reverse Kadane logic
- If sum > 0 → reset

---

# 🔴 4. Maximum Absolute Subarray Sum

## Problem:
Maximize |sum|

## LeetCode:
- 1749. Maximum Absolute Sum of Any Subarray

## Idea:
- Run Kadane twice:
  - max subarray
  - min subarray
- Answer = max(abs(maxSum), abs(minSum))

---

# 🟣 5. Maximum Circular Subarray

## Problem:
Array is circular

## LeetCode:
- 918. Maximum Sum Circular Subarray

## Idea:
Case 1: Normal Kadane  
Case 2: Circular = totalSum - minSubarray  

Final:
max(normal, circular)

⚠️ Edge case:
All negative → return max element

---

# 🟤 6. Maximum Product Subarray

## Problem:
Product instead of sum

## LeetCode:
- 152. Maximum Product Subarray

## Idea:
Track:
- maxProduct
- minProduct (because negative flips)

---

# ⚫ 7. K Concatenation Maximum Sum

## Problem:
Array repeated k times

## LeetCode:
- 1191. K-Concatenation Maximum Sum

## Idea:
- Use Kadane on 2 copies
- Use prefix + suffix if needed

---

# 🟠 8. Maximum Sum with One Deletion

## Problem:
Delete one element to maximize sum

## LeetCode:
- 1186. Maximum Subarray Sum with One Deletion

## Idea:
- Forward Kadane
- Backward Kadane
- Combine results

---

# 🔶 9. Maximum Alternating Subarray Sum

## Problem:
Alternate + and -

## LeetCode:
- 1911. Maximum Alternating Subsequence Sum

## Idea:
- Modified Kadane / DP

---

# 🔷 10. Maximum Sum Rectangle (2D Kadane)

## Problem:
Find max sum rectangle in matrix

## Idea:
- Fix left & right columns
- Compress rows
- Apply Kadane

---

# 🧠 CORE PATTERN SUMMARY

## Pattern 1:
👉 “Max sum” → Kadane

## Pattern 2:
👉 “Min sum” → Reverse Kadane

## Pattern 3:
👉 “Circular” → Total - Min

## Pattern 4:
👉 “Product” → Track min + max

## Pattern 5:
👉 “2D matrix” → Kadane inside loop

---

# ⚠️ COMMON MISTAKES

- Resetting incorrectly
- Ignoring all-negative case
- Not tracking indices
- Forgetting minProduct in product variant

---

# 🔥 FINAL INSIGHT

> Kadane is not about sum.  
> It’s about **deciding whether to continue or restart**.

---

# 🚀 NEXT STEP

Start solving in this order:

1. 53
2. 918
3. 152
4. 1186
5. 1749

Master these → you dominate Kadane questions.
