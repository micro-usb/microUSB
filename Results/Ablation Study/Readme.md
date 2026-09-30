# Ablation Study

To evaluate the contribution of each model, four variants were compared.

| Variant | Models used |
| --- | --- |
| Semantic | Semantic (_S_) |
| Sem.+Part. | Semantic (_S_) + Execution-participation (_P_) |
| Sem.+Rate | Semantic (_S_) + Execution-rate (_R_) |
| Proposed | Semantic (_S_) + Execution-participation (_P_) + Execution-rate (_R_) |

### Method of Selecting Results for Each Variant

The hybrid similarity matrix is a linear combination of the selected models, _M<sub>H</sub>_ = _w<sub>R</sub>M<sub>R</sub>_ + _w<sub>P</sub>M<sub>P</sub>_ + _w<sub>S</sub>M<sub>S</sub>_, where the weights of unused models are 0.

+ ### How to choose the weights (_w<sub>S</sub>_, _w<sub>P</sub>_, _w<sub>R</sub>_) of each app.

1) Each weight was varied from 0 to 1 in steps of 0.025, and only combinations satisfying _w<sub>S</sub>_ + _w<sub>P</sub>_ + _w<sub>R</sub>_ = 1 were used.
2) For each weight combination, our microservice identification method was performed 31 times, and the median accuracy was taken as the accuracy of that combination.
3) We evaluated the performance by selecting the weight combination with the highest accuracy.

### Evaluation Metrics

Accuracy and Macro-F1 were used.

+ Common and unused components (Ground Truth = -1) are counted as Hit regardless of their predicted cluster.
+ For Macro-F1, common and unused components were grouped into an additional category, and the F1-scores of all ground-truth microservices and the additional category were averaged.

### Ablation Study.xlsx

+ One sheet per web app (JPetStore2, JPetStore6, PetClinic, ShoppingApp, DayTrader).
+ Each row is a component of the ground truth, in the same order as the ground-truth file.
+ Columns show the ground-truth microservice and the microservice identified by each variant (cluster numbers mapped to the ground-truth labels).
+ The last two rows show the Accuracy and Macro-F1 of each variant.
