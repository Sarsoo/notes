---
tags:
  - econ
  - securities
---
# Put
- Option to sell
- Provide short position when exercised
	- Used for hedging
- Increase in value
	- Underlying [asset](Asset.md) falls in price
	- Volatility of the underlying asset price increases
	- Interest rates decline.
- Lose value
	- Underlying asset increases in price
	- Volatility of the underlying asset price decreases
	- Interest rates rise
	- Time to expiration nears.

From <[https://www.investopedia.com/terms/p/putoption.asp](https://www.investopedia.com/terms/p/putoption.asp)>

## Cash-Secured Put
- Selling an OTM put and putting aside the money to cover it
	- Neutral to bullish on the underlying asset
	- Hopes for temp downturn in price
- ***If price goes below strike you will have to buy***
	- Probably wanted to, although price might be dipping further

## Married/Protective Put
- Buy ATM put while holding
	- Bullish on underlying
	- Evac strategy on ditching underlying at fixed price
	- Concerned about short term fluctuations
- Usually expensive premium
- Similar risk to covered call
- "Synthetic call"
## Bear Put
- Long ATM/ITM put + Show a lower OTM put

# Call
- Option to buy
- Kind of like a down-payment
## Covered Call
- Selling a call option while holding the underlying asset
	- Passive income in premiums on asset
- Doesn't expect value to change that much
	- Is expecting to hold on to asset
	- ***If the price rises above strike they'll have to sell***
- Short-term hedge
- *"buy-write transaction"*
- Rolling
	- Maintaining position at same or altered terms
		- Raise strike
			- If the price has gone up
			- Sell up ITM option
			- And set a new ceiling
		- Lower strike
			- Price has gone down
			- Lower ceiling for better premium
		- Extend out maturity
			- To maintain strategy
## Bull Spread
- Long ATM/ITM call + Short a higher OTM call
- Limits losses, caps gains
	- Forfeits gains above strike of short call

# Collar Strategy
- Long asset + Long OTM Protective Put + Short OTM Covered Call
- Cap profits to fund evac strategy
- Hedge downside risks but don't want to sell
# Long Straddle
- Long Put + Long Call at same strike/expiration
- Profitable when price moves a lot in either direction
	- Volatile but unsure in which direction
	- Needs to move a lot to cover premiums
# Long Strangle
- Long Put + Long Call with spread in strikes
- Similar to straddle

# Out of the Money
- No intrinsic value
	- Only extrinsic value 
		- The premium
		- Can still make money without going into the money if it approaches it
			- Premium goes up
	- No point exercising, can get a better price on the market
- Higher than current price for **CALLS**
- Lower than current price for **PUTS**

# Styles
- American
	- Can exercise at any point before expiration
- European
	- Can only exercise at expiration