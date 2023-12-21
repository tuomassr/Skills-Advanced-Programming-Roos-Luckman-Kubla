# Skills-Advanced-Programming-Roos-Luckman-Kubla
Run the master_file.py, this is the main file and to it we call/import the other ones

If there are any problems, you can also checkout the demo video

SHORT DESCRIPTION OF THE PROJECT:
The aim of the project is to get input from the user, assessing their risk tolerance and based on that give out some informative feedback on realistic benchmark expectations on the stock market.
It consists of 3 main parts:
1. Prompt user to answer several questions relating to their risk tolerance and using Mean variance portfolio theory to deduct their average risk taking behaviour.
2. Scrape the web using an API for S&P500 stocks > taking any potential restrictions from the user which is a common approach in investing (especially ESG investing) > computing the efficient frontier based on closed form optimization; obtaining the minimum variance portfolio, market portfolio, and the capital market line. Based on the user’s risk tolerance from STEP 1, calculate the expected market return given based on the CAPM model. Please do note that in the demo code the historic stock data from the web scraping is preloaded and the section of the code that does the web scraping is commented out.
3. Provide information on expectations for long-term portfolio returns based on the specific information from the user and the market data. Here we employed several techniques to provide useful and easily interpretable information for the user (Value at risk, shortfall risk, ...).
Please find the YouTube link containing a screen recording of the entire project being ran:
https://youtu.be/JyMl8N8pxCE?si=E5osVGUxAdxVz7L9
NOTE: The project is based on fundamental Portfolio theory approaches. However, as the focus of the project is on the Programming part, we acknowledge several possible improvements of the finance models, most importantly including but not limited to STEP 2:
• Computation of the efficient frontier: Mean-variance portfolio optimization has a limited use if applied in a naïve way as it is very sensitive to mean returns and correlations, and based on historical data, we obtain several negative returns and negatively correlated securities, which are unlikely in ex-ante expectation. Mean returns and variances should be forward looking. The optimisation approach includes
  
The project is coded in several separate Python files (.py).
→The project has to be run in the master_file.py file, where all separate files are imported. There is an additional description of the project and the required packages which are loaded in the beginning.
   
estimating the variance-covariance matrix, namely for the 500 stocks in the S&P it performs 500*250=125,000 estimations based on historical data, which is sensitive to mistakes. A potential approach would to the use of Black-Litteman approach using reverse engineering to extract expected returns from benchmark portfolio. Another approach would be using factor models to estimate variance-covariance matrix.
• Using the CAPM model in calculation of the capital market line. It is well known that CAPM performs poorly when applied to expected stock returns. A potential solution would be using a more sophisticated multi-factor model which empirically performs better, or even using several models.
IMPORTANTLY: Consequently, our approach vastly overestimates the expected returns and underestimates the involved risk, making the magnitude of overestimation of risk-adjusted returns even higher. Both of these shortcomings stem from the STEP 2 of our project. Therefore, refinement of the calculation of the expected returns in the market and the corresponding risk is the only part needed to make the outputs of the entire project realistically applicable. For illustration purposes, a frequently used assumption in finance of an 8% equity risk premia and volatility of 20% can be replaced into the model.
THIS PROJECT THUS DOES NOT CONSTITUE ANY INVESTMENT ADVICE OR GUARANTEE!
HOWEVER, IT COULD BE USED AS AN AUTOMATIC ONLINE FINANCIAL ADVISOR WITH THE USE OF A FEW THEORY ADJUSTMENTS.
