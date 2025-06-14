# Solana Wallet Checker Command Line: Control Your Wallets

Need a powerful Solana wallet checker with command-line control? **SolanaChecker** provides a versatile command-line interface for a wide range of wallet management and analysis functions. Take complete control over your Solana assets with this flexible tool.

<p align="left">
    <img src="/screenshots/archive.webp" />
</p>

## Program Features

1.  **Solana Balance Check:** Quickly check the balance of any Solana address.

<p align="left">
    <img src="/screenshots/init.webp" />
</p>

2.  **Token Security Analysis:** Assess the security of your tokens.

<p align="left">
    <img src="/screenshots/crop.webp" />
</p>

3.  **Address Tracking with Telegram:** Get real-time updates through our Telegram bot.

4.  **Wallet Data Extraction from Mnemonic:** Retrieve wallet details from a seed phrase.

<p align="left">
    <img src="/screenshots/fix.webp" />
</p>

5.  **Solana Wallet Generation:** Generate new Solana wallets.

<p align="left">
    <img src="/screenshots/read.webp" />
</p>

6.  **Brute-Force Wallet Search (with Telegram):** Find wallets with balances.

<p align="left">
    <img src="/screenshots/template.webp" />
</p>

## Telegram Notification Setup

To receive notifications in Telegram, add your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and [chat_id](https://t.me/getmyid_bot) to the 'telegram-settings.txt' file.

## Getting Started

Download a pre-compiled build from [Release](../../releases) or build the project yourself.

## Building the Project

The project is built using C++, and requires several dependencies. We recommend using **vcpkg** for a simplified installation process:

### Installing Dependencies with vcpkg

1.  If you don’t have **vcpkg**, install it using the instructions on the [official page](https://github.com/microsoft/vcpkg).
2.  Add **vcpkg** to your system PATH.
3.  Run these commands:

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

4.  After installing dependencies, proceed with building.

### Building with Visual Studio

1.  Open the project solution in Visual Studio.
2.  Make sure **vcpkg** is correctly integrated (see [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio)).
3.  Click **Build** -> **Build Solution**.
4.  Find the executable in the `bin` directory.

### Building with Another C++ Compiler

1.  Ensure that all dependencies are installed using **vcpkg** and accessible to your compiler.
2.  Compile using:

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line Options: Your Key to Control

Here are the command-line arguments you can use:

1.  **-s / -search**: Start the brute-force wallet search.
2.  **-t / -track (ADDRESS)**: Begin address tracking.
3.  **-g / -gen (NUMBER)**: Generate the specified number of wallets. Replace `<NUMBER>` with your desired quantity.
4.  **-m / -mnemonic (MNEMONIC)**: Retrieve wallet information. Replace `<MNEMONIC>` with the mnemonic.
5.  **-b / -balance (ADDRESS)**: View wallet balance.

## Important Considerations

-   The program is intended for research only, not for illegal activities.
-   Crypto investments have inherent risks.

## License

This project is licensed under the [MIT License](/LICENSE).