# Sports Club & Event Management System (C)

A modular, console-based systems application developed in pure **C** to handle athlete profiles, club memberships, and tournament event tracking. The project emphasizes low-level data structure design, manual dynamic memory management, and persistent file storage.

---

## 🌟 Key Technical Highlights

* **Low-Level Memory Management & Dynamic Allocation:**
  * Uses manual allocation (`malloc`, `realloc`, `free`) to manage data on the heap without static buffer limitations.
  * Implements nested dynamic structures (athletes with dynamically sized arrays of attended events) ensuring zero memory leaks.

* **Custom Data Structures & Algorithms:**
  * Custom sorting algorithms for chronological and alphabetical event ordering.
  * Fast lookup and cross-referencing routines for duplicate detection and player history.
  * System-wide aggregations (e.g., determining top-performing clubs by tournament participation volume).

* **File I/O & Serialization:**
  * Parses and streams structured plain-text database records (`SportsmanData.txt`, `EventData.txt`).
  * Handles bidirectional serialization (loading on startup, flushing updates on demand).

* **Defensive CLI Architecture:**
  * Strict input buffer sanitation and type validation to prevent buffer overflows or unintended runtime crashes during terminal interactions.

---

## 🛠️ Architecture & Concepts

* **Language:** C (Standard C99 / C11)
* **Key Paradigms:** Procedural Programming, Systems Programming
* **Memory Management:** Heap Allocation, Pointer Arithmetic, Nested Structs
* **Storage:** File I/O Persistence

---
