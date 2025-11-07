**November 6, 2025**<br>
**MPAD 2003A Introductory Data Storytelling**<br>
**Joshua Alam, Dana Al-Damiri, Isabel Yome**<br>
**Presented to Jean-Sébastien Marier**<br>

# Exploratory Data Analysis (EDA) & Pitch


## 1. Introduction

For this assignment, we will be analyzing the City of Ottawa’s 2021 Long Form Census. The census is done every 5 years, with a short form questionnaire sent to 100% of households in Ottawa and a long form census sent to only 25% of Ottawa’s households, and the ward data updated 2 years later. 

It contains information on age groups, marriage status, how many people live in the house, employment, income, languages spoken, and more. The dataset compares Ottawa’s wards. The long form census has more than three times the amount of rows than the short form census in order to get a deeper understanding of Ottawa’s population and demographics.

Link to the original dataset: https://open.ottawa.ca/datasets/ottawa::2021-long-form-census-ward-data/about

Link to the CSV file: https://raw.githubusercontent.com/jsmarier/files-for-course-assignments/refs/heads/main/2021_Long_Form_Census_-_Ward_Data.csv

In the following sections, we will be describing how the dataset was originally, and how we cleaned it for our purposes. We will then detail our analysis of the dataset, and the story that we found within.


## 2. Getting Data

To import the dataset into Google Sheets, the first step is to right-click on the webpage containing the data and select “Save as.” After saving the file to your computer, open Google Sheets and import the saved data file. When the import window appears, make sure to change the separator type to “comma” to ensure that the values are properly formatted into separate columns. Once imported, the dataset reveals that it contains 26 columns and 2063 rows, making it quite large and complex. At first glance, the data appears messy and unclear, as it includes mixed data types within several columns and rows that represent totals or subtotals rather than specific wards. These non-ward rows should be excluded to maintain clarity and accuracy in the analysis. The dataset is also wide, meaning that each variable, such as income, population, or education level, is represented by a separate column rather than grouped categories.

Focusing on specific wards, several patterns emerge. In Rideau-Vanier (Ward 12), the quantitative continuous variables show that this area generally has a lower median total income compared to suburban wards, suggesting higher levels of economic inequality in Ottawa’s central neighborhoods. The proportion of residents aged 0–14 years is relatively low, indicating fewer families with young children. Similarly, Somerset (Ward 14) also shows continuous quantitative data, typically reflecting the lowest median household income among all wards, a smaller percentage of children, and a higher share of working-age adults. By contrast, Barrhaven West (Ward 3) demonstrates higher median household incomes and one of the largest youth populations, aligning with its suburban, family-oriented character. Education levels are relatively high here, though slightly below those of more urban wards. Finally, Orleans East-Cumberland (Ward 1) displays strong middle to upper-middle-class characteristics, with high median incomes and one of the highest proportions of children, further emphasizing its family-centered demographic.

Overall, this dataset primarily contains discrete and quantitative variables. A key research question that emerges from these observations is: How do income levels and age distributions differ between downtown and suburban wards in Ottawa, and what might these differences reveal about family demographics and economic inequality?


## 3. Understanding Data

### 3.1. VIMO Analysis

The dataset comes from a questionnaire sent to 25% of households in Ottawa. This means that it does not represent the entire population of the city. While this is true, the dataset is still useful for identifying general trends.

The data that who's validity and accuracy I analyzed was pertaining to the number of people in different age groups and total income levels of the four wards we chose to represent the suburbs and downtown: Orleans East-Cumberland (Ward 1) and Barrhaven West (Ward 3) for the suburbds; Rideau-Vanier (Ward 12), and Somerset (Ward 14) for downtown. 

First, I added the number of people in different age groups according to the table together for each ward to see if they add up to the total number of people in the ward. I did this using the `SUM` function. I found that the sum of all age groups for each ward were equal to their total population +/- 10.
<br>
![](age_sums.png)
*Figure 1: This table shows the populations of each ward, the number of people in different age groups, and the sums of all the age groups for each ward*

I did the same with the different total income levels for each ward. I also found that the sum of the different total income levels of each ward were equal to their population with total income +/- 10.
<br>
![](income_sums.png)
*Figure 2: This table shows the populations of each ward, the number of people in different income levels, and the sums of all the income levels for each ward*

Next, I checked for outliers in the dataset. I did this by putting the data for the age groups of each ward, and the data for the total income levels of each ward into line graphs.
<br>
![](VIMO_age_graph.png)
*Figure 3: This graph shows trends in the populations of different age groups in four wards*

![](VIMO_income_graph.png)
*Figure 4: This graph shows trends in the populations of different income levels in four wards*

As we can see in the graphs, the data follows each other's trends, and there are no datapoints that are wildly out of place.

After this VIMO analysis, I have concluded that this dataset is valid, accurate, and fit for further analysis.
### 3.2. Cleaning Data

Insert text here.

### 3.3. Exploratory Data Analysis (EDA)

Insert text here.

**This section should include a screen capture of your pivot table, like so:**

![](pivot-table-screen-capture.png)<br>
*Figure 2: This pivot table shows...*

**This section should also include a screen capture of your exploratory chart, like so:**

![](chart-screen-capture.png)<br>
*Figure 3: This exploratory chart shows...*

## 4. Potential Story

Insert text here.

## 5. Conclusion

Insert text here.

## 6. References

Include a list of your references here. Please follow [APA guidelines for references](https://apastyle.apa.org/style-grammar-guidelines/references). Hanging paragraphs aren't required though.

**Here's an example:**

Bounegru, L., & Gray, J. (Eds.). (2021). *The Data Journalism Handbook 2: Towards A Critical Data Practice*. Amsterdam University Press. [https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153](https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153)
