# DSAssignment1
Coverage of budget deficits in the NY Times:

For this assignment, I use the NY Times API (http://developer.nytimes.com/docs/read/article_search_api_v2) to create a monthly time series of coverage of budget deficits issues. 

My goal is to generate frequency of NY Times mentioning U.S. federal budget deficit for each month of Fiscal Year 2013. I chose this range because I anticipate that there would be a surge of articles in November 2012 and December 2012 when the federal government was in the midst of “fiscal cliff” negotiations, and also in January 2013, immediately after the American Taxpayer Relief Act (ATRA) of 2012 was passed on January 2, 2013.

In file “Assignment 1C.py,” I carefully chose to implement nine separate searches, three for each of “federal deficit,” “federal budget deficit,” and “U.S. deficit,” since a simple search for “budget deficit” yielded results that discussed state-based, rather than federal budgets. I had to search three times for each of the keyword combinations because NY Times API outputs 10 most relevant search results on its page “0” and since I wanted at least 30 items per search, I had to conduct separate searches to also get results from pages “1” and “2.”

Next, a series of steps involve merging results from three searches per one keyword combination from different pages, and then merging the results from the searches with different keyword combinations, but only after removing potentially duplicate search results. 

Next, the code extracts all occurrences of “year-month” combinations using regular expressions for the date. Then it calculates frequency of each year-month combination.  After converting the result into dictionary format, the code outputs the year-month/frequency combination into CSV file “Assignment1Cfinal.csv.”

I move to R, file “Assignment1CPart2R.R,” to plot time series of the results, using “Assignment1Cfinal.csv,” and outputting the graph in file “Frequency Plot.jpeg.” The plot shows the predicted surge in articles on federal budget deficit in November and December of 2012, and January of 2013.  Could it be because of “fiscal cliff” negotiations?

The second part of “Assignment 1C.py” file adds a “fiscal cliff” argument to “budget deficit” argument in the NY Times API search, completes the same steps as above, then outputs file “Assign1CfiscalcliffFinal.csv.” Now, using the latest file, “Assignment1CPart2R.R” outputs the “Fiscal Cliff Plot.jpeg,” file also exhibiting a surge of observations around November and December 2012, then tapering off after ATRA was passed, and no longer present after June of 2013.  I conclude that fiscal cliff negotiations were associated with a greater frequency of budget deficit discussions in New York Times, reflecting similar preoccupation in the Federal Government.
