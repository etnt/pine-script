# pine-script

A collection of Pine Scripts that I've written and are using
in my Tradingview setup.

To use them, open up the Tradingview Pine Editor, open a new
indicator and replace the content with the new code; save and
add the indicator to the chart.

## Key Moving Averages

A number of Key Moving Averages are plotted;
depending on the timeframe used, different values are used.

The following (default) values are used:

  * Daily: MA10, EMA21, MA50, MA200
  * Weekly: MA10, MA40
  * Intraday: Daily MA5  (idea curtesy: Brian Shannon) and EMA65

The MA200 will be presented in white when On-Balance-Volume is positive,
else it is presented in blue.

It is also possibe to display a Bollinger Band.

[Key Moving Averages](images/key-moving-averages.png)


## Nice Volume

This Volume panel is inspired by TradingLions ditto.

Four different colors are used for the Volume columns:

  * Up/Down down columns.
  * Pocket Pivot columns.
  * Lowest of 10 periods.

A moving average is plotted where the color is changed
depending on the trend of the Acc/Dist volume indicator.

A table is displayed containing some Volume indicators:

  * Up/Down volume ratio, where a value above 1.5 is shown
    in green, indicating that more than 50% och the volume
    is positive; where a value below 0.5 is shown in red.
  * On-Balance Volume trend; the percentage OBV is above/below
    a moving average is displayed; positive/negative in green/red.
  * The trend (Positive/Negative/Weak) of the Acc/Dist indicator
    is displayed in either green/red.

[Nice Volume](images/nice-volume.png)


## Position Sizes

When trading, position sizing and risk calculation are the keys to become
successful.

We need to keep the losses small and adjust the position size according to what
risk we are prepared to take for the planned Entry.

Based on the Account Size and the max percentage we want to risk for any trade,
we calculate, for a number of fixed max Loss percentages:

The Position size, both in percent and in the selected currency.

  * Number of shares to buy.
  * Where to put the Stop Loss.
  * Where a 1RTP (1 Risk amount Take Profit) level could be put .

We also calculate the numbers based on the ATR times a multiple.

The values are presented in a table format and will hopefully aid in selecting
a suitable Stop Loss (based on the chart sutuation) and hence the proper
Position Size.

We also allow for expressing the Account size in currencies other than USD.

Example:

    Account Size in USD and trading US stocks: select USD
    Account Size in SEK but trading US stocks: select USDSEK

[Position Sizes](images/position-sizes.png)


## Inside Bars

Indicate bars where their high and low are inside a previous bar.

Inside bars show a period of consolidation in a market.
They often form following a strong move in a market,
as it ???pauses??? to consolidate before making its next move.

However, they can also form at market turning points and
act as reversal signals from key support or resistance levels."

[Inside Bars](images/inside-bars.png)

