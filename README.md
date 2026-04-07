# 📘 README — `var` vs `let` Interview Quiz

## 🗂️ Project Overview

This is a JavaScript interview-preparation quiz focused on deep understanding of `var` vs `let` behavior. It covers the most common and tricky concepts that appear in real frontend interviews.

---

## 🎯 Learning Objectives

- Understand **hoisting** and how `var` and `let` behave differently before execution
- Recognize the **Temporal Dead Zone (TDZ)** and when it triggers errors
- Distinguish **function scope** (var) from **block scope** (let)
- Identify **shadowing** traps across nested scopes
- Master the classic **closure + loop** trap with `setTimeout`
- Understand **function hoisting** vs **variable hoisting**
- Know when **re-declaration** causes errors

---

## 📋 Quiz Topics — 15 Questions

| # | Topic | Concept Tested |
|---|-------|----------------|
| 1 | Hoisting Trap | `var` is hoisted as `undefined` |
| 2 | Temporal Dead Zone | `let` throws ReferenceError before declaration |
| 3 | Function vs Block Scope | `var` leaks outside `if` blocks |
| 4 | Shadowing + TDZ | `let` inside function creates TDZ for outer `let` |
| 5 | Closure Problem (var) | Loop with `var` shares one `i` |
| 6 | Closure with `let` | Loop with `let` creates a new `i` per iteration |
| 7 | Nested Scope (Closure) | Inner function reads closest scope's variable |
| 8 | Re-declaration Error | `var` then `let` for same name = SyntaxError |
| 9 | Function vs Variable Hoisting | Function declarations hoist before `var` |
| 10 | Scope + Mutation | Modifying outer `let` from inside a function |
| 11 | Block Scope Leakage (var) | `var` inside `{}` leaks to outer scope |
| 12 | Block Scope (let) | `let` inside `{}` stays inside |
| 13 | Parameter Shadowing | Parameter hides outer variable with same name |
| 14 | Closure + Async Trap | `var` in `for` + `setTimeout` = shared variable |
| 15 | IIFE Fix (Advanced) | IIFE captures `i` per iteration to fix the trap |

---

## ⚡ Key Rules to Remember

### `var`
- **Function-scoped** — ignores `if`, `for`, `{}` blocks
- **Hoisted** as `undefined` — accessible before declaration but value is `undefined`
- **Can be re-declared** in the same scope
- **Shared across loop iterations** — dangerous with closures

### `let`
- **Block-scoped** — respects `{}` boundaries
- **Has TDZ** — accessing before declaration throws `ReferenceError`
- **Cannot be re-declared** in the same scope
- **New binding per iteration** — safe to use in closures inside loops

### Hoisting Order
```
Function declarations → var declarations → code runs
```
So `function foo(){}` wins over `var foo = 10` when both exist.

---

## 🛠️ Files

| File | Description |
|------|-------------|
| `js-quiz.html` | Interactive quiz UI — answer prediction questions with explanations |

---
🔗 Link: https://h-othman1515.github.io/Portfolio/js-quiz.html
