# DSAssignment1A

The program in assignment 1A tests if "hard" news discusses mostly positive or negative things about the world. 

I test this hypothesis using twitter data from 10 news organizations: 
* The New York Times
* The Washington Post
* Chicago Sun Times
* Los Angeles Times
* Fox News
* MsNBC
* CNN
* ABC News
* NPR News
* CBS Nws

The program (with code created by Pablo Barbera) first scrapes about 500 tweets from each of the news organizations, using getTimeline function. Subsequently, the program conducts sentiment analysis using lexicon of positive and negative words (from lexicon.csv file). It cleans the text of the tweets by dropping non-unicode characters, removes punctuation, and converts to lower case. Then it classifies the individual tweets as positive or negative and produces the difference. Finally, using the information, the program computers percentage of positive, negative, and neutral words. 

The program finds that 25 % of the tweets positive, 29 % negative, and 46 % neutral. 
Finally, I produce a pie chart that indicates the proportions.
