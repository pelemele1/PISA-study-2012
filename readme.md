# Investigaton of PISA study 2021
## Felix Deichsel


## Dataset
The dataset, that was PISA is a survey of students' skills and knowledge as they approach the end of compulsory education. This survey examines

* how well students have learned the school curriculum,
* how well prepared they are for life beyond school.

It can be downloaded here: (https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud507/pisa2012.csv.zip&sa=D&ust=1581581520574000)

Since the original dataset is too large, I worked with and reduced dataset, that only contains my variables of interest. The final dataset, that is investigated, consists of 17 columns. Those are:

* 2 columns of datatype ordered category, that contain the highest education of mother and father)
* 5 columns of datatype float64 (4 score columns and one, that contains the number of lessons with a parent)
* 10 columns of datatype category (columns giving information about country, OECD status, whether parents are at home, job status and birth country)


dtypes: category(12), float64(5)

## Summary of Findings
For the three test area math, reading and science the score distributions seem to be very similar. The average score in each area is in the range of 481 to 486 points, and the standard deviation is in the range of 98-101 points. This means, that about 68.2% of the students scored between 380 and 580 points in each test area. Furthermore, the combined score from math, reading and science, is also normal distributed. The mean is 1452 points and the standard deviation is 285,12 points. There is a strong correlation between the score in each of the three tested area

The scores of students strongly depends on the country the test was taken. The highest average scores in each test area were achieved in China-Shanghai. Furthermore the front places are held by primarily asian countries like China-Shanghai, Singapore, Hong Kong-China, Chinese Taipei, Korea, Japan, Macao. The countries, that took part, can also be divided in OECD and non OECD countries. The average combined score in OECD countries is about 1505 points, in Non-OECD countries only 1366 points. Also the spread is a larger: The standard deviation is about 294 points for Non-OECD countries and only 265 points for OECD countries.

Concerning the variables, whether mother and/or father are at home or not, its seems, like students perform at their best, when both parents are at home and worst, when no parent is at home. There is a big difference between both parents being at home (score is about 1465 on average) versus both paretns not being at home (score is about 1186 on average). When only one parent is at home, students perform better, if that parent is their mother.

Investigating the relation of score and job status of the parents, it seems, that the more both parents work, the higher the score of the student is.

Another parameter I was looking at was, whether the score is affected when student/mother/father are born in the country of test or not. Students, that were born in the country of test, perform better in reading and science than born abroad students. In math however they perform equally well. If the mother was born abroad, the students perform better in each subject, however with the biggest margin in math. The same is true in case of the father. A further investigation however revealed, that if both parents are born abroad, this effect vanishes. Only if one parental part is born abroad, the student outperforms.

Students seem to perform better, the better the combined education levels of both parents are. The best average performance is achieved, when both parents have education level 5A. Outperformance of female students compared to male students increases, the better both parents are educated.

Most students do not receive any additional lessons by their parents. The distribution is strongly right skewed and non-symmetric. with a maximum of 125220 at 0 hours, and nearly no cases with more than 15 hours. The number of hours spent with those lessons correlate negative with the students performance. In a certain way this is what one would expect, because only students, who need to get better receive extra lessons. Students perform on average 21.3 points worse per received lesson


## Key Insights for Presenatation
I will concentrante my presentation on the last two findings in the chapter before. 
Following changes were made:
Generally, I added proper x- and y-axis labels, for example I replaced 'math_score' with 'Math score'
I changed the color map to viridis for all heatmaps.
In some cases, i created a figure with subplots in order to get all necessary information on one sight.