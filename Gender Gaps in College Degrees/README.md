# Visualization of Gender Gaps in STEM, Liberal Arts, and other degrees
First, I am trying to figure out in which STEM major, fe/male gender dominates or they look even (as in there's not so much gap difference between genders).
Then, I am going to include all 17 degrees to show comparison as a whole.

## Data
Randal Olson, a data scientist at University of Pennsylvania, has cleaned the data containing the percentage of women's bachelor's degrees 
from 1970 to 2012. The data set is broken up into 17 categories of degrees. It is origianlly from [the Department of Education Statistics](http://nces.ed.gov/programs/digest/2013menu_tables.asp).

I will be using,
- percent-bachelors-degrees-women-usa.csv

## Findings

1)
Comparison on STEMs: Engineering, Computer Science, Psychology, Biology, Physical Sciences, and Math and Statistics
  - Degree that women dominate is psychology 
  - Degrees that men dominate are Engineering, CS, Physical Sciences, Math and Statistics
  - Degrees that show large gender gaps are Engineering, CS, Psychology
  - As years passed by, gender gaps are becoming smaller (more even) in Biology and Physical Sciences 
  - Gender gaps in Math and Statistics look almost even
  
2)
Comparison on 17 degrees: 
  - STEMs = ['Psychology', 'Biology', 'Math and Statistics', 'Physical Sciences', 'Computer Science', 'Engineering', 'Computer Science']
  - Liberal Arts = ['Foreign Languages', 'English', 'Communications and Journalism', 'Art and Performance', 'Social Sciences and History']
  - Other degrees = ['Health Professions', 'Public Administration', 'Education', 'Agriculture','Business', 'Architecture']
   
    - Degrees that men dominated are: Engineering, CS, Physical Sciences, Architecture. (3/4 in STEMs) 
    - Degrees that women dominated are: Biology, Psychology, Foreign Languages, Health Professions, English, Public Administration, Eduation, Communications and Journalism, Art and performance 
    - Degrees that showed an even gap are (almost no gap) : Social Sciences and History, Business, Agriculture, Math and Statistics 

## Conclusion
It is clear that while most STEMs are dominated by men, the rest of degrees are most likely to be dominated by women

##Improvement
An advice I received was:
I should try to make the code more efficient by using vector/array operations/DataFrame methods/helper functions from some of the libraries. As my codes include long loops, these can be replaced with one or two lines of succint codes using `cross_val_score` function to help readers read the lines of code better.

