# 🔁 Undo / Redo Simulation in C++

A simple yet powerful **Undo/Redo system simulation** implemented in **C++** using the **Stack data structure**.

This project demonstrates how modern applications (such as text editors) manage **history states** to allow users to revert or reapply changes.

Instead of relying on built-in libraries, the logic is implemented manually to better understand **data structures, state management, and OOP design**.

---

# 📌 Project Overview

Many modern applications support **Undo / Redo functionality**, such as:

- Text Editors (VS Code, Notepad++, Word)
- Graphic Design Tools (Photoshop, Illustrator)
- IDEs and Development Tools

These systems allow users to:

✔ Undo previous actions  
✔ Restore undone actions  

This project **simulates that behavior** using **two stacks** to store history states.

---

# 🧠 Core Concept

The system relies on **two stacks**:

### 1️⃣ Undo Stack
Stores all previous states of the value.

When a new value is assigned:
- The current value is pushed into the **Undo stack**

### 2️⃣ Redo Stack
Stores states that were undone.

When an **Undo** operation occurs:
- The current state moves to the **Redo stack**

When a **Redo** operation occurs:
- The state is restored back from the **Redo stack**

This mechanism allows moving **backward and forward through the history**.

---

# 🏗 Project Architecture

The project contains a custom class:

### `clsMyString`

This class simulates a string object with built-in **Undo / Redo functionality**.

It internally manages:

```
Current Value
Undo Stack
Redo Stack
```

### Internal Structure

```
Current Value
     │
     ├── Undo Stack (history)
     │
     └── Redo Stack (recovered states)
```



---

# 🧪 Program Output

```
Undo/Redo Project

S1  =
S1  = Abdelghani
S1  = Abdelghani 2
S1  = Abdelghani 3

Undo:
__________

S1 after undo = Abdelghani 2
S1 after undo = Abdelghani
S1 after undo =

Redo:
__________

S1 after Redo = Abdelghani
S1 after Redo = Abdelghani 2
S1 after Redo = Abdelghani 3
```

---

# 📦 Data Structure Used

This implementation relies on:

### **Stack (LIFO — Last In First Out)**

Why stacks?

Because **Undo/Redo operations follow a last-action pattern**:

The most recent change is always the first to be undone.

```
Push → Save state
Pop  → Restore state
```

This makes **Stack the perfect structure** for implementing history navigation.

---

# 🎯 Learning Objectives

This project helps reinforce several important concepts:

### Data Structures
- Stack
- LIFO behavior

### Object Oriented Programming
- Encapsulation
- Class design
- Controlled state management

### Software Design Thinking
- Managing history states
- Simulating real application behavior
- Separating logic from usage

---

# 🚀 Real-World Applications

Undo / Redo systems are widely used in:

- Text Editors
- IDEs
- Graphic Design Software
- Version Control Tools
- Game State Systems
- Document Editing Platforms

Understanding this pattern helps developers build **more interactive and user-friendly software**.

---

# 🛠 Technologies Used

- **C++**
- **STL Stack**
- **Object-Oriented Programming**
- **State Management Concepts**

---

# 📚 Educational Context

This project is part of a learning journey focused on:

- Mastering **Data Structures**
- Practicing **OOP in C++**
- Understanding how **real software systems are designed internally**

Instead of only using ready-made tools, the goal is to **understand the logic behind them**.

---

# 📂 Project Files

- `clsMyString.h` → Core class implementing Undo/Redo logic
- `Undo-Redo-Simulation-CPP.cpp` → Demonstration program

  ---
  
# 💡 Key Takeaway

Undo / Redo systems may seem simple from the user's perspective.

But internally they rely on **carefully managed history states** and efficient data structures.

By implementing this manually, we gain deeper insight into:

- Data structure design
- Software architecture
- Application behavior simulation

---


# ⭐ If you found this project useful

Consider giving the repository a **star ⭐**.

It helps support the project and motivates further learning and development.
