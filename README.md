# Estimating-VaR-of-a-portfolio
In this project, which is my Master of Science thesis, I have modeled the dependency between random variables using copula functions. In other words, I model the combined distribution of the return prices of assets in a portfolio using copulas. This joint distribution will then be used to calculate the Value-at-Risk (VaR) of the portfolio. The advantages of this method are that it relies on fewer assumptions than the standard method of VaR computation, which assumes a multivariate normal distribution for the asset price returns. In this method, we will choose a correlation structure (defined by a copula) that best fits the underlying data. The multivariate normal distribution will, in fact, be just one of these copulas that defines a particular correlation structure. Thus, this improves the fit of the correlation structure, and this added detail could avoid over-or-under estimation of the portfolio VaR. With the R software, we will work out the portfolio VaR using the copula that best fits the data, and also compare it to the portfolio VaR figure given that the usual multivariate normal distribution (or normal copula with normal marginals) is assumed.
Data: The data that I have used in my work are daily log returns of 3 main indices for bond, real estate, and stock during 13 years. 
 <img width="1384" height="993" alt="dailylog" src="https://github.com/user-attachments/assets/110c3ce4-d5cf-4655-bdeb-e14e6b308162" />
This figure shows the daily log returns of assets. The picture below picture is closing price of assets.
<img width="887" height="993" alt="closingprice" src="https://github.com/user-attachments/assets/cef6a9fc-b6d5-4ffd-8de3-92fa501d94af" />
After calculating and fitting the best distribution to the daily log returns of indices, and using a hypothesis statistical test, the best distribution fitted to variables.
The following figures illustrates this:  
<img width="368" height="248" alt="download" src="https://github.com/user-attachments/assets/862e4ade-7c34-42e2-8854-983ca6b1b140" />
<img width="368" height="248" alt="download (1)" src="https://github.com/user-attachments/assets/a1a82626-c158-41dd-a78c-d6553a4d552b" />
<img width="375" height="248" alt="download (2)" src="https://github.com/user-attachments/assets/0d852dba-f2e9-43ed-9764-294ab191360b" />
After using Monte Carlo simulation and using the log likelihood function, I found the best copula is the T-Copula.
<img width="1037" height="773" alt="download (5)" src="https://github.com/user-attachments/assets/44a23cea-204c-4f43-af05-cad49acd30b9" />
Moreover, I have used Q-Q plot for the returns of the portfolio and the returns of the T-copula and Gaussian samples. <img width="909" height="876" alt="download (4)" src="https://github.com/user-attachments/assets/f3071f4a-ce61-40f9-ac56-58b6383af90f" />
Finally, I estimated the Value at Risk of a portfolio using Monte Carlo Simulation in 97% confidence level.
