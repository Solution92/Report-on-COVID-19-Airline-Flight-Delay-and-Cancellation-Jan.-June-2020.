# Report-on-COVID-19-Airline-Flight-Delay-and-Cancellation-Jan.-June-2020.

## Table of Content
- [Project Objective](#project-objective)
- [Data Source](#data-source)
- [Tools Used](#tools-used)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Analysis](#data-analysis)
- [Dashboard](#dashboard)
- [Result and Findings](#result-and-findings)
- [Recommendation](#recommendation)
- [Limitation](#limitation)
- [Reference](#reference)


### Project Objective

The United States Department of Transportation’s (DOT) Bureau of Transportation Statistics tracks the on-time performance of domestic flights operated by large air Carriers. The Data collected is from January to June 2020, it contains relevant flight information (one-time, delayed, canceled, and delivered flights), as contained in the Column.

I wanted to know the impact of the virus on the domestic United States airline industry through flight delay and cancellation data. So I downloaded the Dataset from kaggle.com.

### Data Source

[Kaggle](https://www.kaggle.com/datasets/akulbahl/covid19-airline-flight-delays-and-cancellations)

### Tools Used

Power BI

### Data Cleaning and Preparation

This Dataset has 47 Columns and 3 million rows.

In this Analysis, I analyzed the Top 10 United States flight Carriers for 11 million flights. These are American Airlines (AA), Alaska Airlines (AS), JetBlue (B6), Delta Airlines (DL), Frontier Airlines (F9), Allegiant Air (G4), Hawaiian Airlines (HA), Spirit Airlines (NK), United States Airline (UA), and Southwest Airlines (WN).

 Data Exploration is the stage where I deploy my experience in detecting and replacing “null” values in different Columns by highlighting the Column header, right-clicking on it, and doing “Replace Values…”

Here, I also detected an error in the “FL_DATE” Column. I quickly fixed it by selecting the Column header, going to the “Transform Data” tab on the ribbon, did selecting “Replace Errors” and they were gone.

I then loaded the Dataset from the query editor to Power BI Desktop for further insights.

### Exploratory Data Analysis (EDA)

Data analysis Expression. This is where all my measures are created using different formulas. To do that I clicked on the “Enter Data” tab and in the name tab I simply changed the “Table” to “DAX” and clicked on “Load”.

Measures, create Measures I needed to make the DAX table active by just clicking on it on the top right corner of the screen, clicking on “New Measure” and creating the following measures:

- Total No. of Carrier
- Total No. of Carrier Delay
- Total No. of Cancellation
- Total No. of Security Delay
- Total No. of Arrival Delay
- Total No.of Departure Delay
- Carrier with the Highest Arrival Delay
- Carrier with the Highest Cancellation
- Carrier with the Highest Department Delay
- Carrier with the Highest Security Delay
- Highest Carrier Delay

  ### Data Analysis
~~~
- Total No. of Carrier = DISTINCTCOUNT(‘Covid19FlightDelay_Jan-June2020’[MKT_UNIQUE_CARRIER]) = 10
- Total No. of Carrier Delay = DISTINCTCOUNT(‘Covid19FlightDelay_Jan-June2020’[CARRIER_DELAY]) = 1,131
- Total No. of Cancellation = DISTINCTCOUNT(‘Covid19FlightDelay_Jan-June2020’[CANCELLED]) = 2
- Total No. of Security Delay = DISTINCTCOUNT(‘Covid19FlightDelay_Jan-June2020’[SECURITY_DELAY]) = 105
- Total No. of Arrival Delay = DISTINCTCOUNT(‘Covid19FlightDelay_Jan-June2020’[ARR_DELAY]) = 1,393
- Total No.of Departure Delay = DISTINCTCOUNT(‘Covid19FlightDelay_Jan-June2020’[DEP_DELAY]) = 1,371
~~~

### Dashboard

![Screenshot_139](https://github.com/Solution92/Report-on-COVID-19-Airline-Flight-Delay-and-Cancellation-Jan.-June-2020./assets/144762124/b66f02b9-8a20-4771-8c34-d398d8c930a3)


### Result and Findings

- At 213,477, G4 had the highest Sum of ARR_DELAY and was 105.89% higher than WN, which had the lowest Sum of ARR_DELAY at -3,622,905.  WN accounted for 32.18% of Sum of ARR_DELAY.  Across all 10 MKT_UNIQUE_CARRIER, Sum of ARR_DELAY ranged from -3,622,905 to 213477. 
- At 78,904, AA had the highest Sum of CANCELLED and was 6,268.36% higher than HA, which had the lowest Sum of CANCELLED at 1,239.  AA accounted for 27.89% of Sum of CANCELLED.  Across all 10 MKT_UNIQUE_CARRIER, Sum of CANCELLED ranged from 1,239 to 78,904.  
- At 2,771,750, AA had the highest Sum of DEP_DELAY and was 31,458.19% higher than HA, which had the lowest Sum of DEP_DELAY at -8839. AA accounted for 32.36% of Sum of DEP_DELAY.  Across all 10 MKT_UNIQUE_CARRIER, Sum of DEP_DELAY ranged from -8839 to 2,771,750.  
- At 8,435, AA had the highest Sum of SECURITY_DELAY and was Infinity higher than F9, which had the lowest Sum of SECURITY_DELAY at 0.   AA accounted for 33.53% of Sum of SECURITY_DELAY.  Across all 10 MKT_UNIQUE_CARRIER, Sum of SECURITY_DELAY ranged from 0 to 8,435.  
- At 2,060,626, AA had the highest Sum of CARRIER_DELAY and was 3,324.33% higher than HA, which had the lowest Sum of CARRIER_DELAY at 60176.  AA accounted for 29.93% of Sum of CARRIER_DELAY.  Across all 10 MKT_UNIQUE_CARRIER, Sum of CARRIER_DELAY ranged from 60,176 to 2,060,626.  

### Recommendation

- Based on the analyzed dataset of flight delays, carrier AA consistently has the highest sums across various delay categories. To improve overall performance and passenger satisfaction, it is recommended that AA assess and enhance its operational efficiency and reliability. 
- Identifying and addressing the root causes of delays, such as security issues or carrier-related problems, can contribute to a more punctual and secure air travel experience. 
- Additionally, considering collaboration with industry stakeholders and implementing best practices may help AA reduce delays and enhance its standing in comparison to other carriers.

### Limitation

- The dataset limitations include potential gaps in understanding the root causes of delays, as it lacks detailed information on factors like weather conditions or operational issues. 
- The absence of temporal variations and regional breakdowns may obscure trends related to seasonal influences or geographical disparities in delay patterns. 
- Additionally, the dataset does not provide insights into specific flight routes or the overall volume of flights for each carrier, limiting a comprehensive understanding of performance. 
- The presence of missing values, represented by empty cells, raises concerns about data completeness and accuracy, potentially impacting the reliability of the analysis. 
- Finally, the dataset solely focuses on summarized delay metrics, overlooking broader operational aspects that could contribute to a more nuanced evaluation of airline performance.

### Reference

Refer to Data source above.





















