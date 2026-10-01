## Meaning of the Labels in the Ground Truths
+ ### Numeric labels (0, 1, 2, ...): Regular component
    - A regular component is assigned to a specific microservice, and the label indicates that microservice.
+ ### "C": Common component
    - A common component is shared by multiple microservices.
    - Therefore, in this paper, a common component considered by a microservice identification technique is counted as a Hit regardless of the microservice to which it is assigned. Common components not considered by the technique are excluded from both Hit and Considered.
+ ### "N/U": Unused component
    - An unused component _(i.e., dead code)_ is not exercised by the web app.
    - Thus, like a common component, an unused component considered by a technique is counted as a Hit regardless of its assigned microservice.

For Macro-F1 computation, considered common and unused components are grouped into an additional category.

## Why the Component Type Is Specified in the Ground Truths
In our approach, not only classes but also views and tables are considered as components. Therefore, the type of each component (class, view, or table) is specified in the ground truths.
