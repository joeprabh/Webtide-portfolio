# 🚀 Institutional Supply & Demand - Quick Reference Card

## ✅ THE GOLDEN CHECKLIST (Must Meet ALL 5)

| # | Criteria | What to Look For | Script Validates? |
|---|----------|------------------|-------------------|
| 1️⃣ | **EXPLOSIVE IMPULSE** | Large candle (1.5x+ avg range) | ✅ Auto |
| 2️⃣ | **ACCOMPLISHMENT** | Broke swing high/low | ✅ Auto |
| 3️⃣ | **FRESHNESS** | Zone NOT touched yet | ✅ Auto |
| 4️⃣ | **TIME AT LEVEL** | 1-3 candles at base | ✅ Auto |
| 5️⃣ | **LIQUIDITY SWEEP** | Recent high/low swept | ✅ Auto (🎯 shows) |

---

## 🎨 ZONE DRAWING PRECISION

### DEMAND (Buy Zone):
```
└── Last RED candle before impulse
    ├── Top: Body High
    └── Bottom: Wick Low (reduced if wick > 2x body)
```

### SUPPLY (Sell Zone):
```
┌── Last GREEN candle before impulse
├── Top: Wick High (reduced if wick > 2x body)
└── Bottom: Body Low
```

---

## 🎯 TRADING THE ZONES

### Entry Checklist:
- [ ] Zone is FRESH (not touched)
- [ ] Price returned SLOWLY (compression)
- [ ] Confirmation candle formed
- [ ] No major news in next 2 hours
- [ ] Risk:Reward minimum 1:2

### LONG Setup (Demand):
1. Price taps green zone
2. Bullish confirmation (engulfing/hammer)
3. Enter above confirmation close
4. SL below zone
5. TP at swing high

### SHORT Setup (Supply):
1. Price taps red zone
2. Bearish confirmation (engulfing/star)
3. Enter below confirmation close
4. SL above zone
5. TP at swing low

---

## ⚙️ RECOMMENDED SETTINGS

### Conservative (Less zones, higher quality):
- Impulse Multiplier: **2.0**
- Swing Lookback: **12**
- Max Base Candles: **2**

### Balanced (Default):
- Impulse Multiplier: **1.5**
- Swing Lookback: **10**
- Max Base Candles: **3**

### Aggressive (More zones, more trades):
- Impulse Multiplier: **1.2**
- Swing Lookback: **8**
- Max Base Candles: **4**

---

## 🔔 ALERT SETUP

| Alert Type | When to Use | Action |
|-----------|-------------|--------|
| New Demand Zone | Auto-detect buy zones | Mark on chart, wait for return |
| New Supply Zone | Auto-detect sell zones | Mark on chart, wait for return |
| Price in Demand | Potential long entry | Check for confirmation |
| Price in Supply | Potential short entry | Check for confirmation |

---

## ⚠️ AVOID TRADING IF:

- ❌ Zone already touched (auto-deleted)
- ❌ Impulse was weak/slow
- ❌ No structure break
- ❌ High-impact news event
- ❌ Price crashed back to zone (fast return = weak)
- ❌ Inside major consolidation range

---

## 💎 PRO TIPS

| Tip | Why It Matters |
|-----|---------------|
| 🎯 **Trade zones WITH emoji** | Had liquidity sweep = stronger |
| 📊 **Multi-timeframe** | 4H zones + 15min entry = precision |
| 📈 **Trade with trend** | HTF trend + zone = higher win rate |
| ⏰ **First touch only** | 2nd touch = orders already filled |
| 🎨 **Keep it clean** | Max 5-8 zones visible |
| 📉 **Volume confirmation** | High volume impulse = institutional |

---

## 🔧 QUICK TROUBLESHOOTING

| Problem | Solution |
|---------|----------|
| No zones showing | Lower Impulse Multiplier to 1.2-1.3 |
| Too many zones | Raise Impulse Multiplier to 2.0+ |
| Zones keep disappearing | Normal! They delete after touch (freshness) |
| False signals | Use higher timeframe (4H instead of 15min) |

---

## 📊 BEST TIMEFRAMES

| Timeframe | Use Case | Settings |
|-----------|----------|----------|
| **15min** | Scalping, quick trades | Impulse: 1.8, Lookback: 8 |
| **1H** | Day trading | Impulse: 1.5, Lookback: 10 |
| **4H** | Swing trading (BEST) | Impulse: 1.3, Lookback: 12 |
| **Daily** | Position trading | Impulse: 1.2, Lookback: 15 |

---

## 📝 THE R.A.F.T. FILTER

| Letter | Meaning | Implementation |
|--------|---------|----------------|
| **R** | Return | Price should approach slowly |
| **A** | Arrival | Avoid trading during news |
| **F** | Freshness | ✅ Auto-tracked (zones delete after touch) |
| **T** | Time | ✅ Auto-checked (1-3 base candles only) |

---

## 🎓 REMEMBER

> **"The indicator finds the zones. YOU find the trade."**

- Indicator = Identifies valid institutional zones
- You = Wait for confirmation + manage risk
- Success = Patience + discipline + proper execution

---

## 📞 INSTALLATION (30 seconds)

1. Open TradingView
2. Pine Editor → New Indicator
3. Paste code from `institutional_supply_demand.pine`
4. Save → Add to Chart
5. Done! 🎉

---

## 🏆 GOLDEN RULES

1. **Only trade FRESH zones** (auto-enforced)
2. **Wait for confirmation candle** (your job)
3. **Risk max 1-2% per trade** (your discipline)
4. **Set alerts, don't stare** (efficiency)
5. **Trust the checklist** (it filters 90% of noise)

---

**Print this reference card and keep it by your desk! 📌**
