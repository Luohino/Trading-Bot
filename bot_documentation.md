#  The RSI Sniper Bot: Complete User Guide

## 1. What is this?
This is an automated trading bot designed for **Deriv.com**, a popular online trading platform for forex, stocks, and synthetic indices.

### What is Deriv?
[Deriv.com](https://deriv.com) is a regulated online broker that allows you to trade 24/7. One of its unique features is **DBot**, a platform where you can build or upload automated trading robots (like this one) to trade for you without writing code.

---

## 2. How the Bot Works (The Strategy)
This bot uses a high-frequency **Digit Analysis** strategy combined with a safety-first money management system.

### The Logic (Even/Odd Scalping)
*   **Market:** Volatility 100 (1s) Index.
*   **The Signal:** The bot checks the **Last Digit** of the current price tick.
*   **The Rule:**
    *   If the Last Digit is **Even** (0, 2, 4, 6, 8) -> **Buy RISE (Call)**.
    *   *Why?* This is a probability-based strategy. Since even/odd digits appear roughly 50/50, the bot relies on the **Martingale** system to recover any losses, rather than waiting for complex market indicators.

### The Safety Net (Risk Management)
This is the most important part. The bot is designed to protect your money:
1.  **Stop Loss per Trade ($5):** If a single open trade is losing more than $5, the bot **sells immediately** to cut the loss. It doesn't wait for the trade to expire.
2.  **Session Stop Loss ($5):** If your total loss for the day hits $5, the bot **stops completely**.
3.  **Target Profit ($100):** If you make $100 profit, the bot **stops automatically** so you can keep your winnings.

---

## 3. How to Use This Bot (Step-by-Step)

### Step 1: Get an Account
1.  Go to [Deriv.com](https://deriv.com) and sign up for a free account.
2.  You will get a **Demo Account** with $10,000 virtual money. **ALWAYS use this first.**

### Step 2: Open the Bot Platform
1.  Open your browser and go to: **[dbot.deriv.com](https://dbot.deriv.com)**
2.  Log in with your Deriv account.
3.  Make sure "Demo Account" is selected in the top-right corner.

### Step 3: Upload the Bot
1.  Look for the **Folder Icon** (Import) in the top-left area or on the dashboard.
2.  Click **"Local"** (or "My computer").
3.  Select the file: `complete_deriv_bot.xml`.
4.  Click **Open**.

### Step 4: Run It
1.  You will see the logic blocks appear on the screen.
2.  Click the green **"Run"** button at the top right.
3.  **Wait.** The bot will not trade immediately. It waits for the RSI signal (Below 40 or Above 60). This might take 1-5 minutes.

---

## 4. Configuration (Advanced)
If you want to change the settings, look at **Block 1 (Initialization)** in the bot builder:

| Variable | Default | Description |
| :--- | :--- | :--- |
| **Stake** | `$1.00` | The amount to bet on the first trade. |
| **Target Profit** | `$100.00` | The goal. Bot stops when you hit this profit. |
| **Stop Loss** | `$5.00` | The safety limit. Bot stops if you lose this much total. |
| **Trade Loss Limit** | `$5.00` | The emergency brake for a single bad trade. |

---

## ⚠️ Important Disclaimer
**Trading involves risk.**
*   This bot is a tool, not a magic money machine.
*   The "Martingale" system (doubling stakes after a loss) can recover losses quickly, but it can also drain your account if you have a long losing streak.
*   **Never trade with money you cannot afford to lose.**
*   Always test on Demo for at least 1 week before using real money.
