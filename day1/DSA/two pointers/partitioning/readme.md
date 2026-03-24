# 📖 Partitioning — The Story of Arjun Organizing the Crowd

## 🎭 Scene: The Festival Entrance

Arjun is standing at the entrance of a festival.

People are arriving in a random order:[2, 0, 2, 1, 1, 0]



Each number represents a group:
- 0 → VIP  
- 1 → Regular  
- 2 → Late entry  

---

## 🎯 The King’s Order

The king says:

> “Arrange them so that:
> - VIPs come first  
> - Then regular  
> - Then late entries”

---

## 😓 First Thought (Wrong Way)

Arjun thinks:

> “Let me sort them completely”

But sorting:
- Takes extra work ❌  
- Not required ❌  

---

## 🧠 The Breakthrough

Arjun realizes:

> “I don’t need full sorting…  
> I just need to put people in the right zones”

---

# ⚡ The Three Zones

He divides space into 3 parts:
[0 zone | 1 zone | unknown | 2 zone]


---

## 🏃 Three Pointers

- `low` → where next 0 should go  
- `mid` → current person  
- `high` → where next 2 should go  

---

## 🔁 The Process

### Case 1: Person = 0
Swap with low
Move low++
Move mid++


👉 VIP goes to front

---

### Case 2: Person = 1

Just move mid++


👉 Already in correct zone

---

### Case 3: Person = 2

Swap with high
Move high--


👉 Late entry goes to end

⚠️ Don’t move mid yet (new value needs checking)

---

## 🧪 Walkthrough

Start:[2, 0, 2, 1, 1, 0]


Step by step, Arjun rearranges without sorting.

Final result:[0, 0, 1, 1, 2, 2]



---

# 🧠 What Arjun Really Did

He didn’t sort.

He:
- Scanned once  
- Placed elements in correct zones  
- Used pointers to control boundaries  

---

# 🔥 Core Insight

> “Partitioning is about placing elements where they belong, not sorting everything”

---

# ⚡ Mental Model

Instead of:Sort entire array ❌

Think:Push elements to correct side ✅


---

# 🎯 When Arjun Uses This

- Move zeros to end  
- Separate positives & negatives  
- Sort colors (0,1,2)  
- QuickSort partition  

---

# ⚡ One Line to Remember

> “Divide space into zones and place elements accordingly”

---

# 🏁 Final Thought

Arjun didn’t rearrange everything.

He just made sure:
> “Each element moves toward its correct zone”
>
> like we did it quick sort
















