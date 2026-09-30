# Hybrid Model

The hybrid model is a normalized linear combination of three models: the Execution-rate model (Behavioral), the Execution-participation model (Behavioral), and the Semantic model.

Each model is transformed into a component-to-component similarity matrix using cosine similarity, and the three matrices are combined as follows.

_M<sub>H</sub>_ = _w<sub>R</sub>M<sub>R</sub>_ + _w<sub>P</sub>M<sub>P</sub>_ + _w<sub>S</sub>M<sub>S</sub>_, where _w<sub>R</sub>_ + _w<sub>P</sub>_ + _w<sub>S</sub>_ = 1

Every element of _M<sub>H</sub>_ is then normalized into [0, 1] using min–max normalization.

The weights used in the hybrid model for each web application are as follows.

## Weights

| Web Application | _w<sub>S</sub>_ (Semantic) | _w<sub>P</sub>_ (Execution-participation) | _w<sub>R</sub>_ (Execution-rate) |
|-----------------|-------|-------|-------|
| JPetStore       | 0.55  | 0.35  | 0.1   |
| JPetStore6      | 0.525 | 0.225 | 0.25  |
| PetClinic       | 0.25  | 0.375 | 0.375 |
| ShoppingApp     | 0.35  | 0.15  | 0.5   |
| DayTrader       | 0.65  | 0.025 | 0.325 |
