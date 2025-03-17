# STA 141A Final Project: Predicting Decision Outcomes from Neural Activity in Mice

This repository contains the code and data for my final project in STA 141A. The goal of this project is to investigate whether neural activity and visual stimuli can predict decision outcomes (success or failure) in mice. By integrating neural firing rate data with behavioral metrics from multiple sessions, I developed and evaluated predictive models that shed light on how neural signals relate to decision-making.

Project Overview
Objective:
Explore the relationship between neural activity (recorded as spike trains) and decision outcomes, and build predictive models based on these neural features.

Data Source:
The dataset is derived from experiments originally collected by Steinmetz et al. (2019) during a visual decision-making task with varying contrast levels (0, 0.25, 0.5, 1). This analysis focuses on 18 sessions from four mice (Cori, Frossman, Hence, and Lederberg).

Key Variables:
Independent Variables:
contrast_left, contrast_right: Visual stimulus contrast levels.
brain_area: The brain region where spikes were recorded.
Dependent Variables:
spike trains: Neural firing activity (timestamped spike data).
feedback_type: Trial outcome (success: 1, failure: -1).

Hypotheses:
Neural activity predicts trial outcomes.
Stimulus contrast influences decision accuracy.
Different brain regions contribute differently to decision-making.

Model Testing Summary
I evaluated different predictive models using the original neural features. Here is a brief summary of the results on the test data:

Logistic Regression: 72.56% accuracy
Lasso Regression: 72.56% accuracy
Decision Tree: 72.56% accuracy
Gradient Boosting: 72.56% accuracy
k-Nearest Neighbors: 69.78% accuracy

These results suggest that the underlying predictive signal in the neural data is modest. Logistic regression, lasso, decision tree, and gradient boosting converge on similar performance, which implies that the relationship between the features and the outcome may be largely linear or that the current feature set captures a common baseline pattern. The slightly lower performance of k-nearest neighbors indicates that distance-based methods might be more sensitive to local noise in a high-dimensional space.

Conclusion

Data Integration & EDA:
I combined data from 18 sessions into one comprehensive dataset and explored neural and behavioral variables. The EDA revealed that while overall neural firing patterns are similar, subtle differences exist between trials with and without stimulus.
PCA:
PCA on neural features indicated that the main sources of variance are driven by factors other than trial outcome. The lack of clear separation in the PCA plot suggests that additional feature engineering may be necessary to better capture outcome-related differences.
Model Testing:
Multiple models were tested using the original neural features. The similar accuracy of 72.56% across several models suggests that even simple linear models capture the available predictive signal, though there is room for improvement through further refinement of features.
Final Thoughts:
Although the current analysis shows a moderate ability to predict decision outcomes based on neural activity, future work should focus on further refining the feature set and exploring advanced modeling techniques to improve predictive performance and deepen our understanding of the neural mechanisms underlying decision-making in mice.

Acknowledgements
I used generative AI (Gemini and ChatGPT) to help debug code, test different models, and guide my analysis.
This was my first full data science project, and it has been an invaluable learning experience.
Thank you to STA 141A for an engaging and informative course!
