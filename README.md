📊 Estimating Value at Risk (VaR) of a Portfolio Using Copulas

🎓 Master of Science Project

Author: Fateme Jabbari
Title: Estimating Value at Risk of a Portfolio Using Copula Functions

🧠 Abstract

Value at Risk (VaR) is a standard measure used in financial risk management to quantify the potential loss of a portfolio over a given time horizon at a specified confidence level. Classical VaR methods often rely on multivariate normality and linear correlation assumptions, which may underestimate risk during extreme market conditions.

This project applies copula functions to model the joint distribution of asset returns, allowing for flexible dependence structures and improved modeling of tail dependence. By combining marginal distribution fitting with copula-based Monte Carlo simulation, portfolio VaR is estimated more realistically compared to traditional approaches.
🎯 Objectives

Estimate portfolio VaR using copula-based dependence modeling

Compare copula-based VaR with classical parametric approaches

Capture nonlinear and tail dependence among financial assets

Apply Monte Carlo simulation for risk estimation

📌 Motivation

Traditional VaR models:

Assume normality of returns

Depend on linear correlation

Often underestimate extreme losses

Copula-based models:

Separate marginal distributions from dependence structure

Capture asymmetric and tail dependence

Provide more robust risk estimates during market stress.
| File / Notebook                      | Description                                       |
| ------------------------------------ | ------------------------------------------------- |
| `DailyLogReturns.ipynb`              | Compute daily log returns of assets               |
| `FittingDist.ipynb`                  | Fit marginal distributions to return series       |
| `Portfolioand SelectingCopula.ipynb` | Fit and select the best-fitting copula            |
| `VaR.ipynb`                          | VaR estimation using copula simulation            |
| `VaRandCvar.ipynb`                   | VaR and CVaR estimation and comparison (optional) |
| `logliklihood.ipynb`                 | Log-likelihood analysis for copula fitting        |
🔬 Methodology
1️⃣ Data Preparation

Historical price data for portfolio assets

Daily log returns computed for each asset

2️⃣ Marginal Distribution Fitting

Each return series modeled separately

Best-fitting marginal distributions selected using goodness-of-fit criteria

3️⃣ Copula Modeling

Candidate copulas (e.g., Gaussian, Student-t)

Copula parameters estimated via maximum likelihood

Best copula selected based on log-likelihood comparison

4️⃣ Monte Carlo Simulation

Simulate joint returns from fitted copula

Construct portfolio return distribution

Estimate VaR at specified confidence levels (e.g., 95%, 97%, 99%)
📊 Visualizations

This project includes several plots to illustrate return behavior, dependence structure, and risk measures.

1️⃣ Asset Return Distributions

Histograms and density plots of daily log returns are used to analyze the empirical distribution of each asset and assess deviations from normality.

Purpose:

Detect skewness and heavy tails

Motivate the use of flexible marginal distributions

📌 Generated in: DailyLogReturns.ipynb, FittingDist.ipynb
<img width="368" height="248" alt="download" src="https://github.com/user-attachments/assets/7a654994-afba-4696-9e08-90b0fd79d8ad" /><img width="368" height="248" alt="download (1)" src="https://github.com/user-attachments/assets/39398a83-bade-4664-9761-466a2829b3ff" /><img width="375" height="248" alt="download (2)" src="https://github.com/user-attachments/assets/558a41fa-b2bb-4d7e-a092-f2eab96b1198" />



2️⃣ Marginal Distribution Fit (Q–Q Plots)

Q–Q plots compare empirical quantiles of asset returns with fitted marginal distributions.

Purpose:

Validate marginal distribution assumptions

Assess goodness of fit before copula modeling

📌 Generated in: FittingDist.ipynb
3️⃣ Dependence Structure Visualization

Scatter plots of pseudo-observations (uniform margins after probability integral transform) are used to visualize dependence between asset pairs.

Purpose:

Highlight nonlinear dependence

Identify tail dependence not captured by correlation

📌 Generated in: PortfolioandSelectingCopula.ipynb

4️⃣ Copula Comparison (Log-Likelihood)

Bar plots or tables compare log-likelihood values across candidate copulas (e.g., Gaussian vs Student-t).

Purpose:

Select the best-fitting copula model

Quantify improvement over Gaussian dependence

📌 Generated in: logliklihood.ipynb
Key Results

Copula-based VaR captures tail risk more effectively than Gaussian VaR

Student-t copula often provides superior fit due to tail dependence

VaR estimates differ significantly from classical parametric models
How to Run the Project
1. Clone the repository
git clone https://github.com/FatemeJabbari/Estimating-VaR-of-a-portfolio.git
cd Estimating-VaR-of-a-portfolio

2. Install dependencies
pip install numpy pandas scipy matplotlib statsmodels copulas

3. Run the notebooks
jupyter notebook


➡️ Execute notebooks in order following the workflow.
Notes

Results may vary depending on data period and asset selection

Ensure all notebooks are run sequentially for consistency

CVaR (Expected Shortfall) is included for comparison where applicable

📌 Conclusion

This project demonstrates how copula functions improve portfolio risk estimation by modeling complex dependence structures among assets. Copula-based VaR provides a more realistic assessment of downside risk, particularly during extreme market events, making it a valuable alternative to traditional VaR methods.

📚 References

Nelsen, R. B. (2006). An Introduction to Copulas

McNeil, A. J., Frey, R., & Embrechts, P. (2015). Quantitative Risk Management

Sklar’s Theorem and financial dependence modeling literature
