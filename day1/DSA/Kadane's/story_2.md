# 📖 Kadane’s Algorithm — Scene 3: The Circular Trap

## 🎭 The King Changes the Game

Arjun has mastered the street.

But the king smiles and says:

> “Now the street is not straight… it is a circle.”

---

## 🔁 The New Street [5, -3, 5]

Now Arjun can:
- Start anywhere  
- Continue to end  
- AND wrap around to the beginning  

---

## 🎯 The Goal

> “Find the maximum money from a continuous circular path.”

---

## 😓 First Attempt (Old Thinking)

Arjun tries normal Kadane:

- [5] → 5  
- [5, -3] → 2  
- [5, -3, 5] → 7  

Max = 7

---

But then he notices something:

👉 What about:
[5] + [5] (wrap around)


= 10

---

## ⚠️ The Problem

Normal Kadane **cannot see circular connections**

---

## 🧠 The Breakthrough Thought

Arjun thinks differently:

> “Instead of finding the best path…  
> what if I remove the worst part?”

---

## 🔍 The Key Idea

Total sum:5 + (-3) + 5 = 7


Worst subarray:[-3]

So:Best circular = total - worst = 7 - (-3) = 10


---

## ⚡ Final Strategy

Two cases:

### Case 1: Normal Kadane :max1 = max subarray sum

---

### Case 2: Circular Case
max2 = totalSum - minSubarray

---

## 🎯 Final Answer
answer = max(max1, max2)


---

## ⚠️ Critical Edge Case

If all numbers are negative:

Example:[-3, -2, -5]


Then:
- minSubarray = total
- total - min = 0 ❌ (invalid)

👉 So return: max element


---

## 🧠 Mental Model

Normal Kadane:
> “Find best segment”

Circular Kadane:
> “Remove worst segment”

---

## 🔥 What This Scene Teaches

- Sometimes solving directly is hard  
- Solve indirectly by removing bad part  
- Think in terms of total + exclusion  

---

## ⚡ One Line to Remember

> “Maximum circular sum = total sum - minimum subarray”


# 📖 Kadane’s Algorithm — Scene 4: The Multiplication Trap

## 🎭 The King Changes the Rules Again

Arjun returns confidently.

But the king says:

> “No more addition… now everything is multiplication.”

---

## 🔢 The New Street:[2, 3, -2, 4]


Rules:
- Positive → profit  
- Negative → danger  
- Multiply everything  

---

## 🎯 The Goal

> “Find the maximum product of a continuous subarray.”

---

## 😓 First Attempt (Old Kadane Thinking)

Arjun tries:

- 2 → 2  
- 2 × 3 = 6  
- 6 × (-2) = -12 ❌  
- Start again from 4  

Max = 6

---

But something feels wrong…

---

## ⚠️ The Problem

Arjun realizes:

> “A negative number can flip everything.”

Example: (-2) × (-3) = 6


👉 A bad (negative) can suddenly become very good!

---

## 🧠 The Breakthrough

Arjun changes thinking:

> “I must track both good and bad outcomes.”

---

## 🔥 New Strategy

At every step, track:

- **maxProduct** → best possible  
- **minProduct** → worst possible (important!)

---

## ⚡ Why track min?

Because:

> “Today’s worst can become tomorrow’s best.”

---

## 🧪 Step-by-Step Walkthrough

Start:max = 2
min = 2
result = 2


---

### Step 2: 3
max = max(3, 2×3) = 6
min = min(3, 2×3) = 3


result = 6

---

### Step 3: -2

⚠️ Negative → swap max & min

max = max(-2, 3×(-2)) = -2
min = min(-2, 6×(-2)) = -12

---

### Step 4: 4
max = max(4, -2×4) = 4
min = min(4, -12×4) = -48

---

## 🎯 Final Answer
Maximum Product = 6

Subarray:[2, 3]


---

## 🧠 Mental Model

Addition world:
> “Drop negative”

Multiplication world:
> “Negative can become positive later”

---

## 🔥 Core Rule

> “Track both maximum and minimum at every step.”

---

## ⚡ Formula
if (num < 0) swap(max, min)

max = max(num, max * num)
min = min(num, min * num)

result = max(result, max)


---

## 🎯 What This Scene Teaches

- Negative numbers flip outcomes  
- You cannot discard bad values  
- You must carry both possibilities  

---

## ⚡ One Line to Remember

> “In product problems, the worst value can become the best.”


# 📖 Kadane’s Algorithm — Scene 5: The One Mistake Allowed

## 🎭 The King Shows Mercy

Arjun has mastered addition and multiplication.

The king now says:

> “You may skip ONE bad game.”

---

## 🔢 The Street: [1, -2, 0, 3]

---

## 🎯 The Goal

> “Find the maximum sum of a subarray…  
> but you are allowed to delete exactly one element.”

---

## 😓 First Thought (Old Kadane)

Arjun tries normal Kadane:

Best subarray: [0, 3] → sum = 3

---

But then he thinks:

👉 What if I remove `-2`?

[1, 0, 3] → sum = 4


Better!

---

## ⚠️ The Challenge

Arjun realizes:

> “At each position… I have two choices.”

1. Continue normally  
2. Delete one bad element  

---

## 🧠 The Breakthrough

He decides to track two states:

### 1. No Deletion Yet

forward[i]

→ Maximum sum ending at i (normal Kadane)

---

### 2. One Deletion Used

backward[i]


→ Maximum sum starting from i

---

## 🔥 The Core Idea

If we delete element at index `i`: result = forward[i-1] + backward[i+1]


---

## 🧪 Example Thinking

At `-2`:

- Left side: `1`
- Right side: `0 + 3 = 3`

So:1 + 3 = 4


---

## ⚡ Final Strategy

1. Run Kadane from left → build `forward[]`  
2. Run Kadane from right → build `backward[]`  
3. Try deleting each element  

---

## 🎯 Final Answer:Maximum sum = 4

---

## 🧠 Mental Model

Before:
> “Continue or restart”

Now:
> “Continue, restart… or skip one mistake”

---

## 🔥 What This Scene Teaches

- You must track multiple possibilities  
- One decision is not enough  
- Combine past and future  

---

## ⚡ One Line to Remember

> “Best answer may come after removing one bad element.”


# The Final Boss

# 📖 Kadane’s Algorithm — Scene 6: The City of Grids (2D Kadane)

## 🎭 The Final Challenge

Arjun has mastered the street.

Now the king takes him to a city… arranged in a grid:

[
[ 1, 2, -1],
[-3, 4, 5],
[ 2, -1, 3]
]


---

## 🎯 The Goal

> “Find the rectangle (not just a line) with the maximum sum.”

---

## 😨 The Difficulty

Now it's not 1D.

Arjun must choose:
- Top row  
- Bottom row  
- Left column  
- Right column  

Too many rectangles ❌

---

## 🧠 The Breakthrough Thought

Arjun realizes:

> “I know how to solve 1D…  
> can I convert 2D into 1D?”

---

## 🔥 The Trick

Fix two columns:

👉 Left = 0  
👉 Right = 0  

Now collapse rows: [1, -3, 2]


Apply Kadane → best subarray

---

## ⚡ Expand Right

Now:

👉 Left = 0  
👉 Right = 1  

Add column-wise:
[1+2, -3+4, 2+(-1)] = [3, 1, 1]


Apply Kadane again

---

## 🔁 Repeat Process

For every pair of columns:

1. Collapse rows into 1D array  
2. Apply Kadane  
3. Track maximum  

---

## 🧠 Mental Model

2D problem becomes:

> “Multiple 1D problems stacked together”

---

## 🔥 Final Strategy

for (left = 0 → n-1):
temp = [0...0]

for (right = left → n-1):
    add column to temp
    apply Kadane on temp
    update result


---

## 🎯 Key Insight

- Fix boundaries (columns)  
- Reduce dimension  
- Apply known algorithm  

---

## ⚡ What This Scene Teaches

- Complex problems = combination of simple ones  
- Kadane is reusable  
- Dimensional reduction is powerful  

---

## 🧠 Final Realization

Arjun understands:

> “I don’t need new algorithms…  
> I need to reuse what I know in smarter ways.”

---

# 🏁 END OF JOURNEY

## 🔥 Complete Kadane Understanding

| Scene | Concept |
|------|--------|
| 1 | Drop negative |
| 2 | Continue vs restart |
| 3 | Circular logic |
| 4 | Product (track min & max) |
| 5 | One deletion |
| 6 | 2D Kadane |

---

## ⚡ Final Line

> “Kadane is not an algorithm…  
> it is a decision strategy.”






