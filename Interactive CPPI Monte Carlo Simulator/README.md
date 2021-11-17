
# Interactive CPPI Monte Carlo Simulator

Interactive IPython Jupyter widget application to simulate PSP portfolios behavior under CPPI strategy. 

CPPI is an insurance investment strategy that is used for risk management in large cap portfolios. Below is simple explaination of how CPPI works

![CPPI](https://github.com/AbdullahBahi/My-Portfolio/blob/master/Interactive%20CPPI%20Monte%20Carlo%20Simulator/0.png?raw=true)

Given an investment portfolio with an expected average annual return **μ** and estimated annual volatility of **σ**, this simulator allows you to simulate the performance of this portfolio under CPPI strategy.
as showm below, you can modify CPPI Arguments and see the effect immediately on the output graph. The output includes the following statistics:
- **Mean**: Expected return of the portfolio averaged over **n_scenarios**.
- **Median**: the median value of Expected returns.
- **Violation**: Number of violations of the **floor** out of **n_scenarios**.
- **E(shortfall)**: Percentage of number of vilations to **n_scenarios**

![Simulator](https://github.com/AbdullahBahi/My-Portfolio/blob/master/Interactive%20CPPI%20Monte%20Carlo%20Simulator/1.png?raw=true)