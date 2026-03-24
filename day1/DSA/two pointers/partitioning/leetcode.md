# 🚀 Partitioning (Two Pointer) — LeetCode Guide

Partitioning is a technique used to rearrange elements in an array based on a condition, without fully sorting the array. Instead of organizing everything, Arjun focuses only on placing elements into the correct side or group. This makes the approach faster and more efficient, usually reducing time complexity from O(n log n) (sorting) to O(n).

We use partitioning when a problem asks to move or group elements, such as pushing all zeros to one side, separating positive and negative numbers, or dividing elements around a pivot. The key idea is simple: scan the array once and place elements where they belong using swaps. There is no need to compare every element with every other element like sorting does.

Partitioning is especially useful when the problem does not require full ordering, but only grouping. For example, in problems like “Move Zeroes” or “Remove Element,” Arjun only cares about separating valid and invalid elements. In more advanced cases like “Sort Colors,” the array is divided into multiple zones (like 0s, 1s, and 2s), and pointers are used to maintain boundaries between these zones. In pivot-based problems such as QuickSort or QuickSelect, partitioning helps split the array into elements smaller than, equal to, or greater than a chosen pivot.

The core logic is based on two pointers. One pointer scans the array, and another pointer keeps track of where the next valid element should go. Whenever a condition is satisfied, elements are swapped and the boundary pointer is moved forward. This ensures that the left side always contains correctly placed elements, while the rest of the array is yet to be processed.

Common places where partitioning appears include rearranging arrays in-place, grouping elements based on conditions, solving Dutch National Flag problems, and finding kth largest or smallest elements using QuickSelect. It is widely used in interview problems because it combines efficiency with in-place manipulation.

Some important LeetCode problems to practice this technique are:
 283. Move Zeroes  
 27. Remove Element  
 75. Sort Colors  
 2161. Partition Array According to Given Pivot  
 215. Kth Largest Element in an Array  

While using partitioning, common mistakes include incorrect swapping, moving pointers in the wrong order, and forgetting that some swapped elements need to be rechecked. The biggest conceptual mistake is trying to sort the entire array when only grouping is required.

The final takeaway is that partitioning is not about ordering everything — it is about placing elements into the correct side efficiently. Whenever a problem asks to group, separate, or rearrange elements without full sorting, partitioning is often the right approach.


# 🚀 Partitioning (Two Pointer) — Important LeetCode Questions

This list covers the **most important problems** where partitioning is used directly or indirectly.

---

# 🟢 BASIC (Must Start Here)

 283. Move Zeroes ⭐  
 27. Remove Element  
 905. Sort Array By Parity  
 922. Sort Array By Parity II  

👉 Focus:
- Basic swapping
- In-place rearrangement

---

# 🟡 INTERMEDIATE (Core Understanding)

 75. Sort Colors ⭐ (Dutch National Flag)  
 2161. Partition Array According to Given Pivot ⭐  
 88. Merge Sorted Array (in-place idea)  
 977. Squares of a Sorted Array  

👉 Focus:
 Multi-pointer partition
 Zone-based thinking

---

# 🔵 PARTITION + SELECTION

 215. Kth Largest Element in an Array ⭐  
 347. Top K Frequent Elements  
 973. K Closest Points to Origin  

👉 Focus:
 QuickSelect
 Partition with pivot

---

# 🔴 ADVANCED / INTERVIEW LEVEL

 324. Wiggle Sort II  
 280. Wiggle Sort  
 406. Queue Reconstruction by Height  
 870. Advantage Shuffle  

👉 Focus:
 Rearrangement logic
 Pattern recognition

---

# ⚫ HYBRID (Partition + Other Techniques)

 11. Container With Most Water  
 42. Trapping Rain Water  
 15. 3Sum ⭐  
 16. 3Sum Closest  

👉 Focus:
 Partition thinking + two pointers

---

# 🧠 MUST DO (HIGH PRIORITY)

If short on time, do these:

1. 283 ⭐  
2. 75 ⭐  
3. 2161 ⭐  
4. 215 ⭐  
5. 15 ⭐  

---

# 🚀 PRACTICE ORDER

## Day 1:
- 283  
- 27  
- 905  

---

## Day 2:
- 75  
- 2161  

---

## Day 3:
- 215  
- 347  

---

## Day 4:
- 15  
- 11  

---

# ⚡ FINAL INSIGHT

> Partitioning problems are not about sorting —  
> they are about **placing elements in correct zones efficiently**














