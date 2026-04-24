# 📘 Clean Code — Summary & Notes

> A concise summary of *Clean Code by Robert C. Martin (Uncle Bob)*

![License](https://img.shields.io/badge/license-MIT-green)
![Level](https://img.shields.io/badge/level-beginner--intermediate-blue)
![Topic](https://img.shields.io/badge/topic-clean--code-orange)

---

## 📚 About

This repository contains a **clear and structured summary** of key chapters from the book:

> **Clean Code: A Handbook of Agile Software Craftsmanship**  
> 👤 Author: Robert C. Martin

🎯 Goal: Help developers write **clean, readable, and maintainable code**

---

## 📑 Table of Contents

- [Meaningful Names](#-1-meaningful-names-chapter-2)
- [Functions](#-2-functions-chapter-3)
- [Comments](#-3-comments-chapter-4)
- [Objects & Data Structures](#-4-objects--data-structures-chapter-6)
- [Law of Demeter](#-law-of-demeter)
- [Conclusion](#-conclusion)

---

## 🔹 1. Meaningful Names (Chapter 2)

Good naming is critical in programming.

✔ A name should:
- Reveal intention  
- Be clear and unambiguous  
- Be easy to search and pronounce  

❌ Avoid:
- Misleading names (`accountList` if not a list)
- Single-letter names (except in small scopes)

📌 Rules:
- Classes → **Nouns**
- Methods → **Verbs**

---

## 🔹 2. Functions (Chapter 3)

Functions should be:

✔ Small  
✔ Focused  
✔ Doing **one thing only**

📏 Guidelines:
- Prefer < 20 lines
- Keep same level of abstraction

### Arguments:
- 0 → Best  
- 1 → Good  
- 2 → Acceptable  
- 3+ → Avoid  

⚠️ A function should be:
- A **Command** OR
- A **Query**
- ❌ Not both

---

## 🔹 3. Comments (Chapter 4)

> "Comments are a necessary evil"

💡 Prefer **clean code over comments**

### ✅ Good comments:
- Legal info
- Complex explanations
- Design decisions

### ❌ Bad comments:
- Redundant
- Outdated
- Commented-out code

👉 Truth lives in the **code**, not in comments.

---

## 🔹 4. Objects & Data Structures (Chapter 6)

### Objects:
- Hide data
- Expose behavior

### Data Structures:
- Expose data
- No behavior

📌 Trade-off:
- Procedural → easy to add functions
- OOP → easy to add new classes

---

## 📏 Law of Demeter

> "Talk to friends, not strangers"

Avoid deep chaining:

```js
obj.getA().getB().getC().doSomething(); // ❌ Bad
