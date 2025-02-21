# Method of Selecting Results for Each Model-Based Approach

### Behavioral model results

For each behavioral model, our microservice identification method was performed 31 times, and the median accuracy was used to evaluate performance.

### Semantic model results

For each behavioral model, our microservice identification method was performed 31 times, and the median accuracy was used to evaluate performance.

### Integrated model results

A linear combination of semantic and dynamic models was used.

+ ### How to choose the alpha (_a_) value used in the integrated model of each app.

1) We generated 31 outcomes for each of the 20 alpha values evenly distributed between 0 and 1.
2) The accuracy for a particular alpha (_a_) value was the median of the results obtained from 31 repetitions using that alpha.
3) We evaluated the performance by selecting the alpha value with the highest accuracy among the 20 alpha values.


