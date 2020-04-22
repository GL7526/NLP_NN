# NLP_NN

# ** Readme to be updated soon **

<!--

# Predicting Drug Ratings Based On Reviews
This project aims to predict the rating of a review on a drug, based on the text in the review.
The data comes from online pharmaceutical review sites and contains information such as the review and rating of the drug, and condition it was used for. The data can be found in the following link: http://archive.ics.uci.edu/ml/datasets/Drug+Review+Dataset+%28Drugs.com%29
This project was an opportunity to delve into natural language processing by building a multi class classifier that uses English text as the input.

<br>

- [Project Goal](#ProjGoal)
- [Cleaning Data](#Preprocessing)
- [EDA](#EDA)
- [The Model](#Model)
- [Takeaways](#Takeaway)

<br>

## Project Goal <a name = 'ProjGoal'></a>
The goal of this project is to predict the rating of a drug review based on the text.
<br>

## Preprocessing/Data Cleaning <a name = 'Preprocessing'></a>
Cleaning text data is slightly different from cleaning typical numerical data. The inputs are strings that we want to extract information from. For this set of data, I used nltk's TweetTokenizer to tokenize the data. The benefit of using TweetTokenizer as opposed to nltk's word_tokenize is that the former doesn't split words by apostrophes so a word like "didn't" stays as "didn't" instead of becoming two words "did" and "n't". Now that the data is tokenized, the stop words and punctuation can then be removed. The words were then lemmatized according to their parts of speech to reduce dimensionality and also because I saw no loss of meaning from considering words like "jump" and "jumping" the same, at least here. Finally, I used keras' Tokenizer to transform the data into a matrix of tf-idf values of each word.

<br>
<br>

## EDA <a name = 'EDA'></a>
Some interesting findings come from the EDA. One of the 


## The Model <a name = 'Model'></a>


<br>
<br>

## Distribution Of Features To Amount Of Good Tips
The feature that provides the most information is the trip's total cost. Below shows a scatterplot of the total price categorized by whether the tip was good or not:
<br>
<img src = "graphs/tip_well_vs_total.png" width = 550>
<br>
We can see that there is something like a cut off of almost $4 until yellow taxi drivers even get a good tip. 
<br>

### Trip Duration
<img src = "graphs/goodtip_per_duration.png" width = 550>
<br>
For trip duration, the amount of tips that are good seem to decrease as trip duration increases. This kind of shows us that yellow taxi drivers have a higher chance of getting a good tip if the trip is fast. This may be because the passenger would be less likely to give a good tip if the trip is so long that they're going to be late.

### Trip Distance
<img src = "graphs/dist%20of%20distance%20for%20good%20tips.png" width = 550>
<br>
For trip distance, there proportion of tips that are good tips go up and then go down. This might show that if the trip is too short, such as a couple of blocks, then the passenger is less likely to give a good tip.

## Takeaways <a name = "Takeaway"></a>
The data tells us that to get a good tip, drivers should avoid trips that are too short, such as a couple of blocks, and should avoid traffic to make the trip as fast as possible. Although yellow taxi drivers probably can't decline passengers, this data can still be used for drivers who work under companies such as Uber or Lyft, where they can decline rides.
One might also think that some information such as the trip duration and total cost of the trip can't be found until the ride is over, but this information can be estimated from wherever the passenger selects the location they want to go to. An experienced driver might be able to estimate it on the spot pretty fast. <!-- an even better idea is to integrate these calculations in the app or something and recommend/prioritize which passengers to take for each active driver -->
