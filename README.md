# Credit risk scoring for an online lending company

<img width="1018" alt="project_file1" src="https://github.com/user-attachments/assets/6331b400-f8c0-43ba-b342-e874eb2e0d3c">


- [Introduction](#introduction)
- [Objectives](#objectives)
- [Project results](#project-results)
    - [Predictive expected financial loss model + web application](#expected-loss-model)
    - [Business Insights](#business-insights)
- [Project structure](#project-structure)
- [Instructions](#instructions)
- [License](#licensing)

## Introduction <a name="introduction"></a>
The client is an online platform which specialises in lending various types of loans to urban customers. Borrowers can easily access lower interest rate loans through a fast online interface.

When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. Like most other lending companies, lending loans to ‘risky’ applicants is the largest source of financial loss. The company aims to identify such ‘risky’ applicants and their associated loan’s expected loss in order to utilise this knowledge for managing its economic capital, portfolio and risk assessment.

- [Checkout Website here. Play with website for exploaration] ([https://03-notebooks03-systemapp-risk-scoring-deploymentapp-ri-cv1jfo.streamlit.app/](https://03-notebooks03-systemapp-risk-scoring-deploymentapp-ri-cv1jfo.streamlit.app/)

## Objectives <a name="objectives"></a>
Creating an advanced analytical asset based on machine learning predictive models to estimate the expected financial loss of each new customer-loan binomial.

## Project results  <a name="project-results"></a>
### Expected financial loss model and web application <a name="expected-loss-model"></a>
In order to estimate the expected financial loss (EL) associated to a certain loan application, three risk models have been developed:
1. **Probability of default model (PD):** The purpose of this model is to predict the probability that a given borrower will default.
2. **Exposure at default model (EAD):** The objective of this model is to predict the percentage of the loan that a given borrower has not yet repaid when a default occurs.
3. **Loss given default model (LGD):** The objective of this model is to predict the percentage of the principal that will not be possible to recover from a loan that has been defaulted on.

Once the probability of default, exposure at default and loss given default models have been developed, the expected loss (EL) for each new loan application is obtained by simply combining the predictions of these models and the principal amount of the loan as follows:

> EL($) = PD(%) · Principal($) · EAD(%) · LGD(%)

<img width="487" alt="project_data" src="https://github.com/user-attachments/assets/b99c45a0-b8fa-43f9-a4ee-7e842d8787ae">


Finally, in order to get the most value out of the developed machine learning model, a prototype web application has been designed so employees can start using them to make practical decisions. This web app collects, on the one hand, the internal data that the company has for each client and on the other hand, the information provided by the borrower itself through a loan application.

[**Launch Credit Risk Analyzer Web App!**](https://03-notebooks03-systemapp-risk-scoring-deploymentapp-ri-cv1jfo.streamlitapp.com/)

<img width="1018" alt="project_file1" src="https://github.com/user-attachments/assets/6331b400-f8c0-43ba-b342-e874eb2e0d3c">

### Business Insights derived from exploratory data analysis <a name="business-insights"></a>
#### Borrowers:
- Borrowers with poorer credit scores tend to borrow larger amounts and have lower annual incomes than clients with higher credit scores, thus paying higher monthly installments and higher interest rates.
- One third of all customers have been employed for more than 10 years. The job title of most clients is unknown. Of the clients who do provide this information, the top three most frequent jobs are ‘Teacher’, ‘Manager’ and ‘Owner’.
- The score feature appears to be predictive of loan status: the percentage of loans charged off increases as the borrower’s credit score worsens while the percentage of fully paid loans increases as the borrower’s credit score increases.
- Three main groups can be clearly distinguished: those borrowers who used less than 20% of the credit available on their credit card, another group of borrowers have used between 20 and 80 percent of the available credit on their credit card, and a last group of borrower who have used more than 80% of their available credit on their credit card.
#### Loans
- In general, 60-month loans tend to have a higher percentage of late payments and charge-offs.
- The percentage of loans charged off for ‘moving’ and ‘small business’ purposes is slightly higher (16%-17%) than the average for the rest of loan purposes (around 11%).


## Instructions  <a name="instructions"></a>
The project should be run using exactly the same environment in which it was created.

- Project environment can be replicated using 'pf_riskscoring.yml' file which was created during the set up phase of the project. It can be found in the folder '01_Documents'.
- Copy 'pf_riskscoring.yml' file to the directory and using the terminal or anaconda prompt execute:
    > conda env create --file pf_riskscoring.yml --name project_name

By other hand, remember to update the `project_path` variable of the notebooks to the path where you have replicated the project.

## Licensing <a name="licensing"></a>
The data set, licensing, and other descriptive information is available at [LendingClub website](https://www.lendingclub.com/).
