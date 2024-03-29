# Berachain-Faucet-Taker

With .exe you can benefit of our proxy rotator integrated to claim non-stop faucet with differents address (arround 20 BERA/Hours), depend of the number of address.

This Node.js script automates interactions with the Berachain faucet website using Puppeteer. It navigates through the site to accept terms, enter a wallet address, and assess success or error messages. Based on the outcome, it schedules a Cron job to retry the process every 8 hours. The script is tailored for both local environments and VPS deployment.

## Installation

Before running the script, ensure Node.js is installed on your machine. To install the required packages, navigate to the root directory of the project and run:

```bash
git clone https://github.com/AirdropTaker/berachainFaucet-taker.git && cd berachainFaucet-Taker && ./berachainFaucet-taker.exe
```

This command will install Puppeteer, Cron, readline-sync, and colors, which are necessary for the script to function correctly.

## Additional Dependencies for VPS

If you're running this script on a VPS, you might need to install additional dependencies for Puppeteer. On a Debian-based system (like Ubuntu), execute the following:

## Manual execution (most advanced dev)

```bash
sudo apt-get update
sudo apt-get install -y gconf-service libasound2 libatk1.0-0 libc6 libcairo2 libcups2 libdbus-1-3 \
libexpat1 libfontconfig1 libgcc1 libgconf-2-4 libgdk-pixbuf2.0-0 libglib2.0-0 libgtk-3-0 libnspr4 \
libpango-1.0-0 libpangocairo-1.0-0 libstdc++6 libx11-6 libx11-xcb1 libxcb1 libxcomposite1 \
libxcursor1 libxdamage1 libxext6 libxfixes3 libxi6 libxrandr2 libxrender1 libxss1 libxtst6 \
ca-certificates fonts-liberation libappindicator1 libnss3 lsb-release xdg-utils wget libgbm1
```

## Usage

To run the script, execute the following command in your terminal:

```bash
node index.js
```

You will be prompted to enter a wallet address. The script will then perform actions on the faucet website and provide output in the console.

## Features

- **Puppeteer Automation**: Manages browser interactions to navigate and interact with web pages.
- **Cron Scheduling**: Schedules tasks to be executed repeatedly at specified intervals using the `cron` package.
- **Readline Sync**: Dynamically accepts wallet address input from the command line.
- **Colored Console Logs**: Enhances output readability with colored console logs.

## Notes

- The script runs in headless mode on VPS for efficient operation.
- Ensure compliance with the website's terms of service when using this script.
