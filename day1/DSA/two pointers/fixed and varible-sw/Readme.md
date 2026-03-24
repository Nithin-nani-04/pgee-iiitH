# 📖 Sliding Window — Fixed vs Variable (Clear Story)

---

# 🎭 Scene: Two Shops, Two Rules

Arjun is sent to a long street of shops:[2, 1, 5, 1, 3, 2]

But the king gives **two different missions**.

---

# 🟢 SCENE 1: Fixed Window (Strict Rule)

## 🎯 Rule

> “You must pick exactly 3 consecutive shops.”

---

## 🧠 Arjun’s Thinking

He realizes:

- He cannot take 2 shops ❌  
- He cannot take 4 shops ❌  
- It must ALWAYS be 3  

---

## ⚡ His Action

He takes:
[2, 1, 5]

Then moves forward:
[1, 5, 1]
[5, 1, 3]
[1, 3, 2]

---

## 🔥 Realization

> “I don’t need to rebuild the window…  
> I just slide it forward.”

---

## 🧠 Feeling

- Size never changes  
- Only position changes  

---

## ⚡ One Line

> “The window is fixed — just move it.”

---

# 🟡 SCENE 2: Variable Window (Flexible Rule)

## 🎯 Rule

> “You can take as many shops as you want…  
> but total must not exceed 7.”

---

## 🧠 Arjun’s Thinking

He starts small:

[2] → ok
[2, 1] → ok
[2, 1, 5] → sum = 8 ❌


---

## 🔧 What Now?

He doesn’t restart.

He adjusts:Remove 2 → [1, 5] → sum = 6 ✅

---

## 🔁 Continue

[1, 5, 1] → ok
[1, 5, 1, 3] → too big ❌


Shrink again:[5, 1, 3] → ok


---

## 🔥 Realization

> “I don’t have a fixed size…  
> I must adjust based on the condition.”

---

## 🧠 Feeling

- Window grows when possible  
- Shrinks when needed  

---

## ⚡ One Line

> “The window changes size to stay valid.”

---

# 🧠 FINAL DIFFERENCE (CRYSTAL CLEAR)

| Fixed Window | Variable Window |
|-------------|----------------|
| Size is fixed | Size changes |
| Only move forward | Expand & shrink |
| No condition check | Condition controls size |

---

# 🔥 CORE INSIGHT

- Fixed = **No thinking, just sliding**
- Variable = **Constant decision making**

---

# ⚡ MEMORY LINE

> Fixed → “Exactly k”  
> Variable → “At most / condition”

---

# 🏁 FINAL THOUGHT

Arjun didn’t change the street.

He changed how he **controls the window**.

















