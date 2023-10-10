# project-1_Group-5
Using data from the data.cms.gov we aim to determine the following questions on a state basis:

Data Sources and Methods

Our datasets come from https://data.cms.gov/

Once we determined our initial direction of examining hospital readmission rates we looked for data sets that we felt could have a relation.

We decided then to examine Timely and Effective Care, Outpatient Imaging Efficiency, Hospital Medicare Spending, and Healthcare Related Infections

Question 1:
Examine the correlation between state medicaid spending and readmission rates

Conclusion 1:    
    *See Visualization SIR_Spending_Readmission_correlation.png
    Lower 3 charts show Medicaide spending correlated with Hospitals with Outstanding(Above the National Average), Average, or Under Performing (Below National Average)

    The positively correlation between average and under performing hospitals indicates that as spending approaches the national average the readmission rates improve.

    However, we see in the Outstanding Hospitals a negative correlation. This would indicate a point of diminishing returns as once hospitals begin to outperform the national readmission rate average their spending effectiveness trends down.

Question 2:
Which states have the highest readmission rates / which states have the lowest readmission rates?

Conclusion 2:
    *See the Visualization Hospital_Performance_by_State.png
    1.We can see that the states with better performing hospitals with lowest readmissiion rates (compared to the National avreage) are Hawaii, Idaho, Washington, Maine and Utah.
    2.We can see that the states with Under performing hospitals with lowest readmissiion rates (compared to the National avreage) are Maine, New Jersey, Florida, Rhode Island and New York.
    3.All the States have majority of the hospitals under average performing category (are performing same as the National average)
    4.Four teritories American Samoa, Guam,Northern Marana Islands and Virgin Islands does not have enough data to compare with the other states.
From the available data the most of the hospitals falls under the average performance category, which is same as the national average.

Question 3:
Do hospitals with higher rates of associated infections have higher readmission rates?

Conclusion 3:
    *See Visualization SIR_Spending_Readmission_correlation.png 
    We can see that in all three charts SIR has a flat or slightly negative correlation to readmission rates.
    We can conclude that a hospitals SIR Rates are not strongly related to Readmission Rates.

Question 4:
Is there a connection between outpatient imaging efficiency score and readmission rates.

Conclusion 4:
    *See Visualization  Most_Efficient_States_to_Least_Efficient_States.png
    When we compare the from the merged_df:
    1. The top ten outstandig performaning states, there is a 80% efficient rate for the readmissions
    2. When compared to the top thirty states, this efficiency droped to 66.66%
    3. when the bottom ten states are compared, this efficiency is at 50%

There is no enough data to correlate the outpatient immaging and the readmission rate. The imaging efficiency does not have a strong relation to the readmission rate. 


Question 5:
Does timely and efficient care correlate to readmission

Conclusion 5:
    *See the visualizations scatter_discharge_readmission.png
    
    1. Merged two datasets: "Timely_and_Effective_Care-State.csv" and "FY_2023_Hospital_Readmissions_Reduction_Program_Hospital.csv" based on the 'State' column.
    2. Renamed certain columns for clarity and converted various date columns to datetime format. Additionally, converted these dates to ordinal for ease of correlation calculations.
    3. Checked for missing values in the important columns and examined the number of unique values present, ensuring data consistency.
    4. Converted certain columns like 'Score', 'Excess Readmission Ratio', 'Predicted Readmission Rate', 'Expected Readmission Rate', and 'Number of Readmissions' to numeric types, handling non-numeric data cautiously to avoid analysis errors.
    5. Calculated Spearman's rank correlation between 'Timely Care Start Date Ordinal' and 'Readmission Start Date Ordinal', revealing a correlation coefficient and p-value, trying to understand if there's any statistically significant association between the two variables.
    6. Calculated and interpreted the correlation between 'Score' and 'Excess Readmission Ratio' as well as 'Score' and 'Predicted Readmission Rate'. Found a very weak positive correlation in both cases, which suggests that there is almost no linear relationship between these variables.
    7. Discovered a weak negative correlation between 'Number of Discharges' and 'Excess Readmission Ratio', indicating that as the number of discharges increases, the excess readmission ratio slightly decreases.
    8. Visualized data through scatter plots for 'Number of Discharges' vs 'Excess Readmission Ratio' and 'Score' vs 'Expected Readmission Rate', providing a graphical representation of the correlations.
    9. Created boxplots for 'Score' and 'Excess Readmission Ratio' to identify any outliers present in these variables. Implemented the IQR method to detect and plot these outliers, which are crucial for understanding data points that deviate significantly from the rest of the data distribution.
Through this analysis, while some weak correlations were identified, the data doesn't show strong linear relationships between the examined variables. This suggests that other factors might be in play, and further, more analysis could be beneficial.

Final Conclusion:

Medicaid spending has a positive correlation for the average and under-performing hospitals. However, there is a negative correlation in the outstanding hospitals which indicates the spendings by the hospitals have less readmission rates. With the limited data available for us we were unable to find a correlation between the outpatient imaging and readmission rate.​ While larger states had lower readmission rates overall with the limited data there is no positive correlation between the timely and effective care and the readmission rate.​

​






