# StudentPerformanceFactors
Train and optimize 3 AI models to make predictions on student exam scores based on several performance factors using open source kaggle dataset.  

Set out to uncover which behavioral and socio-demographic characteristics most strongly influence students’ exam outcomes. Leveraging the publicly available Student Performance & Behavior Dataset from Kaggle, which encompasses a range of features—from parental education level and teacher quality to time spent studying and distance from home—we focused on explaining variance in the Exam_Score target variable ​. Our central research questions were: Which factors exhibit the strongest linear and non-linear relationships with exam performance? And how do different modeling approaches compare in predictive accuracy and robustness?

Linear Regression is fastest and most transparent but breaks badly in the presence of outliers.


Decision Trees are naturally more robust to extremes, but a single tree can overreact to outliers if you don’t constrain its depth.


Random Forests combine many trees to mute the effect of any single outlier, giving you the best outlier-handling of the three—at the cost of extra computation and reduced interpretability.

a lone decision tree can “go off the rails” around outliers because it (1) makes hard splits that an outlier can hijack, (2) has no ensemble-averaging to dampen that effect, and (3) tends to over-fit noisy points unless carefully pruned or depth-limited.

Systematic exploration of combinations
5-fold CV ensures each candidate is evaluated robustly
R² scoring aligns with our regression objective
