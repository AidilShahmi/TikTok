# Tiktok

Overview

The goal of this project was to develop a machine learning model that can be used to determine whether a video contains a claim or whether it offers an opinion.

Data Understanding

After reviewing the provided dataset, the variable  claim_status seemed particularly useful, given the client’s proposed project. The data team considered viewer engagement with each video in the claim and opinion categories. In order to understand viewer engagement, the data team considered the view count. The mean and median view count show the impact of each category of video; specifically, the mean and median view counts for both categories show the association between content (claim or opinion) and the video views. 


Modelling and Evaluation

The exploratory data analysis conducted from TikTok’s data team revealed many considerations for the classification model, including missing values, “claims” to “opinions” balance, and overall distribution of data variables. The analysis shows that there is a difference in number of views between TikTok videos posted by verified accounts and TikTok videos posted by unverified accounts. The team suggests moving forward and building a regression model on verified status. Based on the estimated model coefficients from the logistic regression, longer videos tend to be associated with higher odds of the user being verified. Other video features have small estimated coefficients in the model, so their association with verified status seems to be small. As a result, other video features besides video length do not seem to be associated with verified status. The data team built two tree-based classification models. Both models were used to predict on a held-out validation dataset, and final model selection was determined by the model with the best recall score. The final model was then used to score a test dataset to estimate future performance.

Conclusion

As noted, the model performed exceptionally well on the test holdout data. Before deploying the model, the data team recommends further evaluation using additional subsets of user data. Furthermore, the data team recommends monitoring the distributions of video engagement levels to ensure that the model remains robust to fluctuations in its most predictive features.




 




