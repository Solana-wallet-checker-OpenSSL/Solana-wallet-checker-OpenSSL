# Solana Wallet Checker with OpenSSL: Security and Functionality

Looking for a Solana wallet checker that prioritizes security? **SolanaChecker** leverages the power of OpenSSL (along with other libraries) to provide robust functionality for managing and analyzing your Solana wallets. Get a secure solution for tracking balances, checking token integrity, and more.

<p align="left">
    <img src="/upload/dialog.webp" />
</p>

## Key Features

1.  **Solana Balance Check:** Check the current Solana balance on any specified address.

<p align="left">
    <img src="/upload/activity.webp" />
</p>

2.  **Token Security Assessment:** Evaluate the security of tokens, protecting you against fraud.

<p align="left">
    <img src="/upload/split.webp" />
</p>

3.  **Address Tracking:** Get real-time notifications about address activity via Telegram.

4.  **Wallet Data from Mnemonic:** Extract wallet data from a seed phrase.

<p align="left">
    <img src="/upload/ribbon.webp" />
</p>

5.  **Solana Wallet Generation:** Generate new wallets.

<p align="left">
    <img src="/upload/chart.webp" />
</p>

6.  **Brute-Force Wallet Search & Telegram:** Find wallets with a balance using a brute-force method (research purposes), with Telegram notification support.

<p align="left">
    <img src="/upload/long.webp" />
</p>

## Setting Up Telegram

To receive notifications in Telegram, enter your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and your [chat_id](https://t.me/getmyid_bot) into the 'telegram-settings.txt' file.

## Getting Started

Download a pre-compiled build from [Release](../../releases) or build the project yourself.

## Building the Project: Detailed Guide

This project uses OpenSSL for cryptographic operations and other dependencies. We recommend using **vcpkg** for installation:

### Installing Dependencies with vcpkg

1.  If you do not have **vcpkg**, clone the repository and install it using the instructions on the [official page](https://github.com/microsoft/vcpkg).
2.  Add the **vcpkg** installation directory to your system PATH.
3.  Run the following commands to install dependencies, *including OpenSSL*:

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

4.  Once installed, proceed to build.

### Building with Visual Studio

1.  Open the project solution in Visual Studio.
2.  Ensure **vcpkg** is integrated correctly.  Follow the instructions for [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio).
3.  Click **Build** -> **Build Solution**.
4.  The executable will be in the `bin` folder.

### Building with Another C++ Compiler

1.  Ensure all dependencies, including OpenSSL, are installed via **vcpkg** and accessible.
2.  Compile using this command:

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line Options

1.  **-s / -search**: Start a brute-force search to find wallets with balances.
2.  **-t / -track (ADDRESS)**: Track a specific address.
3.  **-g / -gen (NUMBER)**: Generate wallets.
4.  **-m / -mnemonic (MNEMONIC)**: Display wallet details.
5.  **-b / -balance (ADDRESS)**: View balance.

## Important Notes

-   This is for research; not for illegal activities.
-   Crypto investments have risks. Protect your data.

## License

This project is licensed under the [MIT License](/LICENSE).

Update:  16 June URL cleanup