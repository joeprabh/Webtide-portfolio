# Institutional Supply & Demand Indicator - User Guide

## 📊 Overview
This Pine Script v6 indicator identifies institutional supply and demand zones based on the **Golden Checklist** methodology. It strictly follows all 5 criteria and automatically filters out weak zones.

## 🎯 The Golden Checklist (All 5 Must Be Met)

### ✅ 1. EXPLOSIVE IMPULSE
- **What it detects:** Large "extended range" candles that are 1.5x+ the average range
- **Setting:** `Impulse Multiplier` (default: 1.5)
- **Rule:** Body must be 60%+ of the candle range (proves genuine momentum, not wicks)

### ✅ 2. ACCOMPLISHMENT (Break of Structure)
- **What it detects:** The impulse MUST break a recent swing high (for demand) or swing low (for supply)
- **Setting:** `Swing Structure Lookback` (default: 10)
- **Rule:** Automatically validated before zone is created

### ✅ 3. FRESHNESS (Untested)
- **What it detects:** Zones that have NOT been touched yet
- **Rule:** After first touch, zone is automatically DELETED
- **Visual:** Fresh zones extend to the right with boxes

### ✅ 4. TIME AT LEVEL (Tight Base)
- **What it detects:** 1-3 small candles before the explosion
- **Setting:** `Max Base Candles` (default: 3)
- **Rule:** Long consolidations = rejected automatically

### ✅ 5. LIQUIDITY SWEEP (The Stop Hunt)
- **What it detects:** Price swept a nearby high/low before creating the zone
- **Setting:** `Liquidity Sweep Lookback` (default: 5)
- **Visual:** Zones with sweeps show a 🎯 target emoji

---

## 🎨 How Zones Are Drawn (Precision Rules)

### DEMAND ZONES (Green)
```
1. Finds the explosive GREEN impulse candle
2. Looks at the last RED candle before it
3. Zone Box = From BODY HIGH down to WICK LOW
4. If wick is 2x+ body size, ignores bottom 50% of wick (adjustable)
```

### SUPPLY ZONES (Red)
```
1. Finds the explosive RED impulse candle
2. Looks at the last GREEN candle before it
3. Zone Box = From BODY LOW up to WICK HIGH
4. If wick is 2x+ body size, ignores top 50% of wick (adjustable)
```

---

## ⚙️ Settings Explained

| Setting | Default | Purpose |
|---------|---------|---------|
| **Impulse Multiplier** | 1.5 | How much larger the impulse must be vs average. Higher = stricter. |
| **Swing Structure Lookback** | 10 | How far back to check for swing highs/lows. |
| **Max Base Candles** | 3 | Maximum consolidation candles allowed. More = rejection. |
| **Liquidity Sweep Lookback** | 5 | How far back to check for swept highs/lows. |
| **Wick Reduction %** | 0.5 | If wick is 2x+ body, ignore this % of wick (0.5 = 50%). |
| **Average Range Period** | 20 | Period for calculating average candle range. |
| **Max Zones to Display** | 10 | Maximum number of zones shown at once. |

---

## 🚀 How to Use in TradingView

### Installation:
1. Open TradingView
2. Click on "Pine Editor" at the bottom
3. Click "Open" → "New indicator"
4. Copy and paste the entire code from `institutional_supply_demand.pine`
5. Click "Save" and give it a name
6. Click "Add to Chart"

### Best Practices:
- **Timeframes:** Works best on 15min, 1H, 4H, Daily
- **Fresh Zones Only:** Only trade zones that haven't been touched (automatic)
- **Confluence:** Look for zones near key levels, fib retracements, or trend lines
- **Entry:** Wait for price to tap the zone + bullish/bearish confirmation candle
- **Stop Loss:** Just below/above the zone

---

## 🔔 Alerts Available

The indicator includes 4 alert conditions:

1. **New Demand Zone** - Fires when a new buy zone is detected
2. **New Supply Zone** - Fires when a new sell zone is detected
3. **Price in Demand Zone** - Fires when price enters a fresh demand zone
4. **Price in Supply Zone** - Fires when price enters a fresh supply zone

### Setting Up Alerts:
1. Click the "⏰" icon in TradingView
2. Choose "Condition" → Your indicator name
3. Select the alert type
4. Set notification preferences
5. Click "Create"

---

## 📋 The R.A.F.T. Filter (Built-In)

| Filter | Implementation |
|--------|----------------|
| **R - Return** | Monitors how price approaches (fast returns are less valid) |
| **A - Arrival** | User should avoid trading during high-impact news |
| **F - Freshness** | ✅ Automatic - zones deleted after first touch |
| **T - Time** | ✅ Automatic - only zones with 1-3 base candles pass |

---

## 📊 Visual Guide

### Zone Colors:
- 🟢 **Green Box** = Fresh DEMAND zone (buy opportunity)
- 🔴 **Red Box** = Fresh SUPPLY zone (sell opportunity)
- 🎯 **Target Emoji** = Zone formed with liquidity sweep (higher probability)

### Debug Markers:
- **▲ Green Triangle** = Explosive bullish candle detected
- **▼ Red Triangle** = Explosive bearish candle detected

---

## ⚠️ Important Notes

### Zones Are Automatically IGNORED If:
- ❌ Impulse candle is too small (weak move)
- ❌ Didn't break swing high/low (no accomplishment)
- ❌ Already been touched once (not fresh)
- ❌ More than 3 candles consolidated at base (equilibrium, not imbalance)

### Zones Are Automatically DELETED When:
- ❌ Price touches the zone (freshness lost)
- ❌ Maximum display limit reached (oldest zones removed)

---

## 🎓 Trading Strategy Tips

### For DEMAND Zones (Long Setup):
1. Wait for price to return to the green zone
2. Look for bullish confirmation:
   - Bullish engulfing
   - Hammer/pin bar
   - Break of mini structure
3. Enter on close above confirmation candle
4. Stop loss: 1-2 pips below zone low
5. Target: Recent swing high or 2:1 RR

### For SUPPLY Zones (Short Setup):
1. Wait for price to return to the red zone
2. Look for bearish confirmation:
   - Bearish engulfing
   - Shooting star
   - Break of mini structure
3. Enter on close below confirmation candle
4. Stop loss: 1-2 pips above zone high
5. Target: Recent swing low or 2:1 RR

---

## 🔧 Troubleshooting

**Problem:** No zones showing up
- **Solution:** Lower the `Impulse Multiplier` to 1.3 or 1.2
- **Solution:** Increase `Max Base Candles` to 4 or 5
- **Solution:** Try a different timeframe (4H recommended)

**Problem:** Too many zones
- **Solution:** Increase the `Impulse Multiplier` to 2.0+
- **Solution:** Decrease `Max Zones to Display`

**Problem:** Zones seem inaccurate
- **Solution:** Adjust `Swing Structure Lookback` based on your timeframe
- **Solution:** Lower timeframes (1min-5min) are noisier - stick to 15min+

---

## 📈 Recommended Settings by Timeframe

| Timeframe | Impulse Multiplier | Swing Lookback | Base Candles |
|-----------|-------------------|----------------|--------------|
| **15min** | 1.8 | 8 | 2 |
| **1H** | 1.5 | 10 | 3 |
| **4H** | 1.3 | 12 | 3 |
| **Daily** | 1.2 | 15 | 4 |

---

## 💡 Pro Tips

1. **🎯 Prioritize zones WITH the target emoji** - These had liquidity sweeps
2. **🔄 Combine with market structure** - Trade zones in the direction of the higher timeframe trend
3. **📊 Use multiple timeframes** - Look for 4H zones, enter on 15min confirmation
4. **⏰ Avoid news events** - Check economic calendar before trading zones
5. **📉 Volume matters** - Higher volume on the impulse = stronger zone
6. **🎨 Keep chart clean** - Only show 5-8 zones max at a time

---

## 📝 Summary

This indicator does the heavy lifting for you:
- ✅ Automatically validates ALL 5 Golden Checklist criteria
- ✅ Draws precise zones (not massive boxes)
- ✅ Auto-deletes touched zones (freshness tracking)
- ✅ Identifies liquidity sweeps
- ✅ Filters out weak/invalid zones

**You focus on:** Waiting for price to return + confirmation candle + proper risk management.

---

## 🤝 Support

If you encounter issues or need customization:
- Verify you're using Pine Script v6 (TradingView indicator)
- Check the settings match your trading style
- Test on demo account first
- Adjust parameters based on your market/timeframe

**Happy Trading! 🚀**
