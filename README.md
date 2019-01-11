`<p>This is done as capstone project in BFSI domain and submitted as first phase.</p>
<p>Problem Description:<br>
Given demographic data and credit bureau data of the CredX applicants, asked to evaluate the customers of CredX using scorecard.</p>
<p>Methodology:<br>
Followed CRISP-DM framework and below are the components. Also described achievments and approach followed in each component.</p>
<ol>
<li>
<p>Business Objective:</p>
<p>CredX is a leading credit card provider that gets thousands of credit card applicants every year. But in the past few years, it has experienced an increase in credit loss. Company believes that the best strategy to mitigate credit risk is to ‘acquire the right customers’.<br>
In this project, we will help CredX to identify the right customers using predictive models. Using past data of the bank’s applicants, we need to determine the factors affecting credit risk, create strategies to mitigate the acquisition risk.</p>
</li>
</ol>
<ol start="2">
<li>
<p>Data understanding:</p>
<p>Exploratory Data Analysis (EDA), is performed in various levels such as univariate, bi-variate and multivariate to understand the data<br>
and to understand the driving factors that impacts ‘PerformenceTag’. Below is the highlevel snapshot of given data.</p>
<p>Demographic/applicant data: This is obtained from the information provided by the applicants at the time of credit card application. It contains customer-level information on age, gender, income, marital status, etc.</p>
<p>Credit Bureau Data: This is taken from the credit bureau and contains variables such as ‘number of times 30 DPD or worse in last 3/6/12 months’, ‘outstanding balance’, ‘number of trades’, etc.</p>
</li>
<li>
<p>Data preparation:</p>
<p>Below data quality issues:</p>
<ol>
<li>Credit bureau data has 3 duplicate application id’s. We have removed it.</li>
<li>Applicant age ‘-3’ has treated as incorrect age.</li>
<li>Gender- 2 rows have missing for gender.</li>
<li>Marital Status is missing for 6 applicants.</li>
<li>Number of Dependents were missing for 3 Applicants , out of which 1 applicants age is 0.</li>
<li>One Applicants Income is mentioned as -0.5.</li>
<li>Education details are missing for 119 applicants.</li>
<li>Profession information is missing for 14 Applicants.</li>
<li>Type of Residence is missing for 8 Applicants.</li>
<li>Performance Tag for 2% of the total applicants is Missing.</li>
<li>All the missing values except Performance Tag were replaced with WOE values.</li>
<li>Missing values for Performance tag have been treated as Rejected applicants.</li>
</ol>
<p>WoE Analysis:</p>
<p>Performed analysis on WoE plots, to identify the impact of PerformenceTag on each of the attribute in given data. Created Wieght of Evidence (WoE) values for each attribute on merged data (Demographic Data + Credit Bureau Data). Populated WoE values in given data for futher model building.</p>
<p>Information Value Analysis:</p>
<p>Created InformationValue for each of the attribute to measure the level of significancy of individual attributes on ‘PerformenceTag’.<br>
Followed the bench mark convention, to identify the significance of attributes.</p>
</li>
<li>
<p>Modeling:</p>
</li>
<li>
<p>Evaluation:</p>
<p>Performed a recommended split of 70:30 of the merged data (Demographic Data + Credit Bureau Data). Built Bayesian logistic regression model, to better understand the string attributes, on training data.Could achieve 90% accuracy, 88% of sensitivity and 90% of specificity. Provided the performence factors of built logistic regression model. Obtained model is further used to compute scorecard of the customer. peformed prediction on test data.</p>
</li>
<li>
<p>Deployment:</p>
</li>
</ol>`