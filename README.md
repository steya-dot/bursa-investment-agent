# 🇲🇾 Bursa Malaysia Investment Strategist Agent

> A professional, institutional-grade AI investment strategist specializing in **Bursa Malaysia equities** and **REITs**, powered by Claude AI. Trade via [Moomoo Malaysia](https://www.moomoo.com/my).

---

## 📌 Overview

This agent skill transforms Claude into a disciplined portfolio manager with deep expertise in Malaysian capital markets. It provides data-driven analysis, entry/exit strategies, and portfolio simulation for Bursa-listed securities — without hype or speculative noise.

**Core Coverage:**
- Malaysian REITs (PAVREIT, SUNREIT, IGBREIT, KLCC, SENTRAL, YTLREIT, etc.)
- Blue-chip Equities (PBBANK, MAYBANK, CIMB, INARI, TENAGA, etc.)
- Bursa Malaysia Main Market & ACE Market

---

## ✨ Key Capabilities

| Feature | Description |
|---|---|
| 📊 **Stock Analysis** | Fundamental + technical analysis on Bursa-listed tickers |
| 🏢 **REIT Specialist** | Yield analysis, NAV comparison, occupancy trends |
| 🎯 **Entry & Exit Planning** | Buy zones, profit targets, stop-loss levels |
| 📐 **Position Sizing** | Risk-adjusted allocation (max 10–15% per REIT) |
| 🔁 **Portfolio Backtesting** | Simulated 3-year performance with dividend tracking |
| 📅 **Horizon Planning** | Short (6M), Medium (12M), Long-term (2Y) strategies |
| ⚖️ **Comparative Analysis** | Side-by-side REIT and equity rankings |
| 🔔 **Rebalancing Triggers** | Quarterly or price-deviation-based alerts |

---

## 🚀 Quick Start

### Option 1: Claude.ai Projects
1. Go to [Claude.ai](https://claude.ai) → **Projects** → **New Project**
2. Click **Set Instructions** (Custom system prompt)
3. Copy and paste the contents of [`system_prompt.md`](./system_prompt.md)
4. Start chatting with your Bursa investment strategist

### Option 2: Anthropic API
```python
import anthropic

with open("system_prompt.md", "r") as f:
    system_prompt = f.read()

client = anthropic.Anthropic()
message = client.messages.create(
    model="claude-opus-4-5",
    max_tokens=2048,
    system=system_prompt,
    messages=[
        {"role": "user", "content": "Analyze PAVREIT vs SUNREIT for a 12-month income portfolio."}
    ]
)
print(message.content[0].text)
```

### Option 3: Direct API (JavaScript)
```javascript
const response = await fetch("https://api.anthropic.com/v1/messages", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
    "x-api-key": process.env.ANTHROPIC_API_KEY,
    "anthropic-version": "2023-06-01"
  },
  body: JSON.stringify({
    model: "claude-opus-4-5",
    max_tokens: 2048,
    system: SYSTEM_PROMPT, // contents of system_prompt.md
    messages: [{ role: "user", content: "Give me a buy zone for IGBREIT." }]
  })
});
```

---

## 💬 Example Prompts

```
"Compare PAVREIT, SUNREIT, and IGBREIT. Which offers the best risk-adjusted yield for 2025?"

"I have RM 50,000 to invest. Build me a Bursa REIT portfolio with entry prices and stop-losses."

"Backtest a portfolio of PBBANK 40% + MAYBANK 30% + INARI 30% over 3 years."

"What is the ideal entry price for SENTRAL REIT given current DPU and NAV data?"

"Create a 6-month trading plan for INARI with profit targets and risk management rules."

"Rebalance my portfolio: I'm overweight KLCCP. What should I trim and reallocate to?"
```

---

## 📁 Repository Structure

```
bursa-investment-agent/
├── README.md              ← You are here
├── system_prompt.md       ← Core agent system prompt (paste into Claude)
├── agent_config.json      ← Metadata for Edge Gallery / API config
├── examples/
│   ├── reit_analysis.md   ← Sample REIT comparative analysis output
│   ├── portfolio_plan.md  ← Sample RM 50K portfolio construction
│   └── entry_exit.md      ← Sample entry/exit strategy output
└── LICENSE
```

---

## ⚠️ Disclaimer

> This agent is for **educational and informational purposes only**. It does not constitute licensed financial advice under the Capital Markets and Services Act 2007 (CMSA). Always conduct your own due diligence and consult a licensed investment advisor before making any investment decisions. Past performance of simulated portfolios does not guarantee future results.

---

## 📜 License

MIT License — see [`LICENSE`](./LICENSE) for details.

---

## 🔗 Links

- 💹 **Trade on Moomoo Malaysia**: [moomoo.com/my](https://www.moomoo.com/my)
- 📈 **Bursa Malaysia**: [bursamalaysia.com](https://www.bursamalaysia.com)
- 🤖 **Claude AI**: [claude.ai](https://claude.ai)
- 📚 **Anthropic Docs**: [docs.anthropic.com](https://docs.anthropic.com)
