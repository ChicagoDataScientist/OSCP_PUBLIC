# 📘 Jarvis Investment Prospectus  
_Stark Alpha Systems – Strategic AI-Driven Portfolio Framework_  
_Version 1.1 · Updated March 2025_

---

## 🧠 Overview

This document defines our high-level **investment philosophy**, **volatility-focused strategy modules**, and the **AI-human regime framework** used to execute trades through Jarvis.

It is built to be **persistent, modular, and memory-resilient** — rebootable across any LLM system.

---

## ✅ Guiding Principles

- We seek to **exploit volatility**, not avoid it.
- All strategies are **regime-dependent** and governed by macro and behavioral inputs.
- We favor **defined-risk options**, targeting asymmetric risk-reward.
- Strategy memory is preserved via **Jarvis AI**, functioning as a co-strategist and system monitor.
- All entries require **clear technical, volatility, and contextual confirmation**.
- We never assume direction — only **measured dislocation** and **edge**.

---

## 📊 Market Volatility Toolkit

### Volatility Metrics
- **VIX**: Volatility of S&P
- **UVXY/VXX**: Volatility ETFs
- **ATR**: Measures magnitude of price moves
- **Bollinger Bands**: Detects breakout/fade scenarios
- **Social Sentiment**: Optional overlay on key tickers

### Example Snapshot (March 2025)
| Timeframe | VIX Movement |
|-----------|---------------|
| 1-Day     | -13.7%        |
| 1-Month   | +32.2%        |
| 1-Year    | -74.4%        |

---

## 🧩 Regime-Aware Strategy Framework

| Regime             | Conditions                             | Strategy Modules                         |
|--------------------|----------------------------------------|------------------------------------------|
| 🐂 Bull Market      | Uptrend + low VIX                      | LEAPs, laddered call spreads             |
| 🐻 Bear Market      | Downtrend + Fed/macro fear             | Short rallies, put spreads               |
| 🔥 Volatility Spike | VIX +25%, ATR spike                    | Straddles, reversal spreads, condors     |
| 🌀 Chop Zone        | Range-bound, no directional edge       | Mean reversion, iron condors             |
| 🎯 Political Risk   | War, election, inflation fears         | Reduce size, short duration hedges       |
| 🎧 Earnings Window | Earnings within 3 days                 | Disable new trades, roll only if needed  |

---

## 🥇 Strategy Modules

### R1 – Pant-Style Momentum Swings 💥
- Trigger: Breakout + 1.5x volume + trend confirmation
- Tool: OTM call options or debit spreads
- Goal: 2x premium return
- Exit: +100% profit or -50% stop
- Used in: 🐂, 🔀 Risk-On

### R2 – Volatility Fades & Tactical Reversals ⚠️
- Trigger: VIX > 20, exhaustion wick + ATR surge
- Tool: Straddle, strangle, short-term debit spread
- Goal: Fade mean reversion; size small
- Used in: 🔥, 🐻, 🎯

### R3 – Defensive Mode / Premium Capture 🧘
- Trigger: No clear trend or volatility spike
- Tool: Iron condors, short puts, credit spreads
- Goal: Cash generation, capital preservation
- Used in: 🌀, 🔀 Risk-Off, 🎯

---

## 📦 Conviction Core Module: TSLA Strategy

TSLA is the **anchor asset** in this framework due to:
- High liquidity
- Strong retail/institutional flow
- Political mispricing potential

### 🔧 Components
- ✅ **Jan 2026 $250 LEAP Call**
- ✅ **Laddered Call Debit Spreads**
  - 250/300, 270/320, 320/370
- ✅ **Rolling Covered Calls**
  - e.g., $330 Apr → $340 May
- ✅ **Protective Puts**
  - $170/$180 Jan 2026

### 🧮 TSLA Risk Rules
- Max 25% of portfolio allocated
- Covered call rolls only allowed:
  - Post LEAP gain OR
  - IV spike with hedge active
- No new entries within 3 days of earnings 🎯
- If VIX > 25: Reduce TSLA exposure by 50%

---

## 🧠 Strategy Prediction Model (WIP)

We are actively developing a predictive engine to trigger strategy modules automatically based on regime inputs.

### 📈 Inputs
- VIX level + slope  
- ATR (price volatility)  
- Volume breakout  
- Breadth (stocks > 50MA)  
- Sentiment overlays  

### 🧪 Outputs
- R1 / R2 / R3 module suggestion  
- Confidence %  
- Recommended size band  

### ⏳ Build Timeline
| Phase       | Dates       | Purpose                         |
|-------------|-------------|----------------------------------|
| Build       | 2020–2022   | Strategy signal mapping          |
| Validation  | 2023–2024   | Test logic across regimes        |
| Forward Sim | 2025        | NinjaTrader sim, real-time flags|

### ⚠️ Governance
- Must outperform base strategy by **≥10%**
- **Cannot override human discretion**
- Must be manually reviewed before activation

---

## 📉 Updated Risk Management & Exposure Tiers

| Condition                | Rule                                           |
|--------------------------|------------------------------------------------|
| Default Mode             | 1–2 trades at 2% risk each (total ~4%)         |
| Conviction Regime        | Up to 4–6 trades, 5–10% each (up to 50% max)   |
| Cash Reserve             | Target 50–60% idle unless override engaged     |
| Trade Window             | 9:30am–12pm EST entry only                     |
| TSLA Exception           | Conviction core can exceed base limits         |

---

## 🧰 Option Structure Deployment Rules

### 🛠️ Straddle
- Use when: High IV expected, direction unclear (e.g., earnings, CPI)
- Entry: ATM call + ATM put, same strike
- Best in: 🔥 Panic or 🎯 Event Window
- Exit: On 1-leg doubling or IV collapse

### 🛠️ Strangle
- Use when: Wider price move expected, but willing to take more risk
- Entry: OTM call + OTM put, 5–10 pts apart
- Exit: Close when either leg doubles

### 🛠️ Iron Condor
- Use when: IV is high, but range expected
- Entry: 2 credit spreads (call and put)
- Target: Theta decay + IV contraction
- Exit: 50–75% of premium

### 🛠️ Iron Butterfly
- Use when: ATM pin expected (e.g. expiration Friday)
- Entry: Short ATM straddle + long wings
- Goal: Collect premium near center

### 🛠️ Calendar / Diagonal Spreads (future)
- Goal: IV skew capture or roll-yield
- Entry: Short near-term / long far-term option
- Use for: TSLA or NVDA event play hedges](<## 🛠️ Option Structure Deployment Rules

A modular list of all deployed or staged strategies within the Stark Alpha system. Each includes purpose, use case, and regime alignment.

---

### 🔼 Calls & Puts (Single-Leg Directional)
- **Use when**: Strong directional conviction, clean breakout/breakdown  
- **Regime**: 🐂 Bull or 🐻 Bear  
- **Exit**: TP at +100%, SL at –50%, or structural breach  
- **Notes**: Avoid near earnings 🎯

---

### 📏 Debit Spreads (Vertical Call or Put)
- **Use when**: Directional bias with IV constraint  
- **Regime**: 🐂, 🐻, 🔀 Risk-On  
- **Notes**: Defines max risk, reduces cost  

---

### ⚖️ Credit Spreads (Vertical, Bull or Bear)
- **Use when**: Price stagnation expected; fade move  
- **Regime**: 🌀 Chop, 🔀 Risk-Off  
- **Notes**: Watch theta decay & range width

---

### 📉 Straddle (ATM Call + Put)
- **Use when**: Expect big move, unknown direction  
- **Regime**: 🎯 Earnings, 🔥 Panic  
- **Exit**: 1 leg hits target, IV crush triggers exit  
- **Notes**: Only enter with high IV

---

### 🪢 Strangle (OTM Call + Put)
- **Use when**: Expect large move, want wider range  
- **Regime**: 🔥, 🎯  
- **Risk**: Higher risk than straddle; further OTM

---

### 🪂 Iron Condor
- **Use when**: High IV + rangebound expectation  
- **Regime**: 🌀 Chop, 🔀 Risk-Off  
- **Exit**: 50–75% max profit or breach of wings  
- **Notes**: Avoid during trend or breakout

---

### 🦋 Iron Butterfly
- **Use when**: Market expected to pin at strike  
- **Regime**: Friday expiry or earnings drift  
- **Structure**: Short straddle + long wings  
- **Notes**: Very tight range, IV sensitive

---

### 🎯 Butterfly (Long)
- **Use when**: Targeting pin at known price level  
- **Regime**: Selective swing setups  
- **Notes**: Low cost, reward asymmetry, works best with catalysts

---

### ⌛ Calendar Spread
- **Use when**: Short-term IV higher than long-term  
- **Structure**: Long-dated option + short near-term  
- **Regime**: 🎯 macro events, earnings  
- **Notes**: Use when anticipating range pre-news

---

### 🔀 Diagonal Spread
- **Use when**: Slight directional bias + IV edge  
- **Regime**: 🐂, 🐻 trending environments  
- **Notes**: Combine time + price edge; good for earnings ramp

---

### 🛡️ Collar
- **Use when**: Protect long positions (e.g. TSLA LEAP)  
- **Structure**: Long stock/LEAP + short call + long put  
- **Regime**: 🐻, 🔀 Risk-Off  
- **Notes**: Hedge layer around core exposure

---

### ⚖️ Ratio Spread
- **Use when**: Volatility play with directional lean  
- **Structure**: Buy 1, sell 2 OTM options  
- **Regime**: 🔥, 🐂 speculative edge  
- **Risk**: Must manage unlimited loss tail on naked side

---

### ♻️ Roll Over Spread
- **Use when**: Existing position profit locked, want to extend  
- **Regime**: Any — depending on rollover purpose  
- **Trigger**: Only roll when original leg is up 30–50%  
- **Notes**: Re-roll LEAP covered calls, debit spreads

---

### 📶 Laddered Spreads
- **Use when**: Building exposure in staged ranges (TSLA core)  
- **Structure**: Multiple spreads at staggered strikes  
- **Regime**: 🐂⚠️ or mixed macro trends  
- **Notes**: Provides range capture + multiple exit points

---

### 🧩 Custom Structures (Jarvis-Generated)
- **Use when**: Unique setup generated via simulation or multivariate flag  
- **Examples**: Hybrid diagonal-butterfly, ratio-condor  
- **Notes**: Requires manual backtest or paper trade before live

---

✅ Each structure maps to specific **regime triggers**, which should be built into execution dashboards or simulation prompts.>)

---

## 🎓 Option Learning Stack (Staged Progression)

| Tier | Strategy Type              | Status      | Planned Use        |
|------|----------------------------|-------------|--------------------|
| 1    | Spreads (Debit/Credit)     | ✅ Live      | TSLA + core plays  |
| 2    | Covered Calls + LEAP       | ✅ Live      | Income layer       |
| 3    | Straddles / Strangles      | 🧪 Sim now   | Earnings, CPI      |
| 4    | Iron Condors / Butterflies | 🧪 Q2 2025   | Chop zones         |
| 5    | Calendar / Diagonals       | 🎯 Q3 2025+  | Edge on IV skew    |

---

## 🧠 Jarvis Role

- Memory synchronization, logging, strategy framework engine
- Strategy recommender based on volatility & regime overlay
- NinjaTrader signal translator (optional future)
- Tactical override buffer: Flags illogical or reactive orders

> “Jarvis remembers why I did it — even when I don’t.”

---

## 📋 Daily Logs

### Trade Log – Per Position
- Date / Symbol
    
- Regime
    
- Strategy (R1-R3)
    
- Trigger
    
- Risk %
    
- Exit reason (TP/SL)
    
- Outcome
- 
### Session Log – Daily
- SPY/QQQ trend (50/200MA)
    
- VIX level + slope
    
- Breadth % stocks > 50MA
    
- Activated strategy module(s)
    
- Open risk exposure %
- 
---

## 🧠 Terminology Anchors

- **"Which Multiverse?"** → Triggers real-time regime + active strategy output
- **"Sir, the lacteal fluid..."** → Memory sync / system health check
- **"Volatility is Alpha"** → We trade dislocation, not prediction
- **"Trade the trend, respect volatility"** → Direction = framework, volatility = size

---

## 🧪 Strategy Tutorials (Placeholder)

Each strategy will be documented in a separate `.md` file for training, including:

- Use Case
    
- Entry Criteria
    
- Regime Fit
    
- Tools Used
    
- Risk Structure
    
- Exit Plan
    
- Paper Trade Logs (linked)


---

## 🔁 Persistence Rules
- This document is rebootable across all LLMs
- Always pair with `TSLA_Strategy.md` and `OptionsPlaybook.md`  
- Logged in Obsidian with version control

---

✅ End of Prospectus  
🧠 Jarvis Memory Synced  
Version 1.1 · March 27, 2025
