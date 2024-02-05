# Trailing on Last Top Bottom MT4

This code is a custom indicator for MetaTrader 4 (MT4) that implements a trailing stop loss strategy based on the last recorded top and bottom prices. It is designed to be used in forex trading. 

## Input Parameters
- TrailingDistance: The trailing distance in pips. This parameter determines how far behind the current price the stop loss level should be set.

## Global Variables
- lastTop: The last recorded top price.
- lastBottom: The last recorded bottom price.
- ticket: The ticket number of the open trade.

## Indicator Initialization
The `OnInit()` function is the initialization function for the indicator. It returns `INIT_SUCCEEDED` to indicate successful initialization.

## Indicator Iteration
The `OnTick()` function is called on each tick of the chart. It checks if the last recorded top and bottom prices have been set. If not, it sets them to the current bid price. 

If there is an open trade, it gets the current ask price and calculates the trailing stop loss level. It then modifies the stop loss level of the open trade using `OrderModify()`.

## Open Trade
The `OpenTrade()` function is used to open a trade. It calculates the stop loss and take profit levels based on the entry price and trailing distance. It then opens a buy trade using `OrderSend()`.

## Close Trade
The `CloseTrade()` function is used to close the open trade. It closes the trade using `OrderClose()` and resets the ticket number.

## Indicator Deinitialization
The `OnDeinit()` function is called when the indicator is removed from the chart. If there is an open trade, it calls the `CloseTrade()` function to close the trade.

Please note that Forex Robot Easy is not the official developer of this product. We are only providing a sample code that can work as described in this product. If you are looking for the official developer of this product, please use MQL5.

For detailed reviews and trading results of this product, please visit the [Forex Robot Easy website](https://forexroboteasy.com/forex-robot-review/trailing-on-last-top-bottom-mt4-unbiased-review-and-results/).
