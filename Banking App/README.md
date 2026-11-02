# Banking System

A command-line banking application written in Python that uses an SQLite database to store card accounts and their balances. Users can create an account, log in with a card number and PIN, check their balance, add income, transfer money, close an account, and log out.

## Features

- Create a bank account with a generated card number and PIN.
- Generate card numbers with a Luhn checksum digit.
- Log in using a card number and PIN.
- View the account balance.
- Add income to an account.
- Transfer money to another existing card account.
- Validate a recipient card number using the Luhn algorithm.
- Close an account.
- Store account information persistently in an SQLite database.

## Requirements

- Python 3
- SQLite support (included with Python through the `sqlite3` module)
- No third-party Python packages are required.

## How to Run

1. Save `banking.py` to a folder on your computer.
2. Open a terminal or command prompt in that folder.
3. Run:

   ```bash
   python banking.py
   ```

   On some systems, use:

   ```bash
   python3 banking.py
   ```

4. Follow the menu displayed in the terminal.

## Main Menu

When the program starts, it displays these options:

| Option | Action |
|---|---|
| `1` | Create an account |
| `2` | Log into an account |
| `0` | Exit the application |

## Account Menu

After a successful login, the account menu provides:

| Option | Action |
|---|---|
| `1` | Display the current balance |
| `2` | Add income |
| `3` | Transfer money to another card |
| `4` | Close the account |
| `5` | Log out |
| `0` | Exit the application |

## Database

The application connects to an SQLite database named `card.s3db` in the current working directory. It creates a `card` table if the table does not already exist.

The table contains these columns:

| Column | Description |
|---|---|
| `id` | Integer primary key |
| `number` | Card number, stored as text |
| `pin` | Account PIN, stored as text |
| `balance` | Account balance, defaulting to `0` |

The database file is created automatically when the application runs.

## Card Number Validation

The program uses the **Luhn algorithm** to calculate a checksum digit when generating a card number. It also uses a Luhn validation method when checking a recipient's card number before a transfer.

## Project Structure

```text
.
├── banking.py
└── card.s3db       # Created automatically when the program runs
```

## Important Notes

- Keep the generated card number and PIN private.
- The database is stored locally in the folder from which the program is run.
- This is a learning/demo project, not a production-ready banking system.
- The current implementation uses SQL statements built with string interpolation. For real applications, use parameterized SQL queries to help prevent SQL injection, and use secure password/PIN hashing rather than storing PINs in plain text.
- The transfer and balance-handling logic should be reviewed and tested carefully before using this code for anything beyond practice.

## Author

Add your name and contact details here if you would like to include author information.
