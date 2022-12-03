---
name: IS 445 - Final Project Part3 - Group 66
tools: [Python, HTML, vega-lite, Jekyll]
image: assets/pngs/inc5000.png
description: This is the  part 3 of the IS 445 final project created by Group 66
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---
![](/assets/pngs/inc50002019.png)
# <center> The Stories Behind The Fastest 5000 Growing Companies in The U.S.</center>
<br/>

#### <center> Group 66 - Tianci Zheng, Yiqing Li </center>
<br/>

## 1. Introduction
"How to succeed" is always the most frequent question every company asks. And we want to help companies answer this question by learning from successful ones. So, we decided to utilize Inc.5000 in 2019, which listed the 5000 Fastest Growing Private Companies in the United States at that year, to figure out the hidden stories based on their data. We hope that our analysis could help people better understand the key factors as well as the common elements a successful company possesses.

The [data file](https://raw.githubusercontent.com/yiqingl8/yiqingl8.github.io/main/cleaned_inc5000-2019.csv) comes from [INC 5000 - 2019](https://data.world/aurielle/inc-5000-2019) on data.world which is orignially from Inc.com.
We performed a series of data processing and cleaning that can be found in our [Analysis](https://github.com/yiqingl8/yiqingl8.github.io/blob/main/python_notebooks/finalprojectpart3_Analysis_Group%2066.ipynb) Jupyter Notebook.

## 2. One Central Interactive Dashboard Visualization


Firstly, we would like to create an [interactive dashboard](https://raw.githubusercontent.com/yiqingl8/yiqingl8.github.io/main/assets/json/centraldashboard.json) (Fig 1) that reveals precious geographic and monetary information regarding those fastest 5000 companies.

<vegachart schema-url="{{ site.baseurl }}/assets/json/centraldashboard.json" style="width: 100%"></vegachart>
<center>Fig 1: Central Interactive Dashboard </center>
<br/>

There are two components in our dashboard. The left part is a heatmap visualization that plots out the company industries and the states they reside. The different color shows the different amount of companies in each combination. 
The chart horizontally shows the business types per state and their count. And looking at the grid vertically can find the distribution of various industries in the United States. 

As for the right bar chart, the x-axis is the length that companies have been on the Inc 5000 list, and the y-axis is an aggregate measure of the average revenue. The chart not only shows the financial status of companies but also depicts potential relationships between the revenue and the total time length. 

Looking at the dashboard holistically provides great flexibility for people to find different but detailed information based on their needs. For example, people who are only interested in companies in IL and IN can select these two rows, and the bar chart will vary to show the specific performance


## 3.Contextual Visualizations
In addition to the dashboard, we also found other columns in the dataset valuable and researched online to find contextual contents that better serve our topic - helping people understand successful companies.
<br/>

### 3.1 Total revenue by industry

One direction we focused on was revenue. Revenue is always an important measure to a company and can reflect many facets, such as operations and financial status. We created a [horizontal bar](https://raw.githubusercontent.com/yiqingl8/yiqingl8.github.io/main/assets/json/contextual_1.json)(Fig 2) chart by calculating the total revenue based on the industry to find the top sectors that make the most money. 
As shown in Fig 2, we can see that Health, Consumer Products & Services, and Construction were the industries with the highest revenue in 2019. And the Health section even made above 38,000 million, which was twice as much as second place. The graph shows us which industries are promising and which ones are not. 
It provides a very good reference for people and entrepreneurs to determine the future direction of their companies.



<vegachart schema-url="{{ site.baseurl }}/assets/json/contextual_1.json" style="width: 100%"></vegachart>
<center>Fig 2: Total Revenue by Industry in 2019</center>
<br/>

Meanwhile, we found a treemap visualization (Fig 3)，created by Gautam Anand <sup>(1)</sup>，that 
also represents industry segments and their revenue. The chart's data are from Inc 5000 list in 2014. 
Based on the graph, we can tell that the Health, Energy, and IT Services industries earned the most in 2014, and their gross revenue was around 20,000 million. Other remarkable industries include Business Products & Services, Financial Services, Construction, and Real Estate. Additionally, we can discover the industry and economic trends and changes in the last few years by comparing Fig 3 with Fig 2. Health is always the leading role among all other sectors, and it outperformed others significantly in 2019. IT and Energy are seriously declining as they went from the top five to below the tenth. Overall, the growth of many industries is not stable, and people should be cautious when determining the industry. 

![](/assets/pngs/industryandrevenue.png)
<center>Fig 3: Total Revenue by Industry in 2014</center>
<br/>


### 3.2 Average Employee Count

Another aspect we worked on was the employee. 
We have seen much news regarding layoffs in famous companies these days, and we think it is necessary to help people learn from fast-growing companies about their strategies in employment. Analyzing the trend of employee count can achieve the purpose.
So, We created another [line chart](https://raw.githubusercontent.com/yiqingl8/yiqingl8.github.io/main/assets/json/contextual_2.json) (Fig 4) to show the average number of employees for companies founded at different times. 
According to the above figure, there is a declining trend which is reasonable as newly established companies tend to have fewer employers. An interesting finding is that most companies have a total number of employees between 100 and 400. We believe this range reflects the number of employees a healthy growing company should maintain. Therefore, people can rely on this interval to judge if they need to control the employee size or continue hiring for faster development.


<center><vegachart schema-url="{{ site.baseurl }}/assets/json/contextual_2.json" style="width: 100%"></vegachart></center>
<center>Fig 4: Average Employee Amount for Companies founded within 30 years </center>


## 4.Conclusion
To conclude, our project utilizes the dashboard to show the distribution of different industries in different states and their financial performances. We also plotted gross revenue and employment trend, aiming to give better insights into the most successful growth companies in the United States. We hope our work can benefit entrepreneurs who would like to learn from others and better develop their companies.

## 5. Citation
1. Anand, G. (2017, January 10). INC. 5000 Companies. Tableau Public. https://public.tableau.com/app/profile/gautam1546/viz/INC_5000Companies/INC_5000CompaniesandRevenue



<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/yiqingl8/yiqingl8.github.io/main/cleaned_inc5000-2019.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/yiqingl8/yiqingl8.github.io/blob/b07ddd594ef1a68bb1816462c4cbdd5d63a34d3c/python_notebooks/finalprojectpart3_Analysis_Group%2066.ipynb" text="The Analysis" %}
</div>
