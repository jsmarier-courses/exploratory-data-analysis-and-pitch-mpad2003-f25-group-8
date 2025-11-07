**November 6, 2025**<br>
**MPAD 2003A Introductory Data Storytelling**<br>
**Student's First Name & Last Name**<br>
**Presented to Jean-Sébastien Marier**<br>

# Exploratory Data Analysis (EDA) & Pitch

Use one hashtag symbol (`#`) to create a level 1 heading like this one.

## Foreword

For this assignment, you must extract data from a dataset provided by the instructor. You must then clean and analyze the data, create exploratory charts/visualizations, and find a potential story idea. Your assignment must clearly detail your process. You are expected to write about 1500-2000 words, and to include several screen captures showing the different steps you went through. Your assignment must be written with the Markdown format and submitted on GitHub Classroom.

I have been assigning different versions of this project to my digital journalism and data storytelling students for a few years now. Its structure was inspired by the main sections/chapters of [*The Data Journalism Handbook*](https://datajournalism.com/read/handbook/one/). This version was further inspired by the [Key Capabilities in Data Science](https://extendedlearning.ubc.ca/programs/key-capabilities-data-science) program offered by the University of British Columbia (UBC).

**Here are some useful resources for this assignment:**

* [GitHub's *Basic writing and formatting syntax* page](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [The template repository for this assignment in case you delete something by mistake](https://github.com/jsmarier/jou4100_jou4500_mpad2003_project2_template)

Did you notice how to create a hyperlink? In Markdown, we put the clickable text between square brackets and the actual URL between parentheses.

And to create an unordered list, we simply put a star (`*`) before each item.

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

To include a screen capture, use the sample code below. Your images should be saved in the same folder as your `.md` file.

![](import-screen-capture.png)<br>
*Figure 1: The "Import file" prompt on Google Sheets.*

**Here are examples of functions and lines of code put in grey boxes:**

1. If you name a function, put it between "angled" quotation marks like this: `IMPORTHTML`.
1. If you want to include the entire line of code, do the same thing, albeit with your entire code: `=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)`.
1. Alternatively, you can put your code in an independent box using the template below:

``` r
=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)
```
This also shows how to create an ordered list. Simply put `1.` before each item.

## 3. Understanding Data

### 3.1. VIMO Analysis

- The dataset comes from a questionnaire sent to 25% of households in Ottawa, so while it might not paint a complete portrait of the population, it is useful for identifying general trends.
<br>
- No missing variables in the columns we are interested in
<br>
- The sum of the population of each age group for each ward is equal to the total population of each ward +/- 10
<br>
![](age_sums.png)
*Figure 1: This table shows the populations of each ward, the number of people in different age groups, and the sums of all the age groups for each ward*
<br>
- The number of people in each age range follows trends and there are no outliers
<br>
![](VIMO_age_graph.png)
*Figure 2: This graph shows trends in the populations of different age groups in four wards*
<br>
- The sum of people in different total income levels with for each ward is equal to the number of people with total income in each ward +/- 10
<br>
![](income_sums.png)
*Figure 3: This table shows the populations of each ward, the number of people in different income levels, and the sums of all the income levels for each ward*
<br>
- The number of people in different total income levels for each ward follows trends and there are no outliers
<br>
![](VIMO_income_graph.png)
*Figure 2: This graph shows trends in the populations of different income levels in four wards*


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
