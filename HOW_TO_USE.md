# INSTITUTIONAL ORDER BLOCKS - HOW TO USE

## FILE TO USE: `INSTITUTIONAL_OB_FINAL.pine`

---

## INSTALLATION

1. Open TradingView
2. Click Pine Editor (bottom of screen)
3. Click "New" → blank script
4. **DELETE EVERYTHING**
5. Open `INSTITUTIONAL_OB_FINAL.pine` from your workspace
6. **COPY ALL THE CODE** (all 185 lines)
7. **PASTE** into Pine Editor
8. Click "Save" (top right)
9. Click "Add to Chart" (top right)

---

## WHAT YOU'LL SEE

- **Green boxes** = DEMAND zones (buy opportunities)
- **Red boxes** = SUPPLY zones (sell opportunities)
- **Labels** = "DEMAND" or "SUPPLY"
- **Table** (top right) = Shows how many fresh zones are active

---

## DEFAULT SETTINGS (Will show zones)

- **Body Multiplier**: 1.5 (balanced)
- **FVG Required**: OFF (only 3 rules active)
- **BOS Lookback**: 10 bars
- **Max Zones**: 20

---

## IF YOU SEE NO ZONES OR TOO FEW

Click the indicator name on chart → Click settings icon → Adjust:

1. **Lower "Body Multiplier"** to 1.2 or 1.1
2. Keep **"Require FVG"** = OFF

---

## IF YOU SEE TOO MANY ZONES

Click the indicator name on chart → Click settings icon → Adjust:

1. **Raise "Body Multiplier"** to 1.8 or 2.0
2. Turn **"Require FVG"** = ON (adds 4th rule)

---

## THE 4 RULES (How zones are detected)

1. **Base Pattern**: Red candle followed by Green (demand) or Green followed by Red (supply)
2. **Explosive Impulse**: The impulse candle body must be > ATR × Multiplier
3. **Fair Value Gap**: Optional - creates a price gap (turn OFF for more zones)
4. **Break of Structure**: Price breaks highest high (demand) or lowest low (supply) over lookback period

---

## ZONE DRAWING (Where boxes appear)

- **Demand Zone**: Drawn on the RED base candle
  - Top = Body high of red candle (open price)
  - Bottom = Wick low of red candle

- **Supply Zone**: Drawn on the GREEN base candle
  - Top = Wick high of green candle
  - Bottom = Body low of green candle (open price)

---

## ZONE DELETION (Keeps chart clean)

- Zones are deleted **immediately** when price touches them
- Only **FRESH, UNTOUCHED** zones are shown
- Maximum zones limited to prevent clutter

---

## BEST PRACTICES

- Use on **4H or 1H timeframe** for EUR/USD
- Scroll back **2-3 months** to see historical zones
- With strict settings (multiplier 2.0, FVG ON), expect 5-15 zones
- With relaxed settings (multiplier 1.3, FVG OFF), expect 20-40 zones

---

## TROUBLESHOOTING

**Problem**: No zones appear
- **Solution**: Lower Body Multiplier to 1.2, turn FVG OFF

**Problem**: Too many zones
- **Solution**: Raise Body Multiplier to 2.0, turn FVG ON

**Problem**: Compilation error
- **Solution**: Make sure you copied ALL the code (lines 1-185)

**Problem**: Zones not disappearing when touched
- **Solution**: The code automatically deletes touched zones. This is working as designed.

---

## FILE NAME: `INSTITUTIONAL_OB_FINAL.pine`

**This is your complete, working indicator with all 4 rules.**
