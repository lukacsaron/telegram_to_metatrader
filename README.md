# TTMT – Telegram to MetaTrader

TTMT copies trading signals from Telegram channels into MetaTrader 4 and MetaTrader 5 accounts. It reads each channel message with an AI parser, places the orders on your broker account through a cloud connection, and manages the position afterwards. No virtual private server (VPS) or always-on terminal is needed.

**[telegramtometatrader.com](https://telegramtometatrader.com/?utm_medium=owned&utm_source=github&utm_campaign=marketplace)**

This repository is the project's public page on GitHub. TTMT is a hosted service, so there is no code to download here. The open parts live in their own repositories, listed [below](#open-repositories).

## What it does

- **Reads the messages channels actually write.** Complete signals, alerts followed by details, and follow-up messages such as closing a trade or moving the stop to breakeven.
- **Checks prices before it trades.** TTMT compares signal prices against the live market and rejects values that look like typos.
- **Layers the entry.** An entry can be split into up to 6 layers inside the entry zone, with volume spread across up to 6 take-profit levels.
- **Manages the trade afterwards.** Stops move to breakeven and trail, and an account halts for the day when its daily loss limit is reached.
- **Routes one signal to several accounts.** Demo, live, and prop-firm accounts, each with its own settings.
- **Keeps a trace.** Every decision on every trade is recorded, so a result can be audited step by step.

It is built for traders who follow forex, gold, and index signal channels and want the trades executed without copying them by hand. It does not pick trades and it is not a signal provider.

## Who should not use it

- You follow one channel that posts a few clean signals a week. A free copier on your own machine can be the right call, and [this page says when](https://telegramtometatrader.com/free-telegram-signal-copier?utm_medium=owned&utm_source=github&utm_campaign=marketplace).
- You want crypto-exchange execution. TTMT trades MetaTrader accounts only.
- You expect a copier to make a losing channel profitable. It executes what the channel posts.

## Pricing

Every plan starts with a 7-day free trial, and a card is required to start it. Yearly billing costs ten months of the monthly price.

| Plan | Monthly | MetaTrader accounts |
|---|---|---|
| Essential | $39 | 1 |
| Pro | $99 | 5 |
| Master | $149 | 10 |

Current plans and limits are on the [pricing section](https://telegramtometatrader.com/?utm_medium=owned&utm_source=github&utm_campaign=marketplace#pricing).

## Measured channel data

TTMT publishes what happened when its users copied each channel: closed trades, win rate, profit factor, and the share of traders in profit. The figures come from executed trades on MetaTrader accounts.

- [Gold (XAUUSD) channels ranked by real trades](https://telegramtometatrader.com/explore/rankings/gold?utm_medium=owned&utm_source=github&utm_campaign=marketplace)
- [How the numbers are counted](https://telegramtometatrader.com/explore/methodology?utm_medium=owned&utm_source=github&utm_campaign=marketplace), including the conflict of interest
- [The full channel directory](https://telegramtometatrader.com/explore?utm_medium=owned&utm_source=github&utm_campaign=marketplace)

Each month's figures are written up in [Signal Channels, Counted](https://telegramcopytrader.substack.com/p/gold-signal-channels-on-telegram), and the snapshots are kept in [telegram-gold-signal-rankings](https://github.com/lukacsaron/telegram-gold-signal-rankings).

## Open repositories

| Repository | What it is |
|---|---|
| [telegram-signal-format](https://github.com/lukacsaron/telegram-signal-format) | An open specification of how Telegram trading signals are written and how software should read them |
| [telegram-signal-test-corpus](https://github.com/lukacsaron/telegram-signal-test-corpus) | Fixtures and a JSON Schema for testing a signal parser |
| [ttmt-mcp](https://github.com/lukacsaron/ttmt-mcp) | Reference for the read-only Model Context Protocol (MCP) connector that lets Claude or ChatGPT answer questions about your own trading data |

## Frequently asked questions

**How do I copy Telegram signals to MetaTrader?**
Connect your Telegram account, connect a MetaTrader 4 or 5 account, and choose which channels trade on which account. From then on each signal in those channels is parsed and executed on its own. Setup guides: [MetaTrader 5](https://telegramtometatrader.com/telegram-to-mt5?utm_medium=owned&utm_source=github&utm_campaign=marketplace) and [MetaTrader 4](https://telegramtometatrader.com/telegram-to-mt4?utm_medium=owned&utm_source=github&utm_campaign=marketplace).

**Do I need a VPS or to keep MetaTrader open?**
No. TTMT runs in the cloud and connects to your broker account directly.

**Does it work with private or VIP channels?**
It reads the channels your own Telegram account is a member of, public or private.

**Can it trade a prop-firm account?**
It can connect one. Whether your firm allows copied signals is the firm's rule, not ours, and [this guide covers what to check](https://telegramtometatrader.com/prop-firm-copy-trading?utm_medium=owned&utm_source=github&utm_campaign=marketplace).

**Is this repository the source code?**
No. TTMT is a hosted, paid service and its code is not open source. The specification, the test corpus, and the connector reference linked above are.

**Is this financial advice?**
No. TTMT executes signals you choose to follow. Trading leveraged products can lose you money quickly. Past results do not predict future results.

## Links

- Website: [telegramtometatrader.com](https://telegramtometatrader.com/?utm_medium=owned&utm_source=github&utm_campaign=marketplace)
- Documentation: [docs.telegramtometatrader.com](https://docs.telegramtometatrader.com/?utm_medium=owned&utm_source=github&utm_campaign=marketplace)
- Telegram: [@ttmtapp](https://t.me/ttmtapp)

Operated by jazzrabbit OÜ, registry code 16489902, Estonia.
