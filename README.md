# BTC strategy based on Fear and Greed index

## Project Overview
    By implementing this project the author was trying to demonstrate Fear and Greed index as powerful investment tool for leveraging your cash <br>

    ***Obvious fact: On top of market(ATH, for example) FnG is also high and vice versa. Therefore, was maken decision to invent strategy based on Fear and Value index***  

## Data Sources
    Whole data was derived from following sources: 
        - [Yahoo Finance](https://finance.yahoo.com/)
        - [Alternative](https://alternative.me/)
## Steps
    1. Data Collection
       
       1. Data was fetched from sourced mentioned above. BTC-USD price value starts with *2018-02-01*
       2. **Fear and Greed** index value is available since pointed date(2018-02-01) through Postman 
    
    2. Preprocessing. 
       
       1. BTC-USD all values were including at fetching data, including OHLC. All values except Close were excluded. FnG was derived entirely, including "Classification" column
       2. Two tables were merged.

        _Notation_: All fetched data was saved in relevant files:  <br>
        *btc_df.csv* *fear_greed_index.csv* *response_fng.csv*
    
    3. Analysis. 
        
        -Initially _Correlation_ between BTC-USD and FnG was found. <br> 
        - BTC-USD value dumps follows Fear and Greed index reaching Extreme High Value and vice versa
    
    ***Strategy description***:
        1. At Extreme Greed FnG value (*85*) BTC is being sold
        2. At Extreme Fear FnG value (*15*) BTC is being bought
    
     4. Results
        
        1. _Correlation_ between two values is <br> *0.4242930280608611*
        2. ![corr](/home/x_ray_trader/ML/BTC_strategy_on_FnG)