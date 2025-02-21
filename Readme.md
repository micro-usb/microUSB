# A Use Case and Semantics-Based Approach to Identifying Microservices in Legacy Monolithic Web Applications 

## Subject web applications 
### [JPetStore](https://github.com/KimJongSung/jPetStore)

It is a full web application in the form of a pet store, showcasing the structure of an e-commerce platform, built on Spring 3 and MyBatis 2.

### [JPetStore6](https://github.com/mybatis/jpetstore-6)

JPetStore6 is another version of JPetStore, built with MyBatis 3, Spring 5, and Stripes.

### [PetClinic](https://github.com/spring-projects/spring-petclinic)

PetClinic is a sample application by SpringSource for the Spring Framework, designed to manage pet and veterinarian information, with both original and Thymeleaf-enabled versions.

### [ShoppingApp](https://github.com/manhduydl/Shopping-web-Jsp-Servlet)

ShoppingApp is a full web application built with Servlet and JSP, without using AJAX.

### [DayTrader](https://github.com/WASdev/sample.daytrader7)

DayTrader 7 is an online stock trading system based on Java EE 7, using JSF, EJB, and JDBC.

## Project structure 

### Ground truths 
To evaluate the proposed technique's performance, a ground truth for each subject web application is required. The ground truth was generated by web application experts.

## JPetStore
| label | service          |
|-----------|---------------------|
| 0         | Order service       |
| 1         | Account service     |
| 2         | Cart service        |
| 3         | Catalog service     |
| C         | Common component    |
| N/U       | Not used            |


## JPetStore6
| label | service          |
|-----------|---------------------|
| 0         | Order service       |
| 1         | Account service     |
| 2         | Cart service        |
| 3         | Catalog service     |
| C         | Common component    |

## PetClinic
| label | service          |
|-----------|---------------------|
| 0         | Vet service         |
| 1         | Visit service       |
| 2         | Customer service    |
| C         | Common component    |
| N/U       | Not used            |

## ShoppingApp
| label | service          |
|-----------|---------------------|
| 0         | Order service       |
| 1         | Account service     |
| 2         | Cart service        |
| 3         | Catalog service     |
| C         | Common component    |

## DayTrader
| label | service          |
|-----------|-------------------------------|
| 0         | Benchmarking service          |
| 1         | Account service               |
| 2         | Portfolio service             |
| 3         | Quotes service                |
| 4         | System configuration service  |
| C         | Common component              |
| N/U       | Not used                      |


### Baselines 
Our approach is compared with the following four baselines.
This folder contains the identification results for each baseline.


  - ### **MEM** 
    + [backend](https://github.com/gmazlami/microserviceExtraction-backend)
    + [frontend](https://github.com/gmazlami/microserviceExtraction-frontend)
  
  - ### **[Bunch](https://github.com/ArchitectingSoftware/Bunch)** 
  - ### **[Mono2micro](https://github.com/rahlk/ASE21-Tutorial)** 
  - ### **UseCaseExec**
    S.-H Kim, D. Jung, N. Mohd Ali, A. B. Md Sultan, and J. Oh, "Microservice identification by partitioning monolithic web applications based on use-cases," J. Inf. Commun. Converg. Eng., vol. 21, no. 4, pp.268-280, 2023 

### Model 
This folder contains the models used in our approach for identifying microservices. Each model reflects specific information about the web application.
- ### Behavioral 
  The behavior model represents the execution status of components for each use case. The execution status is represented by a value of either 0 or 1.
- ### Semantic 
  The semantic model is a collection of vectors that represent the meanings of components. The proposed approach obtains the meaning of each component by semantically analyzing only the name of each component.
- ### Hybrid
  A Hybrid model combining the behavioral model and the semantic model is the final model used to cluster components in our approach.

### Results
This folder includes the experimental results used in the Evaluation section.
