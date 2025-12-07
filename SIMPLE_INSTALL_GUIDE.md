# 🎯 SIMPLE INSTALLATION - ORDER BLOCK ZONES

## ⚡ **USE THIS FILE: `order_blocks_final.pine`**

This is the EXACT indicator you asked for:
- ✅ Rectangular zones (boxes)
- ✅ Drawn on BASE candle only
- ✅ All 3 rules (ERC + FVG + BOS)
- ✅ Auto-delete when touched
- ✅ Simple labels
- ✅ No triangles or markers

---

## 📥 **INSTALL (2 MINUTES)**

### Step 1: Copy Code
1. Open file: `order_blocks_final.pine`
2. Select ALL (Ctrl+A or Cmd+A)
3. Copy (Ctrl+C or Cmd+C)

### Step 2: Add to TradingView
1. Go to TradingView.com
2. Open any chart
3. Click **"Pine Editor"** (bottom)
4. Click **"Open"** → **"New indicator"**
5. Delete default code
6. Paste your code
7. Click **"Save"** → Name: "Order Blocks"
8. Click **"Add to Chart"**

---

## ⚙️ **SETTINGS**

Default settings:
```
Impulse Multiplier: 2.0
Pivot Lookback: 10
ATR Length: 14
Demand Color: Green
Supply Color: Red
```

---

## 📊 **WHAT YOU'LL SEE**

### Green Rectangles:
- Start from RED base candle
- Top = Body high of red candle
- Bottom = Wick low of red candle
- Label: "H4 Order Block" or "H1 Order Block"

### Red Rectangles:
- Start from GREEN base candle  
- Top = Wick high of green candle
- Bottom = Body low of green candle
- Label: "H4 Order Block" or "H1 Order Block"

---

## ⚠️ **IF NO ZONES APPEAR**

### Reason: Requirements are VERY STRICT

All 3 must be true:
1. Body > 2.0 × ATR (very large candle)
2. Fair Value Gap exists (rare pattern)
3. Break of Structure (must break 10-bar high/low)

### Solution: Lower the Multiplier

1. Click ⚙️ next to indicator name
2. Change "Impulse Multiplier" from **2.0** to **1.5**
3. Click OK
4. Wait and scroll back in chart

If still nothing, try **1.3** or even **1.0**

---

## 🎯 **WHAT THIS INDICATOR DOES**

### Detection:
- Finds: Red candle → Big green candle (Demand)
- Finds: Green candle → Big red candle (Supply)
- Validates: All 3 rules pass
- Draws: Rectangle on BASE candle

### Display:
- Green boxes = Buy zones
- Red boxes = Sell zones
- Extends to right indefinitely

### Management:
- If price touches zone → Box deleted immediately
- No old/dead zones shown
- Clean chart

---

## 📋 **NO TRIANGLES, NO MARKERS**

This indicator shows ONLY:
- ✅ Rectangular zones (boxes)
- ✅ Small labels

Nothing else. Simple and clean.

---

## 🚀 **EXPECTED BEHAVIOR**

On a 4H chart with default settings (2.0x):
- You might see **2-5 zones per month**
- This is NORMAL - the rules are very strict
- Lower the multiplier to see more zones

On a 1H chart with 1.5x multiplier:
- You might see **5-10 zones per month**
- More reasonable frequency

---

## ✅ **CHECKLIST**

- [ ] Copied code from `order_blocks_final.pine`
- [ ] Pasted in Pine Editor
- [ ] Saved as "Order Blocks"
- [ ] Added to chart
- [ ] Using 4H or 1H timeframe
- [ ] If no zones: Lower Impulse Multiplier to 1.5

---

**This is EXACTLY what you requested. Simple rectangles following your rules.** 📦
