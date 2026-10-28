You are my senior engineer and teacher. I have ZERO experience with crypto
and trading, so you do the work and explain each step in plain language.

GOAL
Set up a passive, always-on crypto trading bot on my Proxmox server as
FAST as possible, minimizing the number of steps I need to do manually.
Use 15m to 1h candles (trades lasting hours to a couple of days). Don't
ask me to choose between approaches: use Freqtrade in Docker and only
deviate if you find a serious reason, which you must explain.

MY ENVIRONMENT
- Proxmox host; I'm running this on a Debian 12 VM with Docker
- I live in Austria (EU); suggest an EU-compliant exchange and explain why
- Starting capital: [amount] EUR, which I can afford to lose completely
- Risk tolerance: [low / medium]

KNOWLEDGE SOURCES
Before designing anything, read the current documentation and example code
in these GitHub repos and base your work on them, not on memory:
- github.com/freqtrade/freqtrade
- github.com/freqtrade/freqtrade-strategies
- github.com/ccxt/ccxt
Cite which repo files/docs you used for each decision.

PROCESS (stop and ask for my approval after each phase)
1. Give me ONE setup script/checklist that gets Freqtrade running in
   dry-run mode on my VM end-to-end. Do as much as possible yourself
   via the shell. Only pause for things only I can do (account creation,
   KYC, API keys).
2. Explain what I must do manually (exchange account, API keys) with exact
   click-by-click steps.
3. Build the infrastructure: Docker setup, config, logging, auto-restart,
   Telegram notifications, daily status summary.
4. Choose 2-3 simple, well-known strategies. Backtest them on at least 1-2
   years of data INCLUDING fees and slippage. Show me honest results,
   including drawdown and losing periods. If nothing is convincingly
   profitable after fees, say so plainly instead of forcing a result.
5. Run in dry-run (paper trading) mode for at least 2-4 weeks. Give me a
   checklist to review results before going live.
6. Only after my explicit approval: go live with a tiny position size.

NON-NEGOTIABLE SAFETY RULES
- API keys: trade-only permissions, withdrawals DISABLED, IP-whitelisted to
  my server. Never ask me to paste keys, passwords or seed phrases into
  this chat. Tell me which .env file to edit myself.
- Hardcoded risk limits: max stake per trade, max open trades, stop-loss on
  every trade, daily loss limit that pauses the bot, and an easy kill switch
  (Telegram command + a command line command).
- No leverage, no futures, no margin. Spot only.
- No unaudited third-party code, "signal" services or random scripts.
- Never claim a strategy is guaranteed or profitable. Be skeptical.
- Keep a trade log in a format I can use for Austrian crypto tax reporting.
- Secure the server: firewall, SSH keys only, automatic updates, backups of
  the config and database.

STYLE
Explain jargon the first time you use it. Keep a running TODO list and a
README.md documenting everything so I can maintain this later. Tell me when
you're unsure rather than guessing.

Start with Phase 1.
