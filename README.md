# New Dawn Forex Expert Advisor

This code represents the New Dawn Forex Expert Advisor, developed by the Forex Robot Easy Team. Please note that Forex Robot Easy is not the official developer of this product. We are only providing a sample code that can work as described in this product. To find the official developer of this product, please use MQL5.

For detailed reviews and trading results of this product, please visit: [New Dawn Forex Software Review - Automated Multi-Currency Trading](https://forexroboteasy.com/forex-robot-review/new-dawn-forex-software-review-automated-multi-currency-trading/)

## Description

The New Dawn Forex Expert Advisor is an automated trading system designed to trade multiple currency pairs simultaneously. It utilizes an impulse filter to determine when to place new orders. The Expert Advisor sets up order grids for two currency pairs and continuously monitors the market for trading opportunities. It also includes risk management features such as stop loss and take profit levels, as well as a maximum allowed drawdown parameter.

## Input Parameters

The Expert Advisor includes the following input parameters:

- `LotSize`: Trading lot size.
- `GridDistance`: Distance between grid orders in pips.
- `StopLoss`: Stop loss level in pips.
- `TakeProfit`: Take profit level in pips.
- `MaxDrawdown`: Maximum allowed drawdown in account currency.

## Global Variables

The Expert Advisor defines the following global variables:

- `totalOrders`: Total number of open orders.

## Order Structure

The Expert Advisor uses a custom order structure, `SOrder`, which includes the following properties:

- `price`: Order price.
- `stopLoss`: Stop loss level.
- `takeProfit`: Take profit level.

## Order Grids

The Expert Advisor sets up order grids for two currency pairs, `grid1` and `grid2`, each containing 10 orders. Each order in the grid is assigned a price, stop loss level, and take profit level based on the input parameters.

## Initialization

The Expert Advisor initializes by setting up the order grids for the two currency pairs. It assigns prices, stop loss levels, and take profit levels to each order in the grids. The order grids are then printed for verification.

## Trading Operations

The Expert Advisor executes trading operations in the `OnTick` function. It first checks if the maximum drawdown has been reached. If the drawdown limit is exceeded, it closes all open orders for the specified currency pairs.

If the impulse filter is passed, the Expert Advisor places new orders for each currency pair based on the order grids. It checks if the current price is below the order price and sends a buy order with the specified lot size, stop loss level, and take profit level. The total number of orders is incremented if the order is successfully placed.

## Impulse Filter

The `IsImpulseFilterPassed` function is responsible for checking if the impulse filter is passed. The logic for the impulse filter is not implemented in this code and needs to be added separately.

## Conclusion

The New Dawn Forex Expert Advisor is a multi-currency trading system that uses order grids and an impulse filter to determine trading opportunities. It includes risk management features and can trade multiple currency pairs simultaneously. For more information and trading results, please refer to the official developer of this product using MQL5.
