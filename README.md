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
| `checkout_search`, `create_cart`, `update_cart`, `create_checkout`, `set_delivery_details`, `select_shipping`, `complete_checkout` | Buy from a partner store that Zyft can check out at |

## Data the plugin sends

- **Searches and product questions** go to Zyft's server at `mcp.zyft.com`: the search terms and product IDs Claude passes to each tool. Zyft logs tool calls to run and improve the service.
- **Checkout**, only when you ask to buy: your name, email, phone number and delivery address go through Zyft's server to the store you are buying from. Card details you give for `complete_checkout` pass through Zyft's server to the store's payment provider to be tokenised; Zyft doesn't store them. Claude asks you to confirm the order total before placing the order.
- Zyft fetches product, price and stock data from retailers on its own servers. The plugin doesn't contact retailers from your machine.

See Zyft's [privacy policy](https://zyft.com/privacy-policy) and [terms](https://zyft.com/terms-conditions).

## Support

[help.zyft.com](https://help.zyft.com)

---

This repository is generated from Zyft's private source repository on each plugin release. Don't open pull requests here; contact support instead.
