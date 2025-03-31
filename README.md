# ATM System in C

## Description

This is a simple ATM (Automated Teller Machine) simulation program written in C. It allows users to check their balance, withdraw cash, deposit money, and exit the system. The program ensures secure access by requiring a PIN for authentication.

## Features

- PIN authentication to access ATM services
- Balance inquiry
- Cash withdrawal with validation for multiples of 100 and sufficient balance check
- Cash deposition
- Option to perform multiple transactions in one session
- Graceful exit message after transactions

## Requirements

- A C compiler (e.g., GCC, Turbo C, or any other C compiler)
- A terminal or command-line interface to run the program

## Compilation & Execution

1. Compile the program using GCC:
   ```sh
   gcc atm.c -o atm
   ```
2. Run the compiled executable:
   ```sh
   ./atm
   ```

## How to Use

1. Enter the correct PIN (default: `1234`).
2. Choose from the available options:
   - `1` to check balance.
   - `2` to withdraw cash (only in multiples of 100 and maintaining a minimum balance of Rs. 500).
   - `3` to deposit money.
   - `4` to exit the program.
3. After each transaction, the program asks if you want to continue (`y/n`).
4. If `n` is entered, the session ends with a thank-you message.

## Code Explanation

- Uses a `while` loop to validate the PIN entry.
- Implements a `do-while` loop to allow multiple transactions.
- Uses a `switch` statement for transaction selection.
- Ensures proper balance validation during withdrawals.

## Sample Output

```
Type your secret pin number: ****
Hello! Welcome to our ATM Service
1. Balance Checking
2. Cash Withdrawal
3. Cash Deposition
4. Exit
??
Please proceed with your choice: 1
The account balance in Rs: 2000
Would you like to have another ATM transaction? (y/n): y
```

## Notes

- The PIN is hardcoded as `1234`. Modify the code to allow dynamic PIN entry.
- Use `fflush(stdin);` carefully as it may not work as expected on all compilers. A better alternative is using `getchar()` or clearing the input buffer manually.
