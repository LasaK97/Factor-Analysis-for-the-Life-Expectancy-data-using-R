# Factor Analysis for the Life Expectancy Data set

### 1. Introduction
Factor analysis is a powerful statistical technique widely used in the field of data analysis and research. It allows researchers to identify underlying latent variables or factors that explain the relationships among a set of observed variables. These factors help in understanding the complex patterns and structures within the data, enabling more meaningful interpretations and insightful conclusions. So, in this project I have followed a systematic approach to factor analysis, including data preparation, selection of appropriate factor analysis methods, extraction of factors, and interpretation of results to finally obtain meaning full factors that explain the chosen dataset accurately.

### 2. Methodology

#### 2.1 Description of the dataset
This dataset is collected by the Global Health Observatory (GHO) data repository under World Health Organization (WHO) keeps track of the health status as well as many other related factors for all countries The datasets are made available to public for the purpose of health data analysis. The dataset related to life expectancy, health factors for 193 countries has been collected from the same WHO data repository website and its corresponding economic data was collected from United Nation website. Among all categories of health-related factors only those critical factors were chosen which are more representative. It has been observed that in the past 15 years, there has been a huge development in health sector resulting in improvement of human mortality rates especially in the developing nations in comparison to the past 30 years. Therefore, in this project we have considered data from year 2000-2015 for 193 countries for further analysis. The individual data files have been merged into a single dataset.

#### 2.2 Variable description
There are 1938 observations in 22 variables.
- Country – the country where data is collected.
- Year – The year where data is collected.
- Status – The country’s current development status.
- Life expectancy – The Life Expectancy in age.
- Adult Mortality – The Adult Mortality Rates of both sexes (probability of dying between 15 and 60 years per 1000 population).
- infant deaths - Number of Infant Deaths per 1000 population.
- Alcohol - Alcohol, recorded per capita (15+) consumption (in liters of pure alcohol).
- percentage expenditure – The expenditure on health as a percentage of Gross Domestic Product per capita (%).
- Hepatitis B – The Hepatitis B (HepB) immunization coverage among 1-year-olds (%).
- Measles – The number of reported cases per 1000 population.
- BMI – The average Body Mass Index of entire population.
- under-five deaths – The number of under-five deaths per 1000 population.
- Polio – The Polio (Pol3) immunization coverage among 1-year-olds (%).
- Total expenditure – The general government expenditure on health as a percentage of total government expenditure (%).
- Diphtheria – The Diphtheria tetanus toxoid and pertussis (DTP3) immunization coverage among 1-year-olds (%).
- HIV/AIDS – The deaths per 1 000 live births HIV/AIDS (0-4 years).
- GDP – The Gross Domestic Product per capita (in USD).
- Population – The population of the country.
- thinness 1-19 years – The prevalence of thinness among children and adolescents for Age 10 to 19 (%).
- thinness 5-9 years – The prevalence of thinness among children for Age 5 to 9(%).
- Income composition – The human development index in terms of income composition of resources (index ranging from 0 to 1).
- Schooling – The number of years of Schooling(years).

#### 2.2 Procedure
First, the data preparation was done by cleaning the data set and preprocessing the dataset. Then scaled the numerical variables and found the number of factors using scree plot. Then the factors were extracted.

### 3. Results and Discussion

#### 3.1 EDA Results
- There are 2938 observations in 22 variables.
- The highest correlation exists between infant deaths vs under five deaths and GDP vs percentage expenditure.

#### 3.2 EFA Results
*Using varimax rotations*,
- Factor 1 :- This factor has high loadings for variables such as infant deaths (0.969) and under-five deaths (0.967), indicating a strong association between these variables. So, we can explain this factor as child mortality factor.
- Factor 2 :- This factor has a high positive loading for life expectancy (0.908) and a high negative loading for adult mortality (-0.689). According to these values we can say that the higher values on this factor are associated with higher life expectancy and lower adult mortality rates. So, we can explain this factor as adult mortality factor.
- Factor 3 :- This factor has high negative loadings for variables such as BMI (-0.470), thinness in 1-19 years (-0.470), and thinness in 5-9 years (-0.208). According to these values we can say that the higher values on this factor are associated with lower BMI and higher rates of thinness. we can explain this factor as body composition and nutritional indicator factor.
- Factor 4 :- This factor has a high positive loadings for variables such as percentage expenditure (0.946) and GDP (0.965).These values indicated that the higher values on this factor are associated with higher percentage expenditure and GDP.So, this means we can explain this factor as economic indicator factor.
- Factor 5 :- This is factor has a high positive loading for Diphtheria (0.806) and moderate positive loadings for variables such as Hepatitis B (0.657). Acccording to these values higher values on this factor are associated with better Diphtheria and Hepatitis B vaccination coverage. This means this is the factor that explains the specific diseases factor.

### 4. Conclusion and recommendation
The null hypothesis says that the 5 -factor model is sufficient. However, p-value is < .05. So, we have to increase the number of factors until the value becomes greater than 0.05 to obtain the best results.

