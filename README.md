Implied Volatility & Time-Dependent Volatility FittingThis repository contains a Python script that calculates the implied volatility of European options using the Newton-Raphson method based on the Black-Scholes model. It also validates put-call parity and fits a time-dependent volatility curve to market data.
🚀 Key FeaturesNewton-Raphson Solver: Iteratively calculates implied volatility from European option prices across different strike prices ($K$).
Put-Call Consistency Check: Analyzes the relationship between call and put options to verify the absence of arbitrage opportunities.
Volatility Calibration: Uses scipy.optimize.curve_fit to estimate the parameters for a time-dependent volatility function:$$\sigma(t) = \sigma_0 e^{-at} + b(1-e^{-at})$$
Data Visualization: Uses matplotlib to plot implied volatility curves and the fitted functions against time.

🛠️ PrerequisitesTo run this code, ensure you have the following Python libraries installed:Bashpip install numpy scipy matplotlib

📂 Code OverviewThe script is divided into two main parts:
Implied Volatility Function (impvol): Computes the implied volatility using Black-Scholes derivatives ($C_K$ and $\kappa$).
Volatility Curve Fitting: Optimizes parameters $\sigma_0$, $a$, and $b$ to fit the volatility over different time horizons using non-linear least squares.
