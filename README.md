# ada-2020-project-milestone-p3-p3_act

### Title
Improving the performance and explainability of civil war onset predictive models

### Abstract
Our goal is to improve the predictive models proposed by the paper, as well as to explore the interrelation that exists between civil war and the economy, in particular GDP and GDP growth.

While the paper obtained decent predictive performance of civil war onset using random forest, we attempt to further improve the predictive performance with neural networks. The dataset is reasonably large and we believe it is possible that neural networks will outperform all other methods. We will use ROC plots and AUC scores to compare the performance of neural networks to the methods used in the article.

Besides the accuracy, the interpretability is also what we want our model to have. The paper states that the out of bag (OOB) observations can be used to determine some aspects of causality. However, we don’t think that the Random Forest model can really perform causal inference. For example, although the result shows that the GDP growth is the most important variable in the model, we don’t know if it is the bad performance of GDP leads to the civil war, or the civil war causes the decrease of GDP growth. In order to reach a more rigorous conclusion, we will do the following work:
- perform the causal inference and verify if the GDP, or GDP growth is a significant reason for the civil war. And we can know if the conclusions in the paper can really make sense.
- analyze the impact that a civil war has on a national economy, specifically on GDP and GDP growth. Considering only countries that experienced a civil war, we use panel data regression models to understand how GDP and growth change as a consequence of the civil war.

### Research Questions
- Can we create a model with even greater predictive power of civil war onset?
- What is the effect of GDP/GDP growth on Civil War onset?
- What is the impact of a civil war on the economy of a country, specifically GDP and growth?

### Proposed dataset
The civil war dataset (sambnisImp.csv) from the paper. This dataset already contains data on civil war and economic variables (GDP, GDP growth).

### Methods
We will utilize neural networks. The predictive powers of nerural neworks and the methods in the paper will be compared using ROC plots and AUC scores.

We will use the model of causal inference to show the relationship between GDP and Civil War onset. Because the causal inference on continuous treatment (such as GDP) may be different from the binary treatment cases. In order to get more explainable results, we choose to divide the data into two groups: high-gdp-group and low-gdp-group. Then we can match the data in two groups and compare them. Finally we can verify if the GDP or GDP growth really caused the civil war, as the paper says.

To understand the impact of civil war on the economy, we will only consider countries that experienced a civil war in the analyzed period. We will consider economic data (GDP and GDP growth) in the years immediately before and immediately after the civil war. We will carry regressions using econometric panel data methods, specifically a simple pooled cross section method, Fixed Effects and/or Random Effects (depending on characteristics of the data).

### Proposed timeline
12.4
- Reproduce the random forest’s ROCs and AUCs in the paper
- Divide the data into two groups
- Feature selection for the regression model; regression on independently pooled cross-sections across time 

12.11
- Implement a first neural network and compare the results
- Do the matching and balance the data in two groups
- Fixed Effects model

12.18 
- Finish hyperparameter tuning and report the final results
- Do the causal inference and show some conclusions
- Random Effects model; do the Durbin-Wu-Hausman test to check whether we should use Random Effects over Fixed Effects

12.23 
- Short video	

### Organization within the team
Each of the three parts is mainly led by one member of the group. At each stage, all the members cooperate on each task, under the guidance of the member responsible for each part, so that work is split equally.
- Neural network to improve civil war onset prediction: Tiannan Sha
- Isolating the effect of GDP on civil war onset: Chenyang Cao
- Impacts of civil war on the economy: Alessandro Fornaroli


### Questions for TAs (optional)
We have a question about the data matching between the treatment group and control group. In homework 2, we use the score which is obtained from logistic regression.However, what should we do to get this score in our cases?



### Contributions

The same as our organization within the team, each of the team member responsible for their own topic and write the data story of each question:

- Neural network to improve civil war onset prediction: Tiannan Sha
- Isolating the effect of GDP on civil war onset: Chenyang Cao
- Impacts of civil war on the economy: Alessandro Fornaroli



### Data story link

We choose to deploy our data story by using GitHub, and one can access our work by this link:  https://tiannansha.github.io/ada-data-story/

