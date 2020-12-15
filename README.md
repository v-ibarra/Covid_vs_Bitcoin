# Covid_vs_Bitcoin
An analysis to correlate BITCOIN value vs Covid19 Cases

Data used to make this analysis.
  Covid19 data source:
  https://opendata.ecdc.europa.eu/covid19/casedistribution/csv
  
  BTCUSDT data source:
   https://www.binance.com/
   
Original Covid19 dataset has the following columns:
 [1] "dateRep"                                                    "day"                                                       
 [3] "month"                                                      "year"                                                      
 [5] "cases"                                                      "deaths"                                                    
 [7] "countriesAndTerritories"                                    "geoId"                                                     
 [9] "countryterritoryCode"                                       "popData2019"                                               
[11] "continentExp"                                               "Cumulative_number_for_14_days_of_COVID.19_cases_per_100000"

Original BTCUSDT dataset contains these columns:
 [1] "open_time"                    "open"                         "high"                         "low"                         
 [5] "close"                        "volume"                       "close_time"                   "quote_asset_volume"          
 [9] "trades"                       "taker_buy_base_asset_volume"  "taker_buy_quote_asset_volume" "symbol"                
 
 
For the analysis we have joined our datasets in two different CSV's.
  World_vs_Covid19.csv 
      'dateRep':    Date.
      'casosSum':   New Covid19 cases everyday.
      'decSum':     New Covid19 deaths everyday.
      'AcumuladoCasos':   Cumulative Covid19 cases.
      'AcumuladoDecesos': Cumulative Covid19 deaths.
      'BTCUSDT':  Bitcoin value on US Dollars
 
  Groups_vs_Covid19.csv
      'Date':       Date
      'CHN_NewCases': New Covid19 cases in China everyday.
      'CHN_NewCases': New Covid19 deaths in China everyday.
      'CHN_AcuCases': Cumulative Covid19 cases in China.
      'CHN_AcuDeaths': Cumulative Covid19 deaths in China.
      'JAP_NewCases': New Covid19 cases in Japan everyday.
      'JAP_NewCases': New Covid19 deaths in Japan everyday.
      'JAP_AcuCases': Cumulative Covid19 cases in Japan.
      'JAP_AcuDeaths': Cumulative Covid19 deaths in Japan.
      'EU_NewCases': New Covid19 cases in Europe everyday.
      'EU_NewCases': New Covid19 deaths in Europe everyday.
      'EU_AcuCases': Cumulative Covid19 cases in Europe.
      'EU_AcuDeaths': Cumulative Covid19 deaths in Europe.
      'USA_NewCases': New Covid19 cases in USA everyday.
      'USA_NewCases': New Covid19 deaths in USA everyday.
      'USA_AcuCases': Cumulative Covid19 cases in USA.
      'USA_AcuDeaths': Cumulative Covid19 deaths in USA.
      'BTCUSDT':  Bitcoin value on US Dollars
      
 Correlation
  Worldwide New Covid19 cases vs BTCUSDT = 0.894427
 
 Correlation Matrix = DF2 
 
 Rollmean used = 5.
 
 Dyroller applied in Dygraph.
 
