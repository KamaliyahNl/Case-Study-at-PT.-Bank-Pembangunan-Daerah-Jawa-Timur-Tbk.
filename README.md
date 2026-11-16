# Case-Study-at-PT.-Bank-Pembangunan-Daerah-Jawa-Timur-Tbk.

This project tests what moves the profitability of Bank Jatim, the regional development bank of East Java. Using 32 quarters of financial data from the first quarter of 2016 to the fourth quarter of 2023, it runs a multiple linear regression of Return on Assets (ROA) on four bank ratios: non-performing loans (NPL), operating costs to operating income (BOPO), loan to deposit ratio (LDR) and net interest margin (NIM). After the classical assumption tests are passed, the model explains 98.69% of the variation in ROA (adjusted R-squared 0.986876). Operational efficiency (BOPO) and net interest margin (NIM) are the strongest drivers, loan to deposit ratio has a small negative effect, and problem credit has no significant effect. Analysis was done in EViews 12.

# Project background
Bank Jatim is a regionally owned bank whose mission is to support development and economic growth in East Java, which sets it apart from private and national banks. Banks measure their financial performance largely through profitability, and the standard measure is Return on Assets, profit after tax divided by total assets. A higher ROA means the bank earns more from the assets it manages. Bank Jatim's ROA has followed a decreasing trend over 2016 to 2023. It was 3.12% in 2017, then fell to 2.96% in 2018 and 2.73% in 2019. It dropped sharply to 1.95% in 2020 because total assets grew without a matching rise in net profit, recovered slightly to 2.05% in 2021, and fell again to 1.95% in 2022 and 1.87% in 2023. The level is still healthy, since it stays above 1.5%, but the downward drift raises a practical question: which operating and balance-sheet ratios explain it? The project asks how four widely used ratios affect Bank Jatim's ROA, individually and together. The expected directions from the literature are that higher NPL and higher BOPO reduce profitability, while higher LDR and higher NIM raise it.

# Data and methodology
The data are secondary quarterly time series taken from Bank Jatim's published financial reports, covering 2016 Q1 to 2023 Q4, which gives 32 observations. The dependent variable is ROA. The four independent variables are NPL (non-performing loans divided by total loans), BOPO (operating costs divided by operating income, where a lower value means better efficiency), LDR (loans divided by deposits, a measure of liquidity and how much of the funds raised are lent out) and NIM (net interest income relative to productive assets).
The model is a multiple linear regression, ROA = a + b1 NPL + b2 BOPO + b3 LDR + b4 NIM + e, estimated by ordinary least squares in EViews 12. Before interpreting the coefficients, the model was checked against four classical assumptions: normality of residuals, no autocorrelation (Breusch-Godfrey LM test), no multicollinearity (variance inflation factor below 10) and no heteroscedasticity (Glejser test), all judged at the 5% significance level. Hypotheses were then tested with t tests for each variable, an F test for the variables together, and the adjusted R-squared for explanatory power.

# Key findings
1. Descriptive statistics
Over the 32 quarters, ROA averaged 2.81% with a standard deviation of 0.73 and ranged from 1.62% to 4.01%. NPL averaged 4.00% (range 2.49% to 4.92%). BOPO averaged 69.52% (range 59.89% to 79.02%), LDR averaged 63.12% (range 45.88% to 90.48%) and NIM averaged 5.97% (range 4.92% to 7.18%).

2. The model passes the classical assumption tests
Residuals are normally distributed, with a probability of 0.756231, well above 0.05. There is no serial correlation, with a Breusch-Godfrey probability of 0.3336 and a Durbin-Watson statistic of 2.353. There is no multicollinearity, since the centred variance inflation factors are 1.29 for NPL, 2.94 for BOPO, 5.27 for LDR and 8.44 for NIM, all below the threshold of 10. There is no heteroscedasticity, with a Glejser probability of 0.1261.

3. Regression results
The estimated equation is ROA = 4.833848 + 0.024414 NPL - 0.075175 BOPO - 0.008595 LDR + 0.611023 NIM.
Operational efficiency is the dominant driver. BOPO has a negative and highly significant effect on ROA (coefficient -0.075175, t = -15.72, probability 0.0000): every one-point rise in the cost-to-income ratio is associated with a fall of about 0.075 points in ROA. Net interest margin has a positive and highly significant effect (coefficient 0.611023, t = 10.01, probability 0.0000), so a one-point wider margin is associated with about 0.61 points higher ROA.

Loan to deposit ratio has a negative and significant effect (coefficient -0.008595, probability 0.0262). This is the opposite of the expected sign. The authors explain it as lending that grows without matching income: operating expenses stay high, and the interest earned on loans does not exceed the interest paid on deposits, so a higher LDR does not lift ROA.

Problem credit has a positive but insignificant effect (coefficient 0.024414, probability 0.2670). This also differs from theory, and the paper attributes it to Bank Jatim's management of allowances for impairment losses (CKPN), which absorb the cost of bad loans so that rising NPL does not reduce profit. It fits the pattern in the data: from 2016 to 2019, NPL fell by an average of 0.67 points while ROA still fell slightly, and in 2020 to 2021, NPL rose by an average of 0.85 points and ROA fell by 0.78 points in 2020 but recovered a little in 2021.

4. Overall fit
The four ratios together are highly significant (F statistic 583.7852, probability 0.000000). R-squared is 0.988570 and adjusted R-squared is 0.986876, so the model explains 98.69% of the variation in ROA, leaving 1.31% to other factors.


# Recommendations
1. For the bank
Bank Jatim should keep its BOPO ratio low, because it is the strongest lever on profitability. The paper suggests finding cost reductions that do not harm service quality, mainly through automating processes and digitising operations to raise productivity. It should also strengthen credit monitoring and credit portfolio management, for example by diversifying the loan book to avoid concentration on a few borrowers, so that rising lending translates into income rather than cost. Finally, it should protect its net interest margin by monitoring benchmark interest rates, since NIM has the largest positive coefficient in the model.

2. For further research
Future studies should extend the research period to capture longer trends, and add variables that may also drive profitability, such as capital adequacy, credit growth and macroeconomic factors including interest rates.

# Limitations and next steps
The study covers one bank and 32 quarterly observations, so the results describe Bank Jatim and should not be generalised to other banks without more data. The explanatory power is very high (98.69%), which is partly expected because BOPO and ROA are both built from the same income statement, so BOPO moves closely with profit. Robustness checks would show how much of the fit comes from that overlap, for example re-estimating without BOPO or adding lagged variables. Because the data are a time series, testing the variables for stationarity (unit root tests) and, if needed, using a cointegration or error-correction approach would make the estimates more reliable. The paper itself proposes adding capital adequacy, credit growth and macroeconomic variables. Comparing Bank Jatim with other regional development banks would show whether the unexpected LDR and NPL results are specific to this bank.

# Team
Authors, as listed on the paper: Rya Refi Aushaf, Nimas Candhyta Maharani, Nur Laila Kamaliyah, Nabila Yuliana Putri and Vidya Purnamasari, all from the Faculty of Economics and Business, Universitas Negeri Malang. The supervising lecturer is Vidya Purnamasari, S.E., M.Sc.

# References
1. Abdurrohman, Fitrianingsih, D., Salam, A.F. and Putri, Y. (2020). The influence of Capital Adequacy Ratio (CAR), Loan to Deposit Ratio (LDR) and Non-Performing Loan (NPL) on Return on Assets (ROA) in the banking sector on the Indonesia Stock Exchange. Journal of Revenue, 1(1), 125-132.
2. Ashari, N., Ridjal, S. and Sohilauw, M.I. (2024). The influence of CAR and BOPO on banking profitability with non-performing loans as moderating. Management Studies and Entrepreneurship Journal, 5(2), 4520-4531.
3. Iklin, M. (2024). The influence of CAR, NPL, BOPO and LDR on return on assets at regional development banks: empirical study at PT BPD throughout Java, 2005-2021. Al-Kharaj, 6(1), 360-379.
4. Pinasti, W.F. and Mustikawati (2018). The influence of CAR, BOPO, NPL, NIM and LDR on commercial bank profitability, 2011-2015. Nominal Journal, 7(1), 126-142.
5. Rosadi, R.M.V. and Ramadhan, Y. (2024). Contribution of CAR, NPL, LDR, BOPO and NIM to return on assets of regional development banks. Management Studies and Entrepreneurship Journal, 5(2), 3802-3818.
6. Bank Jatim quarterly financial reports, 2016 to 2023 (data source).
