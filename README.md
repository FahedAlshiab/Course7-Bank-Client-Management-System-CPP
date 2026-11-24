# Bank Client Management System (C++)

![Language](https://img.shields.io/badge/Language-C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![IDE](https://img.shields.io/badge/IDE-Visual_Studio_2026-5C2D91?style=for-the-badge&logo=visualstudio&logoColor=white)
[![Course](https://img.shields.io/badge/Course_07-Capstone_Project-orange?style=for-the-badge)](https://github.com/FahedAlshiab/07-Algorithms-Problem-Solving-Level-3)

A console-based **Bank Client Management System** built in C++ as the capstone project (including the Bank Extension) for **[Course 07: Algorithms & Problem Solving Level 3](https://github.com/FahedAlshiab/07-Algorithms-Problem-Solving-Level-3)**. It implements a menu-driven client administration and financial transactions suite backed by flat-file persistence (`Clients.txt`), consolidating custom string tokenization, record serialization, full CRUD operations, and balance management into a unified application.

---

## Core Features

### Main Menu

| Option | Feature | Description |
| :---: | :--- | :--- |
| **[1]** | **Show Client List** | Renders all persisted records in a formatted console table with total client count. |
| **[2]** | **Add New Client** | Validates account number uniqueness before appending new records to `Clients.txt`. |
| **[3]** | **Delete Client** | Confirms `[Y/N]`, flags the record (`MarkForDelete`), and rewrites the file. |
| **[4]** | **Update Client Info** | Previews current details, confirms `[Y/N]`, and persists updated fields. |
| **[5]** | **Find Client** | Searches by `AccountNumber` and displays the client details card. |
| **[6]** | **Transactions** | Opens the financial transactions sub-menu (`Deposit`, `Withdraw`, `Total Balances`). |
| **[7]** | **Exit** | Cleanly terminates the session. |

### Transactions Menu (`[6]`)

| Option | Feature | Description |
| :---: | :--- | :--- |
| **[1]** | **Deposit** | Validates positive deposit amounts, confirms `[Y/N]`, and increments `AccountBalance` in `Clients.txt`. |
| **[2]** | **Withdraw** | Enforces overdraft limits (`Amount <= AccountBalance`), confirms `[Y/N]`, and deducts from balance. |
| **[3]** | **Total Balances** | Renders a condensed account balance table and computes aggregate funds across all clients. |
| **[4]** | **Main Menu** | Returns control cleanly to the primary navigation loop. |

---

## Live Demo

<details>
<summary><strong>[1] & [5] Show Client List & Search</strong></summary>
<br>


https://github.com/user-attachments/assets/272b8ba1-f113-45a7-9476-2d61970104c0


</details>

<details>
<summary><strong>[2], [3] & [4] Client CRUD Operations (Add, Update & Delete)</strong></summary>
<br>



https://github.com/user-attachments/assets/4e823d9f-f6f2-4db8-8e31-6e83b019dcc5


</details>

<details>
<summary><strong>[6] & [7] Transactions Module & Clean Exit</strong></summary>
<br>


https://github.com/user-attachments/assets/822618ea-318d-4598-afa1-1f46282555d9


</details>

---

## System Architecture & Data Flow

Client entities are modeled via `struct sClient` and persisted in `Clients.txt` using a custom `#//#` field delimiter:

```text
AccountNumber#//#PinCode#//#Name#//#Phone#//#AccountBalance
A101#//#1234#//#Fahed Alshiab#//#0791234567#//#12500.500000
