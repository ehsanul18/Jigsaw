# Abstract

The online world has opened the doors to many possibilities. Everyone is free to express their thoughts and ideas. Everyone can give their opinions on topics and it is there for the world to see. However, people with negative mentalities have also made their place in this vast open world. For example, when someone meets another with an oposing idea to their own, they do not hesitate to make hurtful or toxic comments to the person who has the varying idea. This is just one of many example. Hence, for this case, we want to recognize any toxic comments made against any individual based on their gender, religion, etc. 

# Methodology

The goal is to detect whether a comment made is toxic or not. We are supplied with the train and test csv files. For the train dataset, the features or columns that was of our concern was the "comment_text" and "target". 

At first, there was the creation of the "target_class" from the "target" column. The values where it was more than 0.5 were converted to 1 and anything less than that was 0. After that, there was the checking of the amount of 0's and 1's in class. 1 signifies toxicity whilst 0 signifies non-toxic values. 

Then, there was the creation of a function to clean the comments. This meant removal of numeric values, stopwords, punctuation, lemmatization. After that, TfidfVectorizer was applied to those comments with a toxicity of over 20%. Then, the training values were split to apply logistic regression and multinomial Naive Bayes. 

# Result Analysis

After the values were ready, the two models were applied. The AUC values were calculated. Higher AUC values indicates the ability of the model to classify models to be better. Among the two models, it was logisitic regression with the higher AUC values. 

# Conclusion

This is a simple implementation applied on the text data and there is definite room for improvement using neural networks which for me at this point in time is difficult to apply due to my lack of knowledge regarding that topic. 
