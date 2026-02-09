# Idiomatic Patterns & Anti-Patterns

This document defines the specific coding norms enforced by the Overseer.

## Python Norms

### Resource Management
* **Anti-Pattern:** Manually opening/closing files or database connections.
* **Standard:** Use Context Managers (`with` statement) to ensure cleanup even during exceptions.

### Control Flow
* **Anti-Pattern:** Deeply nested `if` statements checking for success conditions.
* **Standard:** Guard clauses that check for failure conditions and return early.

## C++ Norms

### Memory Management
* **Anti-Pattern:** Using `new` and `delete` manually.
* **Standard:** Use `std::make_unique` or `std::make_shared`.

### Iteration
* **Anti-Pattern:** C-style `for` loops with index counters when accessing all elements.
* **Standard:** Range-based `for` loops (`for (const auto& item : items)`).

## General Refactoring Targets
1.  **Dead Code:** Remove unused variables and unreachable code blocks immediately.
2.  **Magic Numbers:** Replace unnamed numerical constants with named `CONSTANTS`.
3.  **Boolean Zen:** Simplify `if (isValid == true)` to `if (isValid)`.
