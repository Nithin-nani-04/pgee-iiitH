# 📖 Prefix Sum Story — Scene 1, 2 & 3: The Real Challenge

## 🧩 Scene 1: The Tired Minister
(Recap)

Arjun was repeatedly calculating sums for different ranges.

Same array. Different queries. Same work again and again.

He felt:

> “I am repeating effort.”

---

## ⚡ Scene 2: The Advisor’s Trick
(Recap)

Ved introduced a scroll:
prefix = [2, 6, 7, 14, 17]

Now instead of recalculating:
Sum(L to R) = prefix[R] - prefix[L-1]



Arjun learned:

> “Prepare once → Answer forever”

---

# 🔥 Scene 3: The King’s Trap

The king was impressed… but not satisfied.

He leaned forward and said:

> “Now I want something harder.”

He gave the same array: [2, 4, 1, 7, 3]


And asked:

> “Tell me… how many subarrays have sum = 7?”

---

## 😨 Arjun Tries Old Method

Arjun started:

- [2] → 2  
- [2,4] → 6  
- [2,4,1] → 7 ✅  
- [4,1,7] → 12  
- [1,7] → 8  
- [7] → 7 ✅  
- [4,1,7,3] → 15  
...

Too many subarrays.

Too slow.

---

## ⚠️ The Failure

Arjun realized:

> “Prefix sum helped with ranges…  
> but now I need to count all subarrays.”

He was stuck again.

---

## 🧠 Ved’s Second Lesson

Ved smiled.

> “You are still thinking like before…  
> calculating every subarray.”

He continued:

> “This time, don’t look forward… look backward.”

---

## 🔍 The Key Observation

Ved asked:

> “If current sum is `currSum`,  
> what should exist before it to make sum = K?”

Then he wrote: currSum - K = previous prefix sum


---

## ⚡ The Breakthrough

Ved explained:

> “If you have already seen a prefix sum equal to `currSum - K`,  
> then a subarray with sum K exists.”

---

## 🧠 How Arjun Thinks Now

As Arjun moves through the array:

He keeps track of:

- Current sum  
- All previous prefix sums  

---

## 📦 The Memory Trick

Ved introduces a map:


---

## ⚡ The Breakthrough

Ved explained:

> “If you have already seen a prefix sum equal to `currSum - K`,  
> then a subarray with sum K exists.”

---

## 🧠 How Arjun Thinks Now

As Arjun moves through the array:

He keeps track of:

- Current sum  
- All previous prefix sums  

---

## 📦 The Memory Trick

Ved introduces a map: Map<prefixSum, frequency>


---

## 🔥 The Process

For every element:

1. Add to current sum  
2. Check:       currSum - K exists?

3. If yes → count increases  
4. Store current sum in map  

---

## 🎯 Example Insight

When current sum becomes `7`:

- Check: `7 - 7 = 0`

If `0` existed before → subarray found

---

## ⚡ The Final Realization

Arjun understood:

> “I don’t need to generate all subarrays…  
> I just need to detect patterns in prefix sums.”

---

## 🔥 The New Rule

> “If problem asks for subarrays with a condition,  
> think in terms of prefix relationships.”

---

## 🧠 Mental Upgrade

Before: Generate → Check → Count

Now:Track → Match → Count

---

## 🚀 What This Scene Teaches

Use Prefix + HashMap when:

- Problem says "subarray sum = K"  
- You need count of subarrays  
- Brute force is too slow  

---

## ⚡ One Line to Remember

> “Find what must exist before, instead of checking everything.”


