# School_District_Analysis

## Overview and Objective

The school district board has presented both school and student data (see resources folder) for analysis. The project involves analyzing school and student statistics with the main feedback being data on percentage pass rates for mathematics, reading and both of these subjects. In addition, the analysis requires summarized results based on a specific set of categories for example top and bottom performing schools, and outcomes based on budget and size, to name a few. However, there is evidence of tampering of reading and math grades for Thomas High School (THS) ninth graders. This dishonesty challenges the integrity of the state-testing standards and may have significant on the overall outcome of the analysis. Considering the analysis was already completed and summarized, the objectives of this report were:

* replace the grades for the above-mentioned school
* repeat the analysis to produce the following summarized outcomes: district summary, school summary, math and reading scores by grade, high and low performing schools, and scores by school budget, school size and school type.
* compare the outcome of the analysis before and after the grades were replaced

## Resources

* The data file used in the analysis is students_complete.csv and school_complete.csv
* Jupyter notebook

## Results

* How is the district summary affected?

	The results for the district summary before and after the data clean up is presented in the figures below. As can be observed, replacing the 9th grade data for THS does not have a significant impact on school district data. 

	Figure showing District Summary before data clean

	<img width="581" alt="DS before" src="https://user-images.githubusercontent.com/92636438/143724436-8927df4e-6425-48a2-82f0-6608a4f64878.png">

	
	Figure showing District Summary after data clean 

	<img width="577" alt="DS after" src="https://user-images.githubusercontent.com/92636438/143724438-cef9e4b1-5760-4ae3-8ece-df63e9a879fb.png">



* How is the school summary affected?

	The table below summarizes THS data output before and after the math and reading scores were replaced. As can be observed, the school summary was only signicantly impacted in the areas of % passing math, % passing english and overall percentage passing both subjects. The averages for THS for these two subjects was not affected by the data clean. 

                        Average math scores   Average reading scores   % passing maths   % passing reading    % Overall passing 
        Before Clean     83.4 	           83.5	                  93                  97                   91 
        After Clean      83.4                    83.9	                  67                  70                   65



* How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?


	By using the ranking function in pandas (shown in the figure below), it was observed that the tampered data had a significant impact on THS overall performance compared to other schools. This overall percent performance is based on both maths and reading have a score greater than or equal to 70%.
    
    	<img width="503" alt="Screenshot 2021-11-28 070156" src="https://user-images.githubusercontent.com/92636438/143766833-eaf7cdb9-2f84-4a05-b50f-7108dff9cfa7.png">

    
	Before the data was cleaned, with an overall passing percent of 91% THS ranked second for all the schools analyzed. 
	After replacing the 9th graders scores, with an overall passing percent of 65% Thomas High School ranked 8th for all the schools analyzed. 

	

* How does replacing the ninth-grade scores affect the following: #Math and reading scores by grade


	The following information is a comparion of the percent math scores for the different grades for THS. 

	       	         9th	10th	11th	12th
        Before Clean   83.6	83.1	83.5	83.5
        After Clean    nan	83.1	83.5	83.5


	The following information is a comparion of the percent reading scores for the different grades for THS.

                         9th	 10th	 11th	 12th
        Before Clean     83.7	 84.3	 83.6	 83.8
        After Clean      nan	 84.3	 83.6	 83.8


	The results is within expectations. The only difference between the scores is that under 9th graders which reflects a "NaN", as was changed in the analysis



* Scores by school spending

	Replacing the reading and maths score for THS with 'Nan' did not affect the school spending per student (budget per student). This is within expectations as the number of students nor budget did not change. Only the math and reading scores from the original was altered and therfore any analysis directly linked to these data would change. THS spending budget per student is approximately $638.00.



* Scores by school size

	THS is in the "Medium (1000-2000)" size bucket. From the data, replacing the 9th grade maths and reading scores did not affect the mean scores for this school range.  



* Scores by school type

	Scores by school type reamins unaffected by the data change.



## Summary

After the 9th grade scores for both maths and reading was replaced the analyzed output most significantly impacted is % passing math, % passing english, overall percentage passing both subjects, and THS overall performance (/ranking) compared to other schools.
