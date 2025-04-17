# House-price
House price prediction

Proposal Feedback: 
- since there are quite a lot variables in your dataset, and you’ve categorized them into several aspects, I suggest try PCA to aggregate the variables and see if the cluster align with your categorization. It would also be interesting to see how these aggregated PCs behave in the model (i.e. use PCs to estimate the target). Can you visualize how house prices change with each factor?
- How many data samples do you have in the dataset? I noticed that there are missing values in your dataset, what is the proportion of the missing values? How do you plan to handle those?
- Regarding "Since we have 79 variables, we will cut down the number," I might consider some of team judgement, pairwise correlations, permutation feature importance, and which variables Lasso retains as alpha increases.
- I might show the most interesting of plots of price vs. individual variables, e.g. scatterplot and simple regression model for a continuous feature or dual density plots of price vs. a categorical variable.
- Regarding "One hot encoding", will this work for a variable with many categories? Maybe read the scikit-learn user guide for "TargetEncoder", which uses average target values across a categories to encode an unordered categorical variable.
- Regarding RMSE, please put it in context, e.g. use some of mean, median, standard deviation, and range of prices (otherwise we won't know whether it is big or small). I'd also report and interpret R^2.
- If you use "mutual information", describe it briefly, as it's not a 451 topic.
- If location data include address, you might include a picture of of typical house or two, along with price. If location data include lat./long., and you might make a heatmap of price vs. location and tell us what characterizes expensive and cheap neighborhoods by studying Google Maps.
