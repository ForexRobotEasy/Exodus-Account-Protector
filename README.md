# Exodus Account Protector

[![Forex Robot Easy](https://forexroboteasy.com/wp-content/uploads/2021/05/forexroboteasy-logo.png)](https://forexroboteasy.com/forex-robot-review/exodus-account-protector-shield-your-forex-trades-from-draw-down/)

Exodus Account Protector is a code developed by Forex Robot Easy Team to protect Forex traders' accounts from significant drawdown. This utility works on both live and evaluation accounts, providing an effective risk management tool.

## Chart and Default Settings
- Chart Symbol: EURUSD
- Chart Timeframe: M1
- Max Drawdown Balance: 4% of Account Balance
- Max Drawdown Equity: 4% of Account Balance
- Target Profit Balance: 1% of Account Balance
- Target Profit Equity: 1% of Account Balance
- Reset Hour: 16 (in 24-hour format)

## Account Protection Variables
- accountBalance: Stores the current account balance
- accountEquity: Stores the current account equity
- maxDrawdownBalance: Stores the maximum allowable drawdown based on account balance
- maxDrawdownEquity: Stores the maximum allowable drawdown based on account equity
- targetProfitBalance: Stores the target profit based on account balance
- targetProfitEquity: Stores the target profit based on account equity
- isLiveAccount: Flag indicating whether the account is a live account (true/false)
- isEvaluationAccount: Flag indicating whether the account is an evaluation account (true/false)
- isProprietaryFirmAccount: Flag indicating whether the account is compatible with proprietary firms (true/false)

## Expert Initialization Function
The OnInit() function initializes the expert advisor. It retrieves the current account balance and equity, checks the account type (live or demo), checks for compatibility with proprietary firms, and calculates the maximum drawdown and target profit based on the account balance.

## Expert Tick Function
The OnTick() function is called on each tick. It updates the account balance and equity, calculates the drawdown based on the difference between the account balance/equity and the account profit, and takes appropriate action if the drawdown exceeds the maximum allowable drawdown.

## Custom Function to Reset the Utility
The ResetUtility() function resets the utility parameters and calculations to their default values based on the current account balance.

## Custom Function to Check if it's Time to Reset the Utility
The IsResetTime() function checks if the current hour matches the specified reset hour and returns true if it's time to reset the utility.

## Expert Deinitialization Function
The OnDeinit() function is called when the expert advisor is being unloaded. It performs necessary cleanup tasks, such as closing positions and enabling trading.

## Custom Function to Handle Proprietary Firm Account Requirements
The HandleProprietaryFirmAccount() function implements additional requirements specified by proprietary firms. It handles specific account protection mechanisms based on the proprietary firm's specifications.

## Expert Start Function
The OnStart() function is called at the start of each execution cycle. It checks if it's time to reset the utility and calls the ResetUtility() function if necessary. It also checks if the account is a proprietary firm account and calls the HandleProprietaryFirmAccount() function if true.

---

Please note that ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product. To find the official developer of this product, please use MQL5.

For detailed reviews and trading results of this product, please visit [Exodus Account Protector Review](https://forexroboteasy.com/forex-robot-review/exodus-account-protector-shield-your-forex-trades-from-draw-down/).
