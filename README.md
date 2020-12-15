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
  
 Correlation Matrix
                CHN_NewCases CHN_Newdeaths CHN_AcuCases CHN_AcuDeaths JAP_NewCases JAP_Newdeaths JAP_AcuCases JAP_AcuDeaths EU_NewCases EU_Newdeaths
CHN_NewCases    1.00000000    0.29372128  -0.27350573    -0.3917687  -0.16279578   -0.16279560   -0.2061047    -0.2736665  -0.1624422   -0.1850925
CHN_Newdeaths   0.29372128    1.00000000  -0.07321241    -0.1453126  -0.08771068   -0.06658083   -0.1510376    -0.2056936  -0.1047124   -0.0177220
CHN_AcuCases   -0.27350573   -0.07321241   1.00000000     0.9372144   0.37992966    0.31844489    0.4643379     0.5795932   0.3639181    0.3589884
CHN_AcuDeaths  -0.39176873   -0.14531259   0.93721439     1.0000000   0.41667916    0.38137326    0.5305528     0.7026597   0.3888969    0.3386650
JAP_NewCases   -0.16279578   -0.08771068   0.37992966     0.4166792   1.00000000    0.50927083    0.7933522     0.7046462   0.6821725    0.6187460
JAP_Newdeaths  -0.16279560   -0.06658083   0.31844489     0.3813733   0.50927083    1.00000000    0.4852789     0.4264981   0.3930109    0.5277246
JAP_AcuCases   -0.20610469   -0.15103764   0.46433791     0.5305528   0.79335222    0.48527888    1.0000000     0.9388179   0.8668164    0.5720259
JAP_AcuDeaths  -0.27366646   -0.20569361   0.57959316     0.7026597   0.70464616    0.42649810    0.9388179     1.0000000   0.7697736    0.4365647
EU_NewCases    -0.16244220   -0.10471240   0.36391815     0.3888969   0.68217248    0.39301094    0.8668164     0.7697736   1.0000000    0.7385867
EU_Newdeaths   -0.18509251   -0.01772200   0.35898836     0.3386650   0.61874601    0.52772464    0.5720259     0.4365647   0.7385867    1.0000000
EU_AcuCases    -0.18194431   -0.13185716   0.40566304     0.4613515   0.82689385    0.50655096    0.9495329     0.8733399   0.9130919    0.7026430
EU_AcuDeaths   -0.29983111   -0.19805445   0.61790199     0.7540934   0.75444130    0.50541263    0.9016606     0.9734163   0.7460861    0.5294854
USA_NewCases   -0.19952461   -0.12827065   0.43470697     0.4945956   0.87226653    0.50461148    0.8722850     0.8212176   0.8411008    0.7314042
USA_Newdeaths  -0.24543339   -0.04603786   0.46138425     0.5379036   0.52471947    0.58553540    0.4054767     0.4118679   0.3740783    0.6810516
USA_AcuCases   -0.21414164   -0.16100825   0.48147000     0.5571684   0.81512104    0.46396839    0.9934331     0.9549776   0.8575979    0.5580119
USA_AcuDeaths  -0.27779690   -0.20283008   0.59236283     0.7196695   0.70839969    0.40653336    0.9266251     0.9938335   0.7419446    0.4041845
BTCUSDT        -0.05128683   -0.09468345   0.31878832     0.3803871   0.80906667    0.44102634    0.9020145     0.8396090   0.8353635    0.5508561
              EU_AcuCases EU_AcuDeaths USA_NewCases USA_Newdeaths USA_AcuCases USA_AcuDeaths     BTCUSDT
CHN_NewCases   -0.1819443   -0.2998311   -0.1995246   -0.24543339   -0.2141416    -0.2777969 -0.05128683
CHN_Newdeaths  -0.1318572   -0.1980544   -0.1282706   -0.04603786   -0.1610083    -0.2028301 -0.09468345
CHN_AcuCases    0.4056630    0.6179020    0.4347070    0.46138425    0.4814700     0.5923628  0.31878832
CHN_AcuDeaths   0.4613515    0.7540934    0.4945956    0.53790361    0.5571684     0.7196695  0.38038712
JAP_NewCases    0.8268938    0.7544413    0.8722665    0.52471947    0.8151210     0.7083997  0.80906667
JAP_Newdeaths   0.5065510    0.5054126    0.5046115    0.58553540    0.4639684     0.4065334  0.44102634
JAP_AcuCases    0.9495329    0.9016606    0.8722850    0.40547669    0.9934331     0.9266251  0.90201454
JAP_AcuDeaths   0.8733399    0.9734163    0.8212176    0.41186789    0.9549776     0.9938335  0.83960899
EU_NewCases     0.9130919    0.7460861    0.8411008    0.37407829    0.8575979     0.7419446  0.83536352
EU_Newdeaths    0.7026430    0.5294854    0.7314042    0.68105161    0.5580119     0.4041845  0.55085610
EU_AcuCases     1.0000000    0.8808911    0.9536719    0.45023807    0.9554279     0.8429420  0.93817701
EU_AcuDeaths    0.8808911    1.0000000    0.8692073    0.54804921    0.9279850     0.9675021  0.83955432
USA_NewCases    0.9536719    0.8692073    1.0000000    0.55783312    0.8995161     0.8000501  0.88854680
USA_Newdeaths   0.4502381    0.5480492    0.5578331    1.00000000    0.4106888     0.4136097  0.35984044
USA_AcuCases    0.9554279    0.9279850    0.8995161    0.41068880    1.0000000     0.9460603  0.91532862
USA_AcuDeaths   0.8429420    0.9675021    0.8000501    0.41360970    0.9460603     1.0000000  0.82305699
BTCUSDT         0.9381770    0.8395543    0.8885468    0.35984044    0.9153286     0.8230570  1.00000000


