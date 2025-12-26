# ATM Banking System Simulation

![Language](https://img.shields.io/badge/Language-C++-00599C?logo=c%2B%2B&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Windows_Console-0078D6)
![Status](https://img.shields.io/badge/Status-Educational-orange)

A console-based banking simulation built in **C++** that demonstrates Object-Oriented Programming (OOP) principles, file-based persistence, and role-based security.

This project simulates a real-world ATM environment where administrators can manage bank accounts and users can perform financial transactions with data persistence across sessions.

---

## 🏦 Key Features

### 🔐 Role-Based Access Control (RBAC)
* **Admin Mode:**
    * Secure Login with password masking.
    * Create, Delete, and Unlock User Accounts.
    * View global user lists and manage system data.
* **User Mode:**
    * Secure PIN authentication.
    * **Withdrawals:** Logic to handle minimum balances (50k VND) and specific denominations.
    * **Transfers:** Real-time fund transfers between valid account IDs.
    * **Change PIN:** Users can update their security credentials.

### 💾 Data Persistence & Logging
* **File I/O:** All account data (Balances, PINs, Names) is stored in structured text files, allowing the system to retain state after closing.
* **Audit Logs:** Every transaction (Withdrawal, Transfer) is automatically time-stamped and written to a dedicated history file (`LichSu[ID].txt`) for tracking.

## 🛠️ Technical Implementation

* **OOP Architecture:** functionality is encapsulated into distinct classes:
    * `QuanLyUser`: The core "Controller" managing business logic and file operations.
    * `Admin` / `User`: Model classes representing actors in the system.
* **Security:** Implements `_getch()` for masking password/PIN input (replacing characters with `*` in the console).
* **Safety Checks:**
    * Prevents withdrawing below the minimum balance (50,000 VND).
    * Locks accounts automatically after 3 incorrect PIN attempts.

## 🚀 How to Run

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/TonyTheSlacker/ATM.git](https://github.com/TonyTheSlacker/ATM.git)
    ```
2.  **Open in Visual Studio:**
    * Open `ATM.sln`
3.  **Build & Run:**
    * Select **Debug** or **Release** mode.
    * Press **F5** to compile and launch the console.

> **Note:** Ensure the data files (`Admin.txt`, `TheTu.txt`) are in the same directory as the executable, or the project will generate default ones.

---

### 📬 Contact
Created by **Tony** - *Computer Science Student*
