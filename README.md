# Institutional Order Blocks - Final Working Version

**MAIN FILE: `INSTITUTIONAL_OB_FINAL.pine`**

---

## Quick Start

1. Copy `INSTITUTIONAL_OB_FINAL.pine` to TradingView Pine Editor
2. Read `HOW_TO_USE.md` for complete instructions
3. Adjust settings based on your needs

---

## What This Indicator Does

Detects institutional order blocks using 4 strict rules:

1. **Base Pattern**: Red→Green (Demand) or Green→Red (Supply)
2. **Explosive Impulse**: Body > ATR × Multiplier
3. **Fair Value Gap**: Optional imbalance detection
4. **Break of Structure**: Price breaks recent high/low

Only shows **FRESH, UNTOUCHED** zones. Zones are deleted when price touches them.

---

## Features

✅ All 4 institutional rules implemented  
✅ Zones drawn on BASE candle (not impulse candle)  
✅ Automatic deletion of touched zones  
✅ Adjustable strictness (Body Multiplier)  
✅ Optional FVG rule (turn ON/OFF)  
✅ Clean visual display with status table  
✅ Built-in alerts for new zones  

---

## Default Settings

- Body Multiplier: **1.5** (balanced)
- FVG Required: **OFF** (3 rules active)
- BOS Lookback: **10** bars
- Max Zones: **20**

**These settings will show zones on EUR/USD 4H/1H timeframes.**

---

## Files in This Workspace

- **`INSTITUTIONAL_OB_FINAL.pine`** ← Main indicator (USE THIS)
- **`HOW_TO_USE.md`** ← Complete installation & usage guide
- Other files: Previous versions and tests

---

## Support

If you see too few zones: Lower Body Multiplier to 1.2  
If you see too many zones: Raise Body Multiplier to 2.0, turn FVG ON

---

**Created for institutional-grade order block detection on TradingView.**
