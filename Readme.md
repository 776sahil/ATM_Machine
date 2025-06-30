# ATM Simulator

## Overview
This Java-based ATM Simulator project mimics the functionality of a basic Automated Teller Machine (ATM). It allows users to log in with a customer number and PIN, select between checking and savings accounts, and perform operations such as viewing balances, withdrawing money, and depositing funds.

## Features
- **User Authentication**: Secure login using a predefined customer number and PIN.
- **Account Selection**: Choose between Checking and Savings accounts.
- **Account Operations**:
  - View account balance.
  - Withdraw money (with balance validation).
  - Deposit funds.
- **User-Friendly Interface**: Console-based menu for easy navigation.
- **Error Handling**: Validates user inputs and prevents invalid transactions (e.g., withdrawing more than the available balance).

## Project Structure
The project consists of three main Java files:
- **`Account.java`**: Contains the core logic for managing account details, balances, and transaction operations (withdrawals and deposits).
- **`OptionMenu.java`**: Extends `Account.java` and provides the interactive menu system for user login and account operations.
- **`ATM.java`**: The main class that initializes the ATM system and starts the login process.

## Prerequisites
- **Java Development Kit (JDK)**: Version 8 or higher.
- **IDE**: Any Java-compatible IDE (e.g., IntelliJ IDEA, Eclipse) or a command-line environment with `javac` and `java` commands.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/atm-simulator.git
   ```
2. Navigate to the project directory:
   ```bash
   cd atm-simulator
   ```
3. Compile the Java files:
   ```bash
   javac ATM.java OptionMenu.java Account.java
   ```
4. Run the application:
   ```bash
   java ATM
   ```

## Usage
1. **Login**:
   - Enter a valid customer number (e.g., `952141` or `989947`).
   - Enter the corresponding PIN (e.g., `191904` for `952141` or `717976` for `989947`).
   - Invalid inputs will prompt an error and allow retry.
2. **Select Account Type**:
   - Choose `1` for Checking Account, `2` for Savings Account, or `3` to exit.
3. **Perform Operations**:
   - Select `1` to view balance, `2` to withdraw, `3` to deposit, or `4` to exit.
   - For withdrawals and deposits, enter the amount when prompted. The system will validate the transaction and display the updated balance.

## Example Interaction
```plaintext
Welcome to ATM
Enter your Customer Number
952141
Enter your PIN Number
191904
Select Account Type you want to Access
Type 1 - Checking Account
Type 2 - Savings Account
Type 3 - Exit
1
Checking Account
Type 1 - View Balance
Type 2 - Withdraw Money
Type 3 - Deposit Funds
Type 4 - Exit
1
Checking Account Balance: $0.00
```

## Limitations
- The user data (customer number and PIN) is hardcoded in a `HashMap` for simplicity.
- No persistent storage; account balances reset when the program terminates.
- Limited error handling for non-numeric inputs in some cases.

## Future Improvements
- Add persistent storage (e.g., database or file-based) for user data and balances.
- Implement advanced security features (e.g., encrypted PINs).
- Enhance error handling for all user inputs.
- Add support for multiple users and account types.
- Introduce a graphical user interface (GUI) for better user experience.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.