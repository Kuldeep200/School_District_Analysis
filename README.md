# School_District_Analysis
## Overview 

The purpose of this project, was to to perform an analysis on the reading and math scores for the high schools in a school district. 



#Results: Using bulleted lists and images of DataFrames as support, address the following questions.

How is the district summary affected?
BEFORE cleaning up the data

Average Math Score = 79.0
Average Reading Score = 81.9
% Passing Math 75
% Passing Reading 86
% Overall Passing 65


 And After cleaning up the data

Average Math Score = 78.9
Average Reading Score = 81.9
% Passing Math 74.8
% Passing Reading 85.7
% Overall Passing 64.9

How is the school summary affected?
BEFORE DATA CLEANUP
top_schools = per_school_summary_df.sort_values(["% Overall Passing"], ascending=False)

top_schools.head()
Thomas High School's Overall Passing was and placing second 90.94

AFTER DATA CLEANUP

Thomas High School's % Overall Passing was 65, placing eight


How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
student_data_df.loc[
    (student_data_df["school_name"] == "Thomas High School") & 
    (student_data_df["grade"] == "9th"), "reading_score"] = np.nan

student_data_df.tail()

Thomas high school, before removing the false 9th grade numbers from the dataset, had an overall passing percent of over 90.94%, but after the 9th grade was removed, the overall passing percent dropped to 90.63%.




How does replacing the ninth-grade scores affect the following:

Math and reading scores by grade
Math and Reading Scores from Thomas High School 9th Grade set to "nan" and equivalent to 0.
Math and Reading Scores from Thomas High School 9th Grade means all of them failed (set to fail for analysis).
Doing that, the only significantly score affected was minimal in a very small in quantity.
Student count() Before THS Cleanup was: 1635
Student count() After THS Cleanup was: 1174

Scores by school spending
Thomas HS is in the spending bucket "$630-644"
Student count() Before THS Cleanup was: 1635
Student count() After THS Cleanup was: 1174

Scores by school size
Thomas High School was resevered on Spending Bin "$630-644

Scores by school type



#Summary
i see most of the changes were in  analysis that were in district analysis and the school summary. In the district summary, the district totals was better off without the thomas high school 9th grader grades with marginally higher passing percentages. Secondly, In the per school summary, the passing percentages for thomas high school dropped some when just summarizing the 10th-12th grade scores.



