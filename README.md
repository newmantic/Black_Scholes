# Black_Scholes

The Black-Scholes model is a mathematical model used to price European-style options, which can only be exercised at expiration. The model provides a formula that gives the theoretical value of an option based on several key factors. The model is one of the most important and widely used in finance due to its simplicity and the fact that it offers a closed-form solution.

Assumptions:
1) Lognormal Distribution: The model assumes that the returns of the underlying asset follow a lognormal distribution, meaning that the price of the asset can never be negative and tends to follow a continuous and smooth path.
2) Constant Volatility: The volatility of the underlying asset's returns is assumed to be constant over the life of the option.
3) Constant Interest Rate: The risk-free interest rate, which is used to discount the future payoff, is assumed to be constant and known.
4) No Dividends: The basic Black-Scholes model assumes that the underlying asset does not pay dividends.
5) Efficient Markets: The model assumes that markets are efficient, meaning that there are no arbitrage opportunities, and that all participants can trade the asset freely without any transaction costs.

Black-Scholes Formula:
The model provides two main formulas: one for pricing European call options and one for pricing European put options.
1) Call Option Pricing:
C = S_{0} × N(d_{1}) − K × e^{−rT} × N(d_{2})

2) Put Option Pricing:
P = K × e^{−rT} ×N(−d_{2}) − S_{0} × N(−d_{1})

Where:
C is the price of the European call option.
P is the price of the European put option.
S_{0} is the current price of the underlying asset.
K is the strike price of the option.
T is the time to maturity (in years).
r is the risk-free interest rate.
σ is the volatility of the underlying asset.
N(⋅) is the cumulative distribution function of the standard normal distribution.

d_{1} and d_{2} are intermediate calculations given by:
d_{1} = \frac{ ln(S_{0}/K) + (r + 0.5×σ^{2} )×T } {σ × \sqrt{T} }
d_{2} = d_{1} - σ × \sqrt{T}
​
𝑁(d_{1}) and 𝑁(d_{2}) are values from the cumulative distribution function of the standard normal distribution. They represent the probability that the asset price will reach certain levels.

For a call option, the price is the difference between the current price of the asset, adjusted for the probability that the option will be in-the-money, and the present value of the strike price, also adjusted for the probability.

For a put option, the price is calculated as the difference between the present value of the strike price and the current price of the asset, both adjusted for the probabilities.

Applications
1) Option Pricing: The Black-Scholes model is primarily used for pricing European-style options on stocks, currencies, and other assets.
2) Risk Management: Financial institutions use the model to hedge portfolios by determining the fair value of options and understanding their risk exposures.
3) Strategic Decision Making: Traders and investors use the model to assess the attractiveness of various option strategies.

   
Limitations
1) Assumptions: The Black-Scholes model relies on assumptions such as constant volatility and interest rates, which may not hold true in real markets.
2) No Dividends: The basic model does not account for dividends, although it can be adjusted to include them.
3) European Options Only: The model is designed for European options, which can only be exercised at expiration, and may not be accurate for American options, which can be exercised at any time.
