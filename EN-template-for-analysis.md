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

![](Raw-Original-dataset-capture.png)

 

Here is a link to the googlesheets spreadsheet: https://docs.google.com/spreadsheets/d/16tJjQn6W34JQ_Rc1QmY7sKetsYflTDc6xKRWELXjo8k/edit?usp=sharing    


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

To prepare the dataset for analysis, I began by deleting all unnecessary columns and rows, keeping only five key columns that were most relevant to the story. This helped simplify the data and focus on what was most important. I then froze the first row to keep the column headers visible while scrolling, ensuring the data remained consistent and easy to follow. After that, I created filters for all rows, which made sorting and searching for specific information much easier. I also removed any duplicate rows to avoid repetition and maintain data accuracy. Using the “Find and Replace” function in Google Sheets allowed me to correct or update recurring entries efficiently. Once the structure was cleaned, I focused on trimming the dataset further by deleting rows that did not relate directly to the story. I was able to remove data that were not relevant to income, and age. This step was especially time-consuming since the dataset originally contained over 2,000 rows. I carefully went through each section, separating different variable groups to make the data clearer and more organized. After this process, the dataset was reduced to just over 200 rows, leaving only the information most relevant to the story and making it much easier to interpret and analyze.

![](Clean-data-table-capture.png)<br>

### 3.3. Exploratory Data Analysis (EDA)

We chose to look at the income and age differences between wards in downtown and suburban Ottawa because we noticed that they follow different trends and wanted to know why that might be. 

Something that stands out to me is that the population of age demographics of the wards in the suburbs is fairly consistent, while in downtown, they vary wildly, suddenly rising and then falling. A potential story here could be investigating the reasons that the number of people increases from ages 15 to 29 in downtown, then begins to decrease again, before settling at ages 45 and up (refer to figure 3).  

![](pie_charts.png)
*Figure 5: Pie charts showing the age demographics in the four wards*
The number of people in different income levels in downtown are similarly erratic, whereas the distribution is again consistent in the suburbs. We could look at if and why the stats generally seem to be more erratic in downtown wards, while the stats in suburban wards seem to be more steady (refer to figure 4).

![](pivot_table.png)
*Figure 5: Pivot table showing the age groups of the four wards*
## 4. Potential Story

Insert text here.

## 5. Conclusion

Insert text here.

## 6. References

Include a list of your references here. Please follow [APA guidelines for references](https://apastyle.apa.org/style-grammar-guidelines/references). Hanging paragraphs aren't required though.

**Here's an example:**

Bounegru, L., & Gray, J. (Eds.). (2021). *The Data Journalism Handbook 2: Towards A Critical Data Practice*. Amsterdam University Press. [https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153](https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153)
