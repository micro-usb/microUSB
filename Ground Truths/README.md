## The Meanings of labels "C" and "N/U" in the ground truths.
+ ### "C": Common component
    - A common component is a web component used in multiple microservices.
    - Therefore, in this paper, it does not matter which microservice the common component is allocated to by the microservice identification techniques.
+ ### "N/U": Not used
    - "N/U" _(i.e., dead code)_ indicates a component that is not used in the web app.
    - Thus, like the common component, this paper does not care about the assignment of unused components to microservices.

## The reason why view, table, and class are indicated for each component in the ground truth.
In our approach, we consider not only classes but also views and tables as components, so the type of each component is specified in the ground truth.
