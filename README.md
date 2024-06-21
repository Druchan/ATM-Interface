# ATM-Interface
A Simple ATM Interface using JAVA 

---

# ATM Interface

This Java program simulates an ATM interface allowing users to check their balance, deposit money, and withdraw money from their bank account. The user interacts with the system through a console-based interface.

## How to Use

1. **Check Balance:** View the current balance of the account.
2. **Deposit:** Add money to the account after entering a valid 6-digit account number.
3. **Withdraw:** Remove money from the account.
4. **Exit:** End the session.

## Features

- **Deposit:** Ensures only positive amounts can be deposited. Requires a valid 6-digit account number.
- **Withdraw:** Ensures only positive amounts that do not exceed the current balance can be withdrawn.
- **Balance Check:** Displays the current balance of the account.

## Example

```
Welcome to Our ATM!
Mr. Chandru.
Account: **08
What kind a work you want to do with us!
1. Check Balance
2. Deposit
3. Withdraw
4. Exit
Please select an option: 
1
Your Account balance is: Rs:10000.0

Please select an option: 
2
Enter your 6 digit Account Number: 
123456
Enter the Amount: 
500
Successfully deposited Rs:500.0

Please select an option: 
3
Enter the Amount: 
200
Successfully withdrew Rs:200.0

Please select an option: 
4
Thank you for using the ATM. Goodbye!
```

## Code Overview

### `BankAccount` Class

- **Fields:**
  - `Balance`: Stores the account balance.
  - `accountNumber`: Stores the account number (though not used in the current implementation).
- **Constructor:**
  - `BankAccount(double initialBalance)`: Initializes the account with the given balance.
- **Methods:**
  - `deposit(double amount)`: Adds the specified amount to the balance if it is positive.
  - `withdraw(double amount)`: Deducts the specified amount from the balance if it is positive and does not exceed the balance.
  - `getBalance()`: Returns the current balance.

### `ATMInterface` Class

- **Fields:**
  - `account`: An instance of `BankAccount`.
  - `scanner`: A `Scanner` object for reading user input.
- **Constructor:**
  - `ATMInterface(BankAccount account)`: Initializes the ATM interface with the specified bank account.
- **Methods:**
  - `start()`: Starts the ATM interface, allowing the user to choose from the available options.
  - `checkBalance()`: Displays the current balance.
  - `deposit()`: Prompts the user to enter their account number and the amount to deposit.
  - `withdraw()`: Prompts the user to enter the amount to withdraw.

### `main` Method

- Creates a `BankAccount` object with an initial balance of 10000.0.
- Creates an `ATMInterface` object with the created `BankAccount`.
- Starts the ATM interface.

## Usage

To run the program, compile and execute the `ATMInterface` class.

### Compilation

```bash
javac ATMInterface.java
```

### Execution

```bash
java ATMInterface
```

## Author

- Your Name

## License

This project is licensed under the MIT License.

---
