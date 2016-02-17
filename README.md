#in Black-Scholes-Merton
#Monte Carlo valuation of European call option
from numpy import *
#Parameter Values
S0=100. #initial index level
K=105. #strike price
T=0.1 #time-to-mmaturity
sigma=0.2 #volatility
r=0.05 #riskless short rate
I=100000 #number of simulations
##in Black-Scholes-Merton
#Monte Carlo valuation of European call option
from numpy import *
#Parameter Values
S0=100. #initial index level
K=105. #strike price
T=0.1 #time-to-mmaturity
sigma=0.2 #volatility
r=0.05 #riskless short rate
I=100000 #number of simulations
#Valuation Algorithm
z=random.standard_normal(I) #pseudorandom numbers
ST=S0 * exp((r-0.5 * sigma ** 2) * T+sigma * sqrt(T) * z)
#index values at maturity
hT=maximum(ST-K,0)
c0=exp(-r * T) *np. sum(hT)/I
#Monte Carlo estimator

#Result Output
print "Value of the European Call Option %5.3f"% c0


