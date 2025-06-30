# ShadowDEX Bot

ShadowDEX is a Telegram-based crypto trading bot and aggregator that integrates multiple exchange APIs and provides advanced trading features.

## Features
- Crypto price aggregation
- Trade execution via Telegram commands
- Portfolio tracking
- P2P payment integration (planned)

## Setup Instructions

1. Clone the repo:
   ```bash
   git clone https://github.com/Mufasazw/shadowdex_bot.git
   cd shadowdex_bot


Google sheet progress report updated by Kudzai Chabvuta: https://docs.google.com/spreadsheets/d/1aBOn3cdWD7HqEp1oy-vMCaYuZraCAfgD/edit?usp=sharing&ouid=103860471818529164564&rtpof=true&sd=true



## 30 June 2025 update

✅ Commit Message:

Fix: Improve /price command accuracy by enforcing symbol-based token lookup


---

📝 Update Summary for README or Changelog:

🚀 Enhancements

Reworked /price command to use only token symbols for CoinGecko ID mapping (e.g., /price btc, /price eth, /price sol).

Added a fallback map (TOKEN_ID_MAP) with hardcoded popular token symbols to avoid incorrect matches from CoinGecko's coins/list API.

Implemented a safe population method to extend TOKEN_ID_MAP with additional symbols from CoinGecko—without overwriting trusted defaults.


🛠 Fixes

Fixed issue where token names (e.g., bitcoin) returned incorrect prices due to conflicts with clone/scam tokens on CoinGecko.

Prevented ambiguous lookups by disabling token name matching—only symbols are accepted now (like btc, not bitcoin).


💡 Notes

Usage of /price must now be strictly by token symbol:

✅ /price btc

✅ /price eth

❌ /price bitcoin (will now return a helpful error)


This greatly improves accuracy and security of price responses.



