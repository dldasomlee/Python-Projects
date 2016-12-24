#Natural Language Processing
I am trying to figure out how to convert written text to numerics and how to use those representation to intuit grammatical rules

##Data
In this project, [Arnaud Drizard](https://github.com/arnauddri/hn) used the [Hacker News](https://news.ycombinator.com/) API to scrape the data from 2006 to 2015
and I am grabbing 1,000 sample random data. 
- [stories.7z.csv](https://github.com/arnauddri/hn/blob/master/data/stories.7z)

Also, going to include only 4 columns below to make the learning simpler,
- submission_time 
- upvotes 
- url 
- headline 

##Findings
Used mean squared error as an error metric and achieved approx. 2324 which I don't consider it as a good error rate. 
Maybe, I can implement a few ways to reduce the error rate. For example,
- Use larger data set
- Use random forest or other machine learning algorithms
- Remove extra columns

I'll get back to this later... 
