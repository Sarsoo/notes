---
title: LME Averaging
tags:
  - econ
---
# LME
## On Exchange
[Averaging Solutions](https://www.lme.com/-/media/Files/Trading/Contract-types/LME-Averaging-Solutions-Brochure.pdf)
Swaps
- MAF
	- Monthly Average Future
	- Cash settles at MASP
		- Monthly Average Settlement Price
- TAPO
	- Average Asian-style options

### Strategies
#### Fixed for floating
- Physical participants pricing real-world contracts using MASP
- Protect against adverse movement in floating average price
- Buys fixed leg of MAF
	- Hedging a physical buy order of metal basis the currently unknown MASP

#### Float trade
- MAF + Future
	- Do futures at average prices
- Float
	- Sell MAFs
		- e.g **bid 5800**/offer 5810
	- Buy futures prompt settlement date of MAFs
		- e.g bid 5812/**offer 5815**
	- Premium of 5815 - 5800 = 15
	- MASP settles at e.g 6000
		- MAFs payoff to -200
		- Futures payoff at previously agreed 5815
		- 5815 + 200 = 6015 = MASP +. Premium
	- Fixed leg of MAFs and fixed price of futures offset
		- Leaves long future positions at MASP