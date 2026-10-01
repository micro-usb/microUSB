# A Hybrid Behavioral and Semantic Approach to Identifying Microservices in Legacy Monolithic Web Applications

## Subject web applications
### [JPetStore](https://github.com/KimJongSung/jPetStore)

JPetStore is a complete pet store web application that demonstrates the structure of an e-commerce platform. It is built on Spring 3 and MyBatis 2.

### [JPetStore6](https://github.com/mybatis/jpetstore-6)

JPetStore6 is another version of JPetStore, built with MyBatis 3, Spring 5, and Stripes.

### [PetClinic](https://github.com/spring-projects/spring-petclinic)

PetClinic is a sample application for the Spring Framework, developed by SpringSource, that manages pet and veterinarian information. It is available in both the original and Thymeleaf-enabled versions.

### [ShoppingApp](https://github.com/manhduydl/Shopping-web-Jsp-Servlet)

ShoppingApp is a complete web application built with Servlet and JSP, without using AJAX.

### [DayTrader](https://github.com/WASdev/sample.daytrader7)

DayTrader 7 is an online stock trading system based on Java EE 7, using JSF, EJB, and JDBC.

## Project structure

### Ground truths
A ground truth for each subject web application is required to evaluate the performance of the proposed approach. The ground truths were created by web application experts.

#### JPetStore
| Label | Service             |
|-------|---------------------|
| 0     | Order service       |
| 1     | Account service     |
| 2     | Cart service        |
| 3     | Catalog service     |
| C     | Common component    |
| N/U   | Unused component    |

#### JPetStore6
| Label | Service             |
|-------|---------------------|
| 0     | Order service       |
| 1     | Account service     |
| 2     | Cart service        |
| 3     | Catalog service     |
| C     | Common component    |

#### PetClinic
| Label | Service             |
|-------|---------------------|
| 0     | Vet service         |
| 1     | Visit service       |
| 2     | Customer service    |
| C     | Common component    |
| N/U   | Unused component    |

#### ShoppingApp
| Label | Service             |
|-------|---------------------|
| 0     | Order service       |
| 1     | Account service     |
| 2     | Cart service        |
| 3     | Catalog service     |
| C     | Common component    |

#### DayTrader
| Label | Service                       |
|-------|-------------------------------|
| 0     | Benchmarking service          |
| 1     | Account service               |
| 2     | Portfolio service             |
| 3     | Quotes service                |
| 4     | System configuration service  |
| C     | Common component              |
| N/U   | Unused component              |

### Baselines
Our approach is compared with the following six baselines.
This folder contains the identification results of each baseline.

  - ### **MEM**
    + [backend](https://github.com/gmazlami/microserviceExtraction-backend)
    + [frontend](https://github.com/gmazlami/microserviceExtraction-frontend)

  - ### **[Bunch](https://github.com/ArchitectingSoftware/Bunch)**
  - ### **[Mono2Micro](https://github.com/rahlk/ASE21-Tutorial)**
  - ### **UseCaseDyn**
    S.-H. Kim, D. Jung, N. Mohd Ali, A. B. Md Sultan, and J. Oh, “Microservice identification by partitioning monolithic web applications based on use-cases,” J. Inf. Commun. Converg. Eng., vol. 21, no. 4, pp. 268–280, 2023.
  - ### **Str-DBV**
    S.-H. Kim and J. Oh, “Migrating monolithic web applications to microservice architectures considering dependencies on databases and views,” Proc. ACM SAC '25, Catania, Italy, pp. 1702–1711, Mar. 2025.
  - ### **UCSM**
    C. Yoo, S.-H. Kim, J.-H. Shin, N. Mohd Ali, A. B. Md Sultan, and J. Oh, “Migrating monolithic web applications to microservice architectures leveraging use case and component similarity,” J. Inf. Commun. Converg. Eng., vol. 23, no. 2, pp. 78–87, 2025.

### Model
This folder contains the models used in our approach to identify microservices. Each model reflects specific information about the web application.
- ### Behavioral
  The behavioral model consists of two models, which represent the execution of components for each use case.
  + **Execution Participation**: Whether each component is executed in each use case, represented by a value of either 0 or 1.
  + **Execution Rate**: The proportion of execution traces of each use case in which each component is executed.
- ### Semantic
  The semantic model represents the meaning of each component, which is obtained by semantically analyzing only the name of the component. This folder contains the cosine similarity between the semantic vectors of the components.
- ### Hybrid
  The hybrid model is a weighted linear combination of the similarity matrices of the execution-participation, execution-rate, and semantic models, normalized into [0, 1]. It is the final model used to cluster components in our approach. The weights for each web application are listed in the Readme.md of this folder.

### Results
This folder contains the experimental results presented in the Evaluation section.
