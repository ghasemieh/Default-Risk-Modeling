# Default Risk Modeling
Data Analysis and Modeling

![Image of Default Risk](/image/defaultRisk.jpg)

## Introduction 
Home Credit is looking for a model to predict the possibility of loan repayment for their clients based on the information about applicants’ applications, credit card history, account balance and etc. The dataset contains of 7 relational tables. 

In my analysis, I will stick to using the main application training and testing data which should be more manageable. This will let me establish a baseline that I can then improve upon. With these projects, it's best to build up an understanding of the problem a little at a time rather than diving all the way in and getting completely lost. Next I will use other tables to tune my model.

## Literature Review
Credit risk management in banks essentially focuses on determining likelihood of client’s default or credit deterioration and how costly it will turn out to be if it does occur (George, Sinha, Murali, 2007) . Decisions concerning credit granting are one of the most important in commercial banks’ policy. Well allocated credits may become one of the biggest sources of profits for banks. On the other hand, this kind of bank’s activity is connected with high risk as big amount of bad decisions may even cause bankruptcy. The key problem consists of distinguishing good (that surely repay) and bad (that likely default) credit applicants. 
The main investigations, in this area, are based on building credit risk evaluation models, allowing for automating or at least supporting credit granting decisions (Zakrzewska, 2007) . According to Lai, Yu, Wang, Zhou(2006)  many different approaches including individual models, such as linear discriminant analysis, logit analysis, probit analysis, linear programming, integer programming, k-nearest neighbor, classification tree, survival analysis, artificial neural  networks, genetic algorithm, support vector machine and some hybrid models are widely applied to credit risk analysis tasks  . In this literature, I review some of these techniques and applications. 

Gabriel and Rosenthal(1991)  used probit analysis to evaluate the effects of borrower race and default risk in mortgage lending. The data include detailed information on the assets and liabilities of a nationally representative sample consisting of over 4,000 U.S. households. Using these data, a probit model of household mortgage loan choice was estimated by maximum likelihood. He found that non-whites are significantly less likely to obtain the conventional financing than whites. Therefore, race effects in the mortgage market.
Lawrence and Smith(1991) , used logistic regression to evaluate risk of mobile home credit. The data includes more than 170,000 loans, which randomly are selected approximately 42,000 accounts that were active as of September 1, 1988. In that model, higher probabilities of loan default are associated with poor payment histories, smaller loans, higher current loan-to-value ratios, loans that have been in effect for shorter periods, lower initial income-to-payment ratios, older borrowers, higher statewide unemployment rates, areas having greater retail sales per household, and states having higher-priced mobile homes.

Boyes, Hoffman and Low(1989)  suggested a model of credit assessment focuses on expected earnings. They demonstrated how maximum likelihood estimates of default probabilities can be obtained from a bivariate ‘censored probit’ framework using a ‘choice-based’ sample originally intended for discriminant analysis. His model demonstrates how expected earnings on revolving credit loans depend both on maintained balances and probability of default. The ‘choice-based’ estimator of Manski(1977)  may then be combined with the notion of ‘partial observability’ to estimate default probabilities from non-random samples of consumer lending behavior originally intended for use in discriminant analysis. They also questioned the sample collection which samples used to estimate repayment probabilities are censored since only applicants that receive credit are observed to default or repay and there is no way to observe the subsequent behavior of the excluded group. Heckman  has shown that censored samples can lead to biased estimates, if, in our example, the sample selection rule is correlated with the errors in the repayment probability equation. However, if lenders rely strictly on quantitative credit scores, sample selection is deterministically governed by applicant attributes and the sample selection rule does not lead to biased estimates while most lenders consider credit scoring as only one parameter of credit assessment procedure. Therefore, the standard Heckman procedure is not applicable. The data employed were obtained from a single large financial institution that monitored a non-random sample of its credit card applicants between 1977 and 1980 as well as the performance through 1984 of those granted credit. He found that variables which are significant (5% level) in both equations and carry opposite sign include age, number of dependents, post-baccalaureate education, home ownership, expenditures to income ratio, finance company reference, several credit bureau variables, number of months on the current job, between 13 and 15 years of education, home rental and department store credit card reference. He suggested instead of using credit scoring models, the complete model credit assessment would account for ‘time-to-default’ by applying split population survival time models of borrower behavior.

Srinivasan and Kim(1987)  applied four statistical models: multiple discriminant analysis (MDA), logistic regression (logit), goal programming (GP) and recursive partitioning algorithm (RPA), and a judgmental model based on the Analytic Hierarchy Process (AHP). The data employed for the study has been provided by an anonymous Fortune 500 corporation. They found that (nonparametric) recursive partitioning methods provide greater information than simultaneous partitioning procedure and the judgmental model performs as well as statistical model.

Hillman(2014)  used a binary logistic regression model to compare borrowers who defaulted against those who made standard “on‑time” repayments. The data is from Postsecondary Students (BPS) survey for 2003–2004 through 2008–2009. Participants in this survey (n ≈ 16,700) attended public, private nonprofit, and private for‑profit institutions in the United States and approximately 9,500 of the respondents had taken out federal student loans while enrolled in college. He found that students who attend for‑profit colleges are systematically (and to a greater magnitude) more likely to default than students attending other sectors of higher education. Also, students who come from upper‑income families or who are not first‑generation students face lower odds of defaulting. Alternatively, lower‑income students, minoritized students, and students who care for dependents face greater odds of defaulting when compared to their White and upper‑income peers who do not care for dependents.
Bellotti and Crook(2009)   applied survival analysis to build the default model using credit card account dataset from a UK bank which includes a period of credit card accounts opened from 1997 to mid-2005 with the total number of 100,000 accounts with application variables such as income, age, housing and employment status along with a bureau score taken at the time of application. They showed that probability of default is affected by general conditions in the economy over time and these macroeconomic variables cannot readily be included in logistic regression models. However, survival analysis provides a framework for their inclusion as time-varying covariates. They believe that a credit application scoring model involves predicting the probability that an applicant will default over a given future time period in terms of characteristics of the applicant measured at the time of application. Moreover, although LR has become a standard method for estimating applicant scoring models (Thomas et al, 2002) , using survival analysis for credit scoring allows us to model not just if a borrower will default, but when. The advantages of this method are that 

- survival models naturally match the loan default process and so incorporate situations when a case has not defaulted in the observation period
- it gives a clearer approach to assessing the likely profitability of an applicant
- survival estimates will provide a forecast as a function of time from a single equation

Survival analysis is used to study time to failure of some population. This is called the survival time. The results of the research demonstrate that survival analysis is competitive in comparison with LR as a credit scoring method for prediction. 

Bastos  (2010) used regression trees to evaluates the ability of a parametric fractional response regression and a nonparametric regression tree model to forecast bank loan credit losses. The dataset employed for this study is provided by the largest private bank in Portugal, Banco Comercial Português. The sample contains 374 loans granted to small and medium size enterprises that defaulted between June 1995 and December 2000. He evaluated the model with two different approaches: an out-of-sample estimation using the complete dataset with the help of a 10-fold cross-validation, and an out-of-time estimation in which the models are fit using defaults from one period and the accuracy is measured on defaults from the following year. When out-of-sample estimation is considered, the regression trees give better results for shorter recovery horizons of 12 and 24 months, while the fractional response regression gives better results for longer horizons.

Moulton, Haurin and Shi(2015)  used bivariate probit model with sample selection to model default, given that households have a choice to select into a HECM. The data employed from a large nonprofit housing counseling organization (ClearPoint Credit Counseling Solutions) for the years 2006–2011 which includes demographic and socio-economic characteristics of the counseled, household credit score, outstanding balances and payment histories on revolving and installment debts, and public records information with total number of 27,894 applicants. The result shows that property tax is one the main reasons which causes the default. 

## Dataset
The dataset has 7 tables. In this project I will try to use other table than application table to refine my result. However, it depends on the time availability. 

![Image of Data Structure](/image/datastructure.png)

### application_{train|test}.csv
- Size (train): 308k x 122
- Size (test): 48.7k x 121
- This is the main table, broken into two files for Train (with TARGET) and Test (without TARGET).
- Static data for all applications. One row represents one loan in our data sample.

### bureau.csv
- Size: 1.72m x 17
- All client's previous credits provided by other financial institutions that were reported to Credit Bureau (for clients who have a loan in our sample).
- For every loan in our sample, there are as many rows as number of credits the client had in Credit Bureau before the application date.

### bureau_balance.csv
- Size: 27.3m x 3
- Monthly balances of previous credits in Credit Bureau.
- This table has one row for each month of history of every previous credit reported to Credit Bureau – i.e the table has (#loans in sample # of relative previous credits # of months where we have some history observable for the previous credits) rows.

### POS_CASH_balance.csv
- Size: 10.0m x 8
- Monthly balance snapshots of previous POS (point of sales) and cash loans that the applicant had with Home Credit.
- This table has one row for each month of history of every previous credit in Home Credit (consumer credit and cash loans) related to loans in our sample – i.e. the table has (#loans in sample # of relative previous credits # of months in which we have some history observable for the previous credits) rows.

### credit_card_balance.csv
- Size: 3.84m x 23
- Monthly balance snapshots of previous credit cards that the applicant has with Home Credit.
- This table has one row for each month of history of every previous credit in Home Credit (consumer credit and cash loans) related to loans in our sample – i.e. the table has (#loans in sample # of relative previous credit cards # of months where we have some history observable for the previous credit card) rows.

### previous_application.csv
- Size: 1.67m x 37
- All previous applications for Home Credit loans of clients who have loans in our sample.
- There is one row for each previous application related to loans in our data sample.

### installments_payments.csv
- Size: 13.6m x 8
- Repayment history for the previously disbursed credits in Home Credit related to the loans in our sample.
- There is a) one row for every payment that was made plus b) one row each for missed payment.
- One row is equivalent to one payment of one installment OR one installment corresponding to one payment of one previous Home Credit credit related to loans in our sample.

### HomeCredit_columns_description.csv
- Size: 219 x 5
- This file contains descriptions for the columns in the various data files.

## Results

