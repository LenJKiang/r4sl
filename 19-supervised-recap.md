# Supervised Learning Overview

At this point, you should know...

### Bayes Classifier {-}

- Classify to the class with the highest probability given a particular input $x$.

$$
C^B({\bf x}) = \underset{k}{\mathrm{argmax}} \ P[Y = k \mid {\bf X = x}]
$$

- Since we rarely, if ever, know the true probabilities, use a classification method to estimate them using data.

### The Bias-Variance Tradeoff {-}

- As model complexity increases, **bias** decreases.
- As model complexity increases, **variance** increases.
- As a result, there is a model somewhere in the middle with the best accuracy. (Or lowest RMSE for regression.)

### The Test-Train Split {-}

- **Never use test data to train a model.** Test accuracy is a measure of how well a method works in general.
- We can identify underfitting and overfitting models relative to the best test accuracy.
    - A less complex model than the model with the best test accuracy is **underfitting**.
    - A more complex model than the model with the best test accuracy is **overfitting**.
    
### Classification Methods {-}

- Logistic Regression
- Linear Discriminant Analysis (LDA)
- Quadratic Discriminant Analysis (QDA)
- Naive Bayes (NB)
- $k$-Nearest Neighbors (KNN)

- For each, we can:
    - Obtain predicted probabilities.
    - Make classifications.
    - Find decision boundaries. (Seen only for some.)

### Discriminative versus Generative Methods {-}

- **Discriminative** methods learn the conditional distribution $p(y \mid x)$, thus could only simulate $y$ given a fixed $x$.
- **Generative** methods learn the joint distribution $p(x, y)$, thus could only simulate new data $(x, y)$.

### Parametric and Non-Parametric Methods {-}

- **Parametric** methods models $P[Y = k \mid X = x]$ as a specific function of parameters which are learned through data.
- **Non-Parametric** use an algorithmic approach to estimate $P[Y = k \mid X = x]$ for each possible input $x$.

### Tuning Parameters {-}

- Specify **how** to train a model. This in contrast to model parameters, which are learned through training.

### Cross-Validation {-}

- A method to estimate test metrics with training data. Repeats the train-validate split inside the training data.

### Curse of Dimensionality {-}

- As feature space grows, that is as $p$ grows, "neighborhoods" must become much larger to contain "neighbors," thus local methods are not so local.

### No-Free-Lunch Theorem {-}

- There is no one classifier that will be best across all datasets.


## External Links

- [Wikipedia: No-Free-Lunch](https://en.wikipedia.org/wiki/No_free_lunch_theorem)
- [Do we Need Hundreds of Classifiers to Solve Real World Classification Problems?](http://www.jmlr.org/papers/volume15/delgado14a/delgado14a.pdf) - A paper that argues that No-Free-Lunch may be true in theory, but in practice there a only a few classifiers that outperform most others.

## RMarkdown

The RMarkdown file for this chapter can be found [**here**](12-classification-overview.Rmd). The file was created using `R` version 4.0.2.
