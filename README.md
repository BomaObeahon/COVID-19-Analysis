# Final-Project-Tableau

## Project/Goals
The general goal of this project is to collaborate with classmates on github and apply all the skills that have been aquired throughout the course till now including:
* data collection (from APIs or other methods)
* data cleaning
* EDA
* regression modelling
* creating visualizations

For our project specifically, we will be exploring the topic of COVID-19 - more specifically, we will be trying to answer the following questions:

1. How does the GDP per capita affect rates of confirmed cases and rates of mortality?
2. How does location (longitude and neighbouring countries) affect the rates of infection and mortality?
3. What kinds of insights can be made to predict future pandemics, their spread and outcomes?

## Process
### Step 1: Data Collection
Exploring what kinds of data is available for free
### Step 2: EDA
Initial exploration efforts to understand data and cleaning data as needed
### Step 3: Insights and Regression Modelling
In narrowing down the questions, various models are tried and iterated to get a reliable regression model
### Step 4: Create Visualizations
Once conclusions were reached, visualizations were created for presentation

## Results
As of March 9th, 2023, (our last recorded update in the data set) the global COVID-19 situation reports over 687 million confirmed cases worldwide, with approximately 7 million confirmed deaths. The top five most severely affected countries by the COVID-19 pandemic were the United States, India, France, Germany, and Brazil. These nations experienced a significant impact in terms of confirmed cases, and deaths. 

(See data > animation_cleaning
and animations)

Through these general results, we wanted to understand the answers to 2 questions:
1. How does the LONGITUDE (ie. average temperatures) of a country affect confirmed cases and mortality rates of COVID-19?

The longitude had a minor positive correlation to the rate of confirmed cases. Even though anecdotally, we understand that the transmission rate is higher in warmer climates compared to colder ones, it seems that many more factors seem to play a role in determining the outcome of COVID-19 in a country. Some major factors that we suspect being more effective in predicting the amount of cases is governmental policy and restriction effectiveness within a country. 

This conclusion is also true when looking into the Fatality Ratio Per 100 Cases and the Incident Rate per 100,000 Population. The countries that have the high incident rate per population does not correlate well with the fatality rate per cases. The conclusion being that many more factors play into the mortality rate of COVID mainly being other health care provisions and the way the country handled the pandemic as a whole

(See data > pipedream)

2. How does the GDP and POPULATION affect confirmed cases and mortality rates of COVID-19?

When analyzing the correlation between GDP or POPULATION against CONFIRMED CASES we have these take aways
* GDP / CONFIRMED CASES
  * R-squared = 0.105 (predicts ~10% of the variance)
  * P-value = 4.85 e-5 (statistically significant)
  * COEF = 57.6124 (increase of 57.6124 cases per increase of GDP / capita)
* POP / CONFIRMED CASES
  * R-squared = 0.124 (predicts ~12% of the variance)
  * P-value = 9.61 e-6 (statistically significant)
  * COEF = 2.797 e+4 (increase of 2797 cases per increase of 1 million population)

In general we can see that both GDP and Population can be predicted to increase the amount of confirmed cases in a country. While we expect the population increase to increase COVID cases, the result of increased GDP = increased cases was more unexpected. Originally, we hypothesized that an increased GDP meant that there would be more financial ability to provide public safety meansures. However, the data points towards the opposite conclusion. It seemed that the private freedoms that citizen demanded from their governments in higher GDP countries ultimately led to a higher increase of confirmed cases of COVID-19 unfortunately.

(See data > GDP_POP regression)

## Challenges 
The major challenge was the introduction of collboration on GitHub. This was the first time that any of us had any significant usage of Git and GitHub aside from the other projects (but did not require much Git usage). The process of data professions working together on one project similar to that of a workplace was able to teach us the importance of communication in:

* direct messaging updates
* comments on new commits
* comments on code 
* general organization (within GitHub, scheduling, and presenting)

Another challenge we faced was gathering data. In an effort to challenge ourselves, we wanted to query APIs to gather our data. Our oversight of the fact that the COVID-19 pandemic was official declared over in most countries by May of 2023, all API providers had since ended their regular updates. As a result, we were unable to query and APIs and had to rely on historical data. Fortunately, this data was very robust and useful for the rest of the project. Some of these data sets sheer size (~shape = 1500 x 500) and our inexperience with cleaning data also proved to be a challenge we had to overcome. 

Lastly, collaboration on Tableau also introduced its own host of challenges. Since we only have Tableau, we quickly ran into its issues - specifically with data extraction and saving these files so other group members could have access to compile them all together. A new technique that we experimented with - animations - proved to be a very valuable asset for our presentation, but also was a very time consuming effort on its own.

## Future Goals
With the introduction of this project, we had barely begun to scratch the surface of the implications that these results could potentially generate. Given more time, it would to useful to explore any subset of these following questions:

* How does governmental policies / healthcare policy / funding / government subsidies affect the number of confirmed cases and mortality for COVID-19?
* How does personal characteristics (predisposition to other health issues / weight / age / career / beliefs) affect the likelihood of someone contracting COVID-19?
* How did specific medical procedures help the outcome of COVID-19? Does it have any affect on mortality rates?
* How does long COVID-19 continue to affect people now?
* How does r0 (transmission rate) compare in different parts of the world taking into account the above situations?
* How did COVID-19 spread from country to country, province to province?

All of these questions can be used to analyze and create a fully model of how this most recent pandemic has affected our world. The applications of this would heighten governmental and healthcare policies for the next inevitable pandemic and demonstrate weak spots where policies and procedures put in place to protect people failed. From these expanded results, (since COVID-19 is the first pandemic of our fully globalized and fully interconnected world), we may be able to better predict what to do if this situation every presents itself again. This ultimate scenario is not just a hypothetical but a certainty according to epidemology experts, it is more a question of when compared to a question of if.

## References [Data Sets]

International Monetary Fund. (2023). Download WEO Data: October 2023 Edition. [Data set]. https://www.imf.org/en/Publications/WEO/weo-database/2023/October

John Hopkins Hospital (2023). Coronavirus Cases and Deaths. [Data set]. https://nuttaphat.com/covid19-api

M-Media-Group (2023). Covid-19-API [Data set]. https://github.com/M-Media-Group/Covid-19-API

Worldwide; IMF. (2023). The 20 countries with the lowest estimated gross domestic product (GDP) per capita in 2023. [Data set]. https://www.statista.com/statistics/256547/the-20-countries-with-the-lowest-gdp-per-capita/

Worldwide; IMF. (2023). The 20 countries with the largest gross domestic product (GDP) per capita in 2022.[Data set]. https://www.statista.com/statistics/270180/countries-with-the-largest-gross-domestic-product-gdp-per-capita/

HDX - Novel Coronavirus (COVID-19) Cases Data. https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases
