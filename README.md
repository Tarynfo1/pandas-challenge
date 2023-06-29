# pandas-challenge
Module 4 homework PyCity Schools challenge

## Acknowledgements

The code implementation for the groupby function and using zip was provided by https://www.statology.org/pandas-groupby-count-with-condition/. The provided code snippet helped in understanding where the code was failing to calculate correctly.

### Code Snippet

``
' ...

'Summary_Table = school_data_complete[school_data_complete['maths_score'] >=50].groupby(['school_name'])
'School_Passing_Maths = [(i/j)*100 for i,j in zip(Summary_Table.maths_score.count(), School_Total_Students)]
'Summary_Table = school_data_complete[school_data_complete['reading_score'] >=50].groupby(['school_name'])
'School_Passing_Reading = [(i/j)*100 for i,j in zip(Summary_Table.reading_score.count(), School_Total_Students)]
'Percent_Overall_Passing = [(i+j)/2 for i,j in zip(School_Passing_Maths, School_Passing_Reading)]

' ...


The insights and code helped enhance the functionality and efficiency of the assignment. 

The code implementation for creating a series for each year level by score was assisted by AskBCS Mohamed. The provided code snippet helped in fixing an error where only 0 was populating the column.

### Code Snippet

``
' ...

'Create a series for each year level  by score

'year_9 = school_data_complete[(school_data_complete["year"] == 9)]
'year_10 = school_data_complete[(school_data_complete["year"] == 10)]
'year_11 = school_data_complete[(school_data_complete["year"] == 11)]
'year_12 = school_data_complete[(school_data_complete["year"] == 12)]

' ...

'The insights and code helped enhance the functionality and efficiency of the assignment. 


The code implementation for cleaner formatting was assisted by https://www.geeksforgeeks.org/applying-lambda-functions-to-pandas-dataframe/. The provided code snippet helped in using this as a template for my own formatting.

### Code Snippet

``
' ...

'area_summary_df['Total Students'] = area_summary_df.apply(lambda x: "{:,.0f}".format(x['Total Students']), axis=1)
'area_summary_df['Total Budget'] = area_summary_df.apply(lambda x: "{:,.0f}".format(x['Total Budget']), axis=1)

' ...

'The insights and code helped enhance the functionality and efficiency of the assignment. 