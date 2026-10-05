# 🏧 ATM System Console Application (C++)

A simple ATM simulation built from scratch in C++. Clients log in with their **account number and PIN**, then withdraw, deposit, and check their balance through a clean command-line interface. All data is read from and saved to a plain text file (`Clients.txt`), the same format used by the Bank System project, so the two work together out of the box.

> 🚨 **Note:** Feel free to fork, modify, or use this as a learning resource! 🛠️

---

## ✨ Features

- 🔐 **Login Screen**
  - Authenticates by account number + PIN code
  - Shows an error and re-prompts on invalid credentials

- 📋 **Main Menu**
  - ⚡ **Quick Withdraw**: one-tap amounts (20, 50, 100, 200, 400, 600, 800, 1000)
  - 💸 **Normal Withdraw**: custom amount (must be a multiple of 5)
  - 💵 **Deposit**: positive amounts only
  - 📊 **Check Balance**: view your current balance
  - 🚪 **Logout**: returns to the login screen

- 🛡️ **Safety Checks**
  - Prevents overdraft (withdrawal can't exceed balance)
  - Confirmation prompt (`y/n`) before every transaction

- 💾 **Data Persistence**
  - Reads from and writes to `Clients.txt` using a custom delimiter (`#//#`)
  - Balance updates are saved instantly after each transaction

---

## 🛠️ How to Compile & Run

1. Save the source code as `Atm-System.cpp`.
2. Compile with any C++ compiler (e.g., g++):

   ```bash
   g++ Atm-System.cpp -o ATM
   ```

3. Make sure `Clients.txt` is in the same folder, then run:

   ```bash
   ./ATM
   ```

> 💡 Uses `system("cls")` and `system("pause")`, so it's designed for **Windows**. On Linux/macOS, replace them with `clear` and a `cin.get()`.

---

## 📄 Data File Format

Each line in `Clients.txt` represents one client:

```
AccountNumber#//#PinCode#//#Name#//#Phone#//#Balance
```

**Example:**

```
A150#//#1234#//#Mohammed Ali#//#0500000000#//#5000.000000
```

---

## 🔗 Related Project

🏦 **Bank System Console Application**: the admin side for managing clients (add, update, delete, search). Both projects share the same `Clients.txt` file.
