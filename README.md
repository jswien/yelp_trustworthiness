# How Trustworthy Is This Yelp Review?
One of the challenges with using websites like Yelp to help you decide whether to go to a restaurant or not is that not all reviews tend to be trustworthy. Often, just based on reading the review one can see that the person writing it might be pickier than the average customer or might have just had a bad experience. My goal was to write a machine learning algorithm to pick out these types of reviews. 


To construct a labeled training set, I downloaded the freely available Yelp dataset (https://www.yelp.com/dataset/). From this dataset, I took only reviews from well reviewed business. For each reviews, I calculated the difference between the number of stars given and the mean of the reviews for the business. Reviews that significantly deviated from the mean were labeled as "untrustwory." 

To build the classifier, I first used a pretrained word2vec model to transform each review into a sequence of word vectors. Then, I used a 1D CNN with two convolutional layers to determine if a review was trustworthy or not.


