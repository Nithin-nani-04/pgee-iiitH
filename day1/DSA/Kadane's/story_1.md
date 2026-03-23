# 📖 Kadane’s Algorithm — Scene 1: The Gambling Street

## 🎭 The Beginning

Arjun walks into a long street filled with gambling games.

Each game has a number:[ -2, 1, -3, 4, -1, 2, 1, -5, 4 ]

Rules:
- Positive → he earns money 💰  
- Negative → he loses money 💸  

---

## 🎯 The Goal

Arjun wants to:

> “Earn the maximum money by playing a **continuous sequence of games**.”

⚠️ He cannot skip randomly — it must be continuous.

---

## 😓 First Approach (Brute Force Thinking)

Arjun tries everything:

- Start from every position  
- Try all possible subarrays  
- Calculate their sums  

Examples:
- [-2]  
- [-2, 1]  
- [-2, 1, -3]  
- [1, -3, 4]  
- [4, -1, 2, 1]  

---

## ⚠️ The Problem

Too many possibilities.

Time is running out.

Arjun feels:

> “I am doing too much work…”

---

## 🧠 The Key Observation

While playing, he notices something important:

At one point: -2 + 1 + (-3) = -4


Now he thinks:

> “If I continue from here… I’m already in loss.”

---

## ⚡ The First Real Insight

Arjun realizes:

> “Why should I carry a loss forward?”

---

## 🔥 The Rule is Born

He makes a decision:

> “If my current total becomes negative… I will drop it and start fresh.”

---

## 🧠 Mental Shift

Before: Try all possibilities
Now:
Make decision at each step


---

## 🎯 What This Scene Teaches

- You don’t need to check all subarrays  
- Negative sum is harmful for future  
- Drop bad past, focus on future  

---

## ⚡ One Line to Remember

> “Never carry a negative sum forward.”

---
# 📖 Kadane’s Algorithm — Scene 2: The Winning Strategy

## 🎭 The Situation Continues

Arjun is still on the gambling street: [ -2, 1, -3, 4, -1, 2, 1, -5, 4 ]


But now… he has a rule:

> “If my total becomes negative, I restart.”

---

## 🧠 The Plan

Arjun decides to track two things:

1. **current sum** → money he has right now  
2. **maximum sum** → best money he has ever seen  

---

## ⚡ The Strategy

At each step:

1. Add current game value  
2. Update maximum  
3. If current sum becomes negative → reset to 0  

---

## 🧪 Step-by-Step Walkthrough

Start:
current = 0
max = -∞

---

### Step 1: -2
current = -2
max = -2
👉 Negative → reset to 0

---

### Step 2: 1
current = 1
max = 1

---

### Step 3: -3
current = -2

👉 Reset to 0

---

### Step 4: 4
current = 4
max = 4

---

### Step 5: -1
current = 3


---

### Step 6: 2
current = 5
max = 5


---

### Step 7: 1

current = 6
max = 6

---

### Step 8: -5
current = 1

---

### Step 9: 4
current = 5


---

## 🎯 Final Answer

Maximum Sum = 6


Subarray:[4, -1, 2, 1]


---

## 🔥 What Just Happened?

Arjun never checked all subarrays.

Instead, he:
- Made a decision at every step  
- Dropped bad past  
- Carried forward good momentum  

---

## 🧠 Core Formula (Hidden Inside Story)
current = max(arr[i], current + arr[i])
max = max(max, current)


---

## ⚡ Mental Model

At every step ask:

> “Is it better to continue… or restart from here?”

---

## 🎯 What This Scene Teaches

- Kadane is greedy  
- Local decision → global optimum  
- Reset is the key  

---

## 🔥 One Line to Remember

> “At every step: continue or restart.”



















