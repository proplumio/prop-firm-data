# Prop firm data

Open datasets about futures and forex prop trading firms, from [PropLumio](https://proplumio.com). Every figure comes from the firm's own website, checkout or help center and is re-checked regularly. A scheduled job copies the files here from proplumio.com every day.

| File | What it contains | Source page |
| --- | --- | --- |
| [`data/prop-firm-statistics.csv`](data/prop-firm-statistics.csv) | One row per firm and account size: price, billing, activation fee, profit target, max drawdown, daily loss limit, profit split, drawdown type, consistency rules, payout speed, platforms and the date each firm was last verified | [Prop firm statistics](https://proplumio.com/prop-firm-statistics) |
| [`data/prop-firm-changes.csv`](data/prop-firm-changes.csv) | A dated log of changes we confirmed on the firms' sites: new and ended discount codes, price changes, rule updates and new or renamed plans, each with a source link | [Prop firm news](https://proplumio.com/prop-firm-news) |

## Columns

**prop-firm-statistics.csv**

`firm`, `market` (futures or forex), `review_url`, `account_size_usd`, `price`, `price_currency`, `price_usd`, `billing` (monthly or one-time), `activation_fee_usd`, `profit_target_usd`, `max_drawdown_usd`, `daily_loss_limit_usd`, `headline_profit_split_pct`, `evaluation_drawdown_types`, `consistency_rule_evaluation`, `consistency_rule_funded`, `consistency_thresholds_pct`, `fastest_payout`, `platforms`, `last_verified`. List prices, before any discount code.

**prop-firm-changes.csv**

`date` (the day we confirmed the change), `firm`, `type` (code, price, rule or plan), `change`, `detail`, `source`.

## How the data is collected

Our monitoring checks every covered firm's codes, prices and rules daily, and every program and account size weekly. Anything that changes is verified in a browser on the firm's own pages before it is published. We don't use coupon sites, rumors or unverifiable claims. See the [methodology](https://proplumio.com/methodology).

Prices and rules change often. Always confirm a firm's current terms on its own site before buying a challenge. This data is for information only and is not financial advice.

## License and citation

The data is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You may use it in articles, videos, research and products, including commercial ones, as long as you credit PropLumio and link to the source page.

> PropLumio, "Prop firm statistics" and "Prop firm news: rule, price and code changes", https://proplumio.com

See [`CITATION.cff`](CITATION.cff) for a machine-readable citation. Questions or corrections: hello@proplumio.com.
