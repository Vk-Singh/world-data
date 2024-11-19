# World Data

The World bank dataset consists of a number of features which can be used to develop interesting patterns in the data. I have collected the data for 7 countries for about 20 features. The data was pre-processed to remove columns with too many missing values and fill missing values with the average values for the features. Another way would have been to remove records with missing fields, however, this was not done since the data consists of records for 59 years only (one record per year per country). Hence, removing these values would have resulted in a very small dataset not suitable for analysis. Other efficient techniques can be used to find missing values to enhance the analysis.

Some analysis was done between the Population counts, birth rate and death rate which revealed some interesting patterns about how the birth rate and death rate affect the overall population. Similarly, based on the nature of the countries, it was found that India has highest percentage of Employment in agriculture. Other analyses on the power consumption variation with the total population also showed that electrical power consumption is the highest in most countries which relates to their population.

Further to this, more analysis can be performed on the Employment features such as percentage of males and females in each sector and comparisons can be made across years in different countries.

This analysis can also be used to develop predictive models to predict the population growth based on Birth Rate and Death Rate or GDP growth based on employment. The analysis can be extended in the future by including other features from the API like Arable land, Education, Health services, etc. and make predictions.


## Data Identification

For this analysis, the following API has been selected: https://datahelpdesk.worldbank.org/knowledgebase/articles/889392-api-documentation

The World Bank data consists of demographic and other statistical data related to Population, Employment, Health, GDP, Energy Consumption, etc. for all the countries from the year 1970 to 2023. These categories are called indicators and are each defined by a code.

The following indicators have been chosen for analysis:
* SP.POP.TOTL - Total Population
* SP.POP.TOTL.FE.IN - Total Female Population
* SP.POP.TOTL.MA.IN - Total Male Population
* SP.DYN.CBRT.IN Birth Rate
* SP.DYN.CDRT.IN Death Rate
* SE.COM.DURS - Compulsory Education Duration
* SL.IND.EMPL.ZS - Employment in Industry(%)
* SL.AGR.EMPL.ZS - Employment in Agriculture(%)
* SL.AGR.EMPL.FE.ZS - Female Employment in Agriculture(%)
* SL.IND.EMPL.FE.ZS - Female Employment in Industry(%)
* SL.UEM.TOTL.ZS - Unemployment(%)
* NY.GDP.MKTP.CD - GDP in USD
* NY.ADJ.NNTY.PC.KD.ZG - National Income per Capita
* NY.GSR.NFCY.CD - Net income from Abroad
* NV.AGR.TOTL.CD - Agriculture value added(in USD)
* EG.USE.ELEC.KH.PC - Electric Power Consumption(kWH per capita)
* EG.FEC.RNEW.ZS - Renewable Energy Consumption (%)
* EG.USE.COMM.FO.ZS - Fossil Fuel Consumption (%)
  
The following countries have been chosen for analysis:
* US - United States of America
* IN - India
* CN - China
* JP - Japan
* CA - Canada
* GB - Great Britain
* ZA - South Africa

The base API URL is http://api.worldbank.org/v2/ and is followed by the country code and indicator code to obtain the data for each year.
No authentication is required to use the API.
