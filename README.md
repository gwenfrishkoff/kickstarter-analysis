# An Excel-Based Analysis of Kickstarter Campaigns

## Overview of Project
Our client, Louise, has provided a set of data (***data-1-1-3-StarterBook.xlsx***) on kickstarter (crowd-funded) campaigns across a range of industries (e.g., music, theater, technology, games), countries (e.g., United States, Great Britain), and time periods, which can be summarized by quarterly and monthly launch dates. Louise has two broad aims:
	<ol>
	<li> Her primary (immediate) aim is to conduct a successful crowd-funded campaign to finance a play in the United States (U.S.).
	<li> A secondary (future) aim is to finance a musical production in Great Britain (G.B.).
	</ol>
### Purpose
To support our client aims, we conduct a series of analyses to identify factors make for a successful crowd-funding campaign, with a focus on factors leading to successful past campaigns in similar markets (i.e., theater in the U.S. and musicals in G.B.). 

## Analysis and Challenges
To analyze these data, we use MS Excel to organize, sort, analyze, and interpret the kickstarter data to reveal trends that can inform Louise's crowd-funding campaign.

The dataset presents a few challenges. 
	<ol>
  	<li> **Readability of Data** -- Some data in the original spreadsheet were not readable. For example, data in Columns I and J ("deadline" and "launched_at") were associated with Unix timestamps. To address this issue, we created Columns S and T ("Date_Created_Conversion" and "Date_Ended_Conversion") and populated these columns using the Excel =Date formula.
	<li> **Organization of Data** -- Column N ("Category_and_Subcategory") contained hierarchical data, i.e., data combining a parent category (industries, such as music, theater) and a subcategory (e.g., music/jazz, mussic/rock, theater/musical, theater/plays). To address this issue, we used the Text-to-Columns method in Excel to split Column N data into two separate columns, Columns Q and R ("Parent_Category" and "Subcategory").
	 <li> **Data Distribution (spread)** -- Some records contained outlier data that could affect statistical summaries. For example, we created a new category (Column O: "Percentage_Funded"), which contains average (mean) pledges (in USD). Two records, ID #2734 and ID #2243, were associated with very large Percentage_Funded values. These values were highlighted when we used Conditional Formatting to color-code Percentage_Funded (initially, they were the only two values to be color-coded blue, representing the upper half or 50th percentile (red was used to color-code the lower half of values). As a short-term solution (work-around), we edited the rule for conditional formatting, setting the the upper value ("Max Type") to the 90th Percentile. This resulted in more meaningful color coding, with roughly half of the Percentage_Funded values now shown in blue (vs. red). To represent statistical outliers in the data, we used a Box-and-Whisker plot ((***kickstarter_box_plot.png(***): statistical outliers are represented as isolated data points, far above the upper limit (whiskers) of the plot.
	 <li> **Complexity** -- The data represent a range of industries, time periods, and geographic locations. We used Filters, Pivot Tables (data subsets), and computed (descriptive) statistics to provide a simpler and more focused overview and analysis. We plotted the summary data using stacked bar charts (shown in 8 uploaded figures: (***kickstarter_chart_outcomes_GBtheater.png, kickstarter_chart_outcomes_UStheater.png, kickstarter_chart_outcomesXcategory_GB.png, kickstarter_chart_outcomesXcategory_US.png, kickstarter_chart_outcomesXlaunch_date.png, kickstarter_chart_outcomesXsubcategory_GB.png, kickstarter_chart_outcomesXsubcategory_GBtheater.png, kickstarter_chart_outcomesXsubcategory_UStheater.png(***).
	</ol>

### Analysis of Outcomes Based on Launch Date
Analysis results are summarized in the figure ***kickstarter_chart_outcomesXlaunch_date.png***. 


### Analysis of Outcomes Based on Goals


### Challenges and Difficulties Encountered

## Results

- We can draw two general conclusions about Outcomes based on Launch Date:
	<ol>
  	<li> Most successful theater campaigns began in the 2nd quarter (May & June), and campaign success tapered off steadily after June. 
  	<li> This trend appears to be industry-specific. For example, the trend lines for successful funding of technology campaigns were much more erratic (unpredictable) over time.
	</ol>


- The analysis of Outcomes based on Goals suggests two main conclusions:
	<ol>
  	<li> In general, failed Kickstarter campaigns were associated with higher fundraising goals than successful Kickstarter campaigns.
  	<li> However, the median and mean pledged amounts were lower for failed pledges, which suggests that additional factors (other than high fundraising goals) may explain why people did not ultimately fund projects.
	</ol>


- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
