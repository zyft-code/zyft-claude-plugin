# Zyft for Claude

Zyft compares prices across Australian retailers. Ask Claude where something is cheapest, whether a price is genuinely low, or what the best deals are right now, and it answers with live prices from Zyft in AUD, with a direct link to each retailer.

## What you can ask

- "Find me the best price on Sony WH-1000XM5 headphones"
- "Is now a good time to buy a PS5? Show me the price history"
- "What are the best TV deals in Australia right now?"

## What the plugin contains

- **A remote MCP server** at `https://mcp.zyft.com/mcp`, run by Zyft. The plugin runs no code on your machine.
- **A skill** (`skills/zyft-shopping`) that tells Claude when to use Zyft's tools and how to present prices, deals and price history.

## Tools

| Tool | What it does |
|---|---|
| `search_products`, `get_product`, `get_offers` | Find products and compare retailer prices |
| `get_price_history` | Price history, all-time low and average for a product |
| `get_deals` | Current deals, each checked against the last 90 days of prices |
| `show_product_picker`, `show_deals`, `open_zyft_panel` | Show products and deals in an interactive view |

## Data the plugin sends

- **Searches and product questions** go to Zyft's server at `mcp.zyft.com`: the search terms and product IDs Claude passes to each tool. Zyft logs each tool call (the tool, its arguments and its result) to run and improve the service. You don't need a Zyft account, and the plugin sends no name, email or other account details.
- Zyft fetches product, price and stock data from retailers on its own servers. The plugin doesn't contact retailers from your machine, and nothing is bought on your behalf.

See Zyft's [privacy policy](https://zyft.com/privacy-policy) and [terms](https://zyft.com/terms-conditions).

## Support

[help.zyft.com](https://help.zyft.com)

---

This repository is generated from Zyft's private source repository on each plugin release. Don't open pull requests here; contact support instead.
