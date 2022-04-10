# Module-4-Challenge - Analyzing Portfolio Risk and Return

This program analyzes 4 Whale funds against S&P 500 market data to recommend a fund to be included for retirees.

The Starter Code was provided along with the fund data in csv format.

---

## User Story

As a quantitative analyst for a FinTech investing platform, you've been tasked with evaluating four new investment options for inclusion in the client portfolios. You’ll need to determine the fund with the most investment potential based on key risk-management metrics: the daily returns, standard deviations, Sharpe ratios, and betas.

This Fintech investing platform aims to offer clients a one-stop online investment solution for their retirement portfolios that’s both inexpensive and high quality. 

---

## Acceptance Criteria

* The data to be acceptable in csv format  
* Ablility to clean data by:  
    - removing NaN data items  
* Data Analysis covering:
    - Volatility: using box plots of daily percent returns data 
    - Performance: using cumulative daily percent returns data
    - Risk: using standard deviation/annualized standard deviation with rolling window of 21 days
    - Risk/Return: using Sharpe Ratios 
    - Sensitivity to Market: using Betas with rolling window of 60 days for the fund against the market
    
---

## The Application  

The application follows these stages:  
* Data Collection - the application reads in the csv data file, **whale_navs.csv**. 
* Data Preparation - 
    - indexing on Date/Timestamp
    - converts the trade data to daily percent returns using pct_change()
    - cleaning the data - removes NaN entires.
* Data Analysis -
    - Performance: to see if any fund performed better than S&P 500, using:
        - dailiy returns 
        - cumulative returns
    - Volatility: to determine relative volatility and the most & least volatile funds
        - for all the four funds and S&P 500 using box plots
        - only for four funds using box plots
    - Risk: to compare portfolio risk against the market and also determine the riskiest fund using:
        - portfolio standard deviation
        - annualized portfolio standard deviation using a rolling window of 21 days, with and without market
    - Risk/Return: to determine which fund offers the best risk adjusted returns, using:
        - Sharpe Ratios 
        - plotting Sharpe Ratios on a Bar plot
    - Sensitivity to Market: to determine the fund sensitivity to S&P 500 and make recommendation, using:
        - Beta calculations using rolling window of 60 days for the selected funds:
            - using covariance for funds and market variance
        
---

## Technologies

The application is developed using:  
* Language: Python 3.7,   
* Packages: fire 0.3.1 for CLI and questionary 1.5.2 for prompts  
* Development Environment: VS Code and Terminal, Anaconda 2.1.1 with conda 4.11.0, Jupyterlab 3.2.9  
* OS: Mac OS 12.1

---

## Installation Guide

Following are the instructions to install the application from its Github respository.  

### Clone the application code from Github as follows:


copy the URL link of the application from its Github repository      
open the Terminal window and clone as follows:  

    1. $cd to_your_preferred_directory_where_you want_to_store_this_application  
    
    2. $git clone URL_link_that_was_copied_in_step_1_above   
    
    3.  $ls     
        Module-4-Challenge    
        
    4. $ cd Module-4-Challenge     


At this point you will have the the entire application files in the current directory as follows:

    * README.md                   (this file that you are reading)
    * risk_return_analysis.ipynb      (the application jupter lab notebook)
    * Resources                        (folder)
        - whale_navs.csv   (Coinbase Exchange Data)

---

## Usage

The following details the instructions on how to run the application.  

### Setup the environment to run the application
Setup the environment using conda as follows:

    5. $conda create dev -python=3.7 anaconda  
    
    6. $conda activate dev  
    
    7. $jupyter lab  

---

### Run the Application

THIS ASSUMES FAMILIARITY WITH JUPYTER LAB. If not, then [click here for information on Jupyter Lab](https://jupyterlab.readthedocs.io/en/stable/).  

After step 7 above, this will take you to the jupyter lab window, where you can open the application notebook **risk_return_analysis.ipynb** and run the application.  

**NOTE**:
>Your $ prompt will look something like __(dev) ashokpandey@Ashoks-MBP loan_qualifier_app$__ ,  with:  
    - '(dev)' indicating the activated 'dev' environment,   
    - ' ashokpandey@Ashoks-MBP ' will be different for you as per your environment, and   
    - 'loan_qualifier_app' directory is where app.py is located.  
    - '$' sign is the dollar prompt  

---

## Contributors

Ashok Pandey - ashok.pragati@gmail.com   
www.linkedin.com/in/ashok-pandey-a7201237

---

## License

The source code is the property of the developer. The users can copy and use the code freely but the developer is not responsible for any liability arising out of the code and its derivatives.

---