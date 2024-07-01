---
layout: note
type: note
title: Scientific Methods
---

# 1 - Philosophies of Correlation

## CORRELATION

Extent to which two features of the world tend to occur together.

COVARIANCE. Relationship between variation of two features.

$$
cov(x,y) = \sum_{i}^{n} \frac{(x_i - \mu_x)(y_i - \mu_y)}{n}
$$

CORRELATION COEFFICIENT. Covariance scaled by variability.

$$
corr(x,y) = \frac{cov(x,y)}{\sigma_x \sigma_y}
$$

Limitations of correlation coefficient:

1. Strength of association. Thus, it cannot be used descriptively in that manner nor to make predictions.
2. Nonlinearity. Correlation can only reflect linear relationships.

REGRESSION COEFFICIENT. Slope.

$$
\beta = \frac{cov(x,y)}{\sigma_x^2}
$$

## USES

1\. DESCRIPTION.

2\. PREDICTION.

For a prediction to be 'right' (on average):

1. The relationship must be linear.
2. The sample must be representative.
3. The forecast must be within our range of data.

3\. CAUSAL INFERENCE.

Requires the additional assumption of CETERIS PARIBUS, that all things are equal.

## CAUSATION

Change in one feature of the world results from a change in another feature of the world.

COUNTERFACTUAL DEPENDENCE:

1. Y occurs when X occurs.
2. Y would not have occurred in the counterfactual world where X did not occur.

Potential outcomes:

|                                    | $E[Y_1\|T=1]$                         | $E[Y_0\|T=0]$                           | $E[Y_1\| T=0]$                                                             | $E[Y_0\| T=1]$                                                             |
| ---------------------------------- | ------------------------------------- | --------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| Description                        | Average outcome <br> in treated group | Average outcome <br> in untreated group | Average outcome <br> in treated group <br> if they had <br> been untreated | Average outcome <br> in untreated group <br> if they had <br> been treated |
| Observable or <br> counterfactual? | Observable                            | Observable                              | Counterfactual                                                             | Counterfactual                                                             |

The FUNDAMENTAL PROBLEM of causal inference. $Y_1 - Y_0$ is unobservable. At best, we are able to measure AVERAGE CAUSAL EFFECTS.

Other problems:

1. Proximity. 'What is the cause of World War II' is unanswerable.
2. Unanswerable questions. It's impossible to answer what the effect will be on an individual, only for a population based on a representative sample.
