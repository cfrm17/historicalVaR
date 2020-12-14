# Historical Value At Risk Introduction

Value at Risk (VaR) is the regulatory measurement for assessing market risk. It reports the maximum likely loss on a portfolio for a given probability defined as x% confidence level over N days. VaR is vital in market risk management and control. Also regulatory and economic capital computation is based on VaR results. Although VaR measure is objective and intuitive, it doesn’t capture tail risk. There are three commonly used methodologies to calculate VaR – parametric, historical simulation and Monte Carlo simulation. This presentation focuses on historical VaR.  

Keywords:
Value at Risk, VaR, historical VaR, market risk, financial market, trading risk, risk analytics, risk implementation

	Historical VaR
	Definition
Value at Risk (VaR) is the regulatory measurement for assessing market risk. It reports the maximum likely loss on a portfolio for a given probability defined as x% confidence level over N days. VaR is vital in market risk management and control. 
 

	VaR Roles
	Risk measurement
	Risk management
	Risk control
	Financial reporting
	Regulatory and economic capital

	VaR Pros & Cons
	Regulatory measurement for market risk
	Objective assessment
	Intuition and clear interpretation
	Consistent, flexible and stable measurement
	Doesn’t measure risk beyond the confidence level: tail risk
	Non sub-additive

	VaR Approaches
	Parametric VaR
	Historical VaR
	Monte Carlo VaR

	Historical Simulation
	Assumption
The past is a good indicator of the near-future
	Pros
Simple
Intuitive
Easy back and stress test
No distribution assumption
No calibration
	Cons
Poor accuracy for higher confidence level and tail risk
Difficult for long horizons
Limited scenario

	Historical VaR Methodology
	Obtain one year historical value time series of all market factors, such as a stock price time series is ■(x ̅_1&⋯&x ̅_251 )
	Assuming today’s value is x_0, generate 250 historical scenarios. The i-th is  x_i=(x ̅_i⁄x ̅_(i-1) -1)x_0
	Compute base PV at today t as P(x_o)
	Compute 250 scenario PVs:  P(x_i)
	Compute 250 scenario P&L:	P(x_i )-P(x_0)
	Sort 250 scenario P&L. The VaR is the average between 2nd and 3rd lowest (negative) numbers
	VaR Scaling
	Normally firms compute 1-day 99% VaR
	Regulators require 10-day 99% VaR
	Under IID assumption, 10-day VaR = √10*〖VaR〗_(1-day)

	VaR Backtest
	The only way to verify a VaR system is backtest
	At a certain day, compute hypothetic P&L (valuation date and portfolio unchanged)
If (hypothetic P&L > VaR)  breach
	For one year
If number of breaches is 0-4, the VaR system is in Green zone
If number of breaches is 5-9, the VaR system is in Yellow zone
If number of breaches is 10 or more, the VaR system is in Red zone


You can find more details at
https://finpricing.com/lib/FiBond.html

