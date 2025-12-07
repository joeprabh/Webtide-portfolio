# INSTALL THIS: order_blocks_working.pine

## COPY THIS CODE TO TRADINGVIEW

1. Open `order_blocks_working.pine`
2. Copy ALL
3. TradingView → Pine Editor → New Indicator
4. Paste → Save → Add to Chart

## SETTINGS TO SEE ZONES

After installing, click ⚙️ and set:

**Impulse Multiplier: 1.5** (or try 1.3 if nothing shows)

## WHAT IT DOES

- Finds: Red → Big Green (Demand)
- Finds: Green → Big Red (Supply)
- Draws: Green rectangles (buy)
- Draws: Red rectangles (sell)
- Deletes: When price touches

## IF YOU SEE NOTHING

The rules require ALL 3:
1. Body > 1.5x ATR
2. Fair Value Gap exists
3. Break of Structure

These are RARE when combined.

**Try this:**
- Lower Impulse to 1.3
- Scroll back on chart (load more data)
- Wait - zones are rare with strict rules

## THE REALITY

With your exact rules (ERC + FVG + BOS), you will see:
- 4H chart: Maybe 2-5 zones per MONTH
- 1H chart: Maybe 5-10 zones per MONTH

This is NORMAL. The rules are very strict.
