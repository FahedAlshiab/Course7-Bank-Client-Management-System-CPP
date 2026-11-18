# Bank Client Management System (C++)

![Language](https://img.shields.io/badge/Language-C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![IDE](https://img.shields.io/badge/IDE-Visual_Studio_2026-5C2D91?style=for-the-badge&logo=visualstudio&logoColor=white)
[![Course](https://img.shields.io/badge/Course_07-Capstone_Project-orange?style=for-the-badge)](https://github.com/FahedAlshiab/07-Algorithms-Problem-Solving-Level-3)

A console-based **Bank Client Management System** built in C++ as the capstone project for **[Course 07: Algorithms & Problem Solving Level 3](https://github.com/FahedAlshiab/07-Algorithms-Problem-Solving-Level-3)**. It implements a menu-driven client administration suite backed by flat-file persistence (`Clients.txt`), consolidating custom string tokenization, record serialization, and full CRUD operations into a unified application.

---

## Core Features

| Option | Feature | Description |
| :---: | :--- | :--- |
| **[1]** | **Show Client List** | Renders all persisted records in a formatted console table with total client count. |
| **[2]** | **Add New Client** | Validates account number uniqueness before appending new records to `Clients.txt`. |
| **[3]** | **Delete Client** | Confirms `[Y/N]`, flags the record (`MarkForDelete`), and rewrites the file. |
| **[4]** | **Update Client Info** | Previews current details, confirms `[Y/N]`, and persists updated fields. |
| **[5]** | **Find Client** | Searches by `AccountNumber` and displays the client details card. |
| **[6]** | **Exit** | Cleanly terminates the session. |

---

## System Architecture & Data Flow

Client entities are modeled via `struct sClient` and persisted in `Clients.txt` using a custom `#//#` field delimiter:

```text
AccountNumber#//#PinCode#//#Name#//#Phone#//#AccountBalance