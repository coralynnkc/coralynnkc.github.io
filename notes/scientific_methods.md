---
layout: note
type: note
title: Scientific Methods
---

# 1 - Philosophies of Correlation

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

# 2 - Always Compare

Correlation does not imply causation.

SELECTING ON THE DEPENDENT VARIABLE. Including observations only with particular outcomes.

# 3 - A Useful Equation

Estimate = Estimand + Bias + Noise

- ESTIMATE. What we see in the data. Sample statistic.
- ESTIMAND. What we are interested in knowing about. Population parameter.
- BIAS. The causal inference problem. Errors for systematic reasons.
- NOISE. The statistical inference problem. Errors because of chance.

## POTENTIAL OUTCOMES

AVERAGE TREATMENT EFFECT. ATE.

$$
E[Y_{1i}-Y_{0i}]
$$

AVERAGE TREATMENT EFFECT ON THE TREATED. ATT.

$$
\bar{Y}_{1, T=1} - \bar{Y}_{0, T=1}
$$

AVERAGE TREATMENT EFFECT ON THE UNTREATED. ATU.

$$
\bar{Y}_{1, T=0} - \bar{Y}_{0, T=0}
$$

For ATE = ATT: Expected outcomes for the treated subjects in the counterfactual where they were untreated are the same to the untreated subjects.

$$
\bar{Y}_{1, T=1} - \bar{Y}_{0, T=0} = \bar{Y}_{1, T=1} - \bar{Y}_{0, T=1} \rightarrow \bar{Y}_{0, T=0} = \bar{Y}_{0, T=1}
$$

For ATE = ATU: Expected outcomes for the untreated subjects in the counterfactual where they were treated are the same to the treated subjects.

$$
\bar{Y}_{1, T=1} - \bar{Y}_{0, T=0} = \bar{Y}_{1, T=0} - \bar{Y}_{0, T=0} \rightarrow \bar{Y}_{1, T=1} = \bar{Y}_{1, T=0}
$$

# 4 - BIAS & NOISE

## BIAS

CONFOUNDER. Extraneous variable that directly affects both the treatment status and the treatment outcome.

Three conditions:

1. Associated with the treatment.
2. Cause of the outcome separate from any effects it has on the treatment.
3. Not along a causal path between treatment and outcome (not a MEDIATOR / MECHANISM).

RANDOMIZATION solves by guaranteeing that the treatment and control groups have the same potential outcomes in expectation.

An estimator is UNBIASED if by repeating our estimation procedure over and over again an infinite number of times, the average value of our estimates would equal the estimand.

$$
\text{Bias} = E[Y_{0,T=1} - Y_{0,T=0}]
$$

## NOISE

An estimator is PRECISE if by repeating our estimation procedure over and over again, the various estimates would be close to each other.

An estimator is EFFICIENT if by repeating our estimation procedure over and over again, the various estimates would, on average, be close to the estimand.

LAW OF LARGE NUMBERS. The sample average can be arbitrarily close to the true population average by making the sample large enough.

An estimator is CONSISTENT if it converges exactly to the estimand as the sample size grows to infinity.

STANDARD ERROR. If we repeated our estimator an infinite number of times, how far it would be on average from the true estimand.

- Standard deviation of the sampling distribution of our estimator.

$$
\widehat{SE} = \sqrt{\frac{\widehat{Var(Y_0)}}{N-m}+\frac{\widehat{Var(Y_1)}}{m}}
$$

# 5 - EXPERIMENTS

## CONFIDENCE INTERVALS

POINT ESTIMATE. The single statistic we get from a study or analysis.

CONFIDENCE INTERVAL. A range representing our uncertainty about our point estimate due to random error or noise.

- Providing a range of possible true values consistent with our estimate.

95% Confidence. 95% of the intervals constructed in this way around an estimate will contain the true value.

CENTRAL LIMIT THEOREM. If we repeated a study infinite times, the value of many of the statistics we get will follow a normal distribution.

## HYPOTHESIS TESTING

P-VALUE. The probability of getting an estimate by chance alone.

Assuming the NULL HYPOTHESIS, there is a P-VALUE chance of obtaining a result as extreme as the ESTIMATE.

## EXPERIMENTS

STRATIFIED RANDOMIZATION. Split subjects by a few factors and randomize within those strata.

- Done to ensure better balance on stratification variables - usually choose expected strong confounders.

LAB EXPERIMENTS. Complete control.

FIELD EXPERIMENTS. Randomized control trial manipulated in the real world.

## THREATS TO INTERNAL VALIDITY

1\. CHANCE IMBALANCE.

Remedies:

1. Throw out the experiment.
2. Proceed as normal
3. Condition on the confouding variable in order to account for the imbalance and get a more efficient estimate.

2\. LACK OF STATISTICAL POWER.

POWER. The ability to detect a true effect if one exists.

3\. NONCOMPLIANCE.

INTENT TO TREAT EFFECT. Average effect of Z for the whole sample.

4\. PLACEBO EFFECT.

Remedy. Compare the treated group to the placebo.

5\. ATTRITION.

6\. INTERFERENCE.

CONTAMINATION. Treatment subjects become control and vice versa.

SPILLOVER. Treatment affects those in control.

# 6 - REGRESSION

Using observational data to mimic an experiment - once we control for enough things / make the comparison groups similar enough, the difference between the treatment & control groups is functionally random.

$$
Y_i = \alpha + \beta T_i + \gamma V_i + r_i
$$

- $\alpha$. The constant term.
- $\beta$. The effect of the treatment.
- $\gamma$. The 'effect' of the control variable.

The error associated with each prediction is $Y_i - (\hat{\alpha} + \hat{\beta} T_i + \hat{\gamma} X_i) = Y_i - \hat{Y_i}$

SUM OF SQUARED ERRORS. Measure of how well our estimates fit the data.

- ORDINARY LEAST SQUARES.

## OMITTED VARIABLE BIAS

Long regression: $Y_i = \alpha^l + \beta^l T_i + \gamma^l X_i + \epsilon_i$

Short regression: $Y_i = \alpha^s + \beta^s T_i + \epsilon_i$

$\epsilon$ is all the unexplained variation.

Quantifying the bias:

$$
X_i = \tau + \pi T_i + \mu_i
$$

- $\pi$ is a measure of the correlation between X and T.

$$
\beta^s - \beta^l = \pi \gamma
$$

Signing the bias:
| | Positive $\pi$ | Negative $\pi$ |
| ----------------- | -------------- | -------------- |
| Positive $\gamma$ | + | - |
| Negative $\gamma$ | - | + |

## CONDITIONAL-INDEPENDENCE ASSUMPTION

Assumption required for regression is assumption of controlling for all relevant differences.

- Also called the SELECTION-ON-OBSERVABLES assumption.

Problems:

1. How do we know we've controlled for all the relevant differences?
2. Some of the differences are unobservable and/or don't have very good proxies.

# 7 - Difference-in-Difference

Problem: Things change over time.

Solution: Account for that by looking at trends in proxies for the counterfactual.

PARALLEL TRENDS ASSUMPTION. Trends in potential outcomes are the same for treated and control units.

Measurement:

$$
(Y1_{treated, t=2} - Y0_{treated, t=1}) - (Y0_{untreated, t=2} - Y0_{untreated, t=1})
$$

- Change in treated before and after - change in untreated before and after.

Bias:

$$
(Y0_{treated, t=2} - Y0_{treated, t=1}) - (Y0_{untreated, t=2} - Y0_{untreated, t=1})
$$

- The bias is the difference in trends for the treated unit in the counterfactual and the trends for the untreated unit.

It CANNOT account for time-variant differences between units.

# 8 - Regression Discontinuity

Used when cutoffs on a RUNNING VARIABLE splits units into treated and untreated groups.

- Also known as the FORCING variable.

Measures the LOCAL AVERAGE TREATMENT EFFECT.

- ATE for those at the threshold for treatment assignment.

Measurement:

$$
\lim_{x\to 0+} E[Y1_i|X] - \lim_{x\to 0-} E[Y0_i|X]
$$

CONTINUITY ASSUMPTION. You could fit a smooth, continuous function for the potential outcomes across the threshold in both the treated and untreated groups.

$$
\lim_{x\to 0+} E[Y1_i|X] = \lim_{x\to 0-} E[Y1_i|X] \\
\lim_{x\to 0-} E[Y0_i|X] = \lim_{x\to 0+} E[Y0_i|X]
$$

Violation if units have control over whether they're on either side of the threshold, indicated by BUNCHING or CLUMPING.

# 9 - Instrumental Variables

Solution to noncompliance or natural experiments.

Problem: Can't drop people who don't comply with an experiment, because their potential outcomes are likely different.

|     | Z=1                             | Z=0                            |
| --- | ------------------------------- | ------------------------------ |
| T=1 | Compliers OR <br> Always Takers | Always Takers                  |
| T=0 | Never Takers                    | Compliers OR <br> Never Takers |

Estimate the proportion of noncompliers by comparing the average value of T in our treatment group & the average value of T in our control group.

INTENT-TO-TREAT EFFECT. ITT. Effect of Z on Y.

4 assumptions:

1. EXOGENEITY. Instrument must be randomly assigned.
2. EXCLUSION. All of the reduced form effect occurs through the treatment of interest.
3. COMPLIERS EXIST.
4. NO DEFIERS.

Measurement: WALD ESTIMATE.

$$
\frac{E[Y|Z=1] - E[Y|Z=0]}{E[T|Z=1] - E[T|Z=0]}
$$

- COMPLIER AVERAGE TREATMENT EFFECT (CATE) \* proportion of compliers.

# 10 - Bayesian Inference

PROBABILITY. Chance that an event occurs. $P(A)$

SAMPLE SPACE. Set of possible outcomes. $S = {}$

- Sum of all probabilities has to equal one.

INDEPENDENT EVENTS. Knowing that one event occurred tells you nothing about the likelihood another event occurred.

- Joint probability is $P(A) * P(B)$

CONDITIONAL PROBABILITY. Probability a given event occurs given the condition another event occurs. $P(A | B)$

JOINT PROBABILITY. Probability of two events.

$$
P(A \text{ and } B) = P(A | B) * P(B)
$$

BAYES' RULE:

$$
P(B | A) =  \frac{P(A | B) * P(B)}{P(A)}
$$

Expanded:

$$
P(B|A) = \frac{P(A|B) * P(B)}{P(A|B) * P(B) + P(A|B^c)*P(B^c)}
$$

BAYESIAN INFERENCE. PRIORS $\rightarrow$ EVIDENCE $\rightarrow$ POSTERIORS.

- PRIORS. Beliefs before. Also known as BASE RATES.
- EVIDENCE. New information.
- POSTERIORS. Beliefs after.

Application:

$$
P(\text{effect}|\text{estimate}) = \frac{P(\text{estimate}|\text{effect}) * P(\text{effect})}{P(\text{estimate}|\text{effect}) * P(\text{effect}) + P(\text{estimate}|\text{no effect}) * P(\text{no effect})}
$$

- $P(\text{effect}|\text{estimate})$ = significance level.
- $P(\text{estimate}|\text{effect})$ = power.
- $P(\text{effect})$ and $P(\text{no effect})$= prior.
- $P(\text{estimate}|\text{no effect})$ = p-value.

# 11 - Multiple Testing

SELECTIVE REPORTING and PUBLICATION BIAS mean that only meaningful results are published. That can result in bad science, either due to noise or manipulation.

P-HACKING. When an individual tries out different research questions, methods and subgroups.

P-SCREENING. When only some studies from a pool of many get published.

Solutions include:

1. Pre-registration.
2. Replication.
3. Significance thresholds.
4. Important hypotheses.
5. Skepticism.

# 12 - Reversion to the Mean

Any outcome that's partly a function of signal and noise demonstrates reversion to the mean, because extremes are a combination of strong signal and strong noise.

# 13 - Adaptation

People change their behavior in response to changes in the world.

Problems:

1. Studying the wrong outcome.
2. Extrapolating from a narrow quantitative result.

# 14 - PREDICTION

Best guess for an outcome given some meaningfully associated data.

Explanatory assumptions:

1. All confounders are included in the model or are marginalized away by controlling.
2. No mediators are included in the model.

Prediction assumption. The set of observations is representative of the population of interest.

STATIC PREDICTION. Assumes environment is static.

DYNAMIC PREDICTION. Environment may change due to adaptation or other change.

Good predictors:

1. Avoid redundancy.
2. Avoid pure noise.
3. Precise information reduces noise.
4. Predictors from a variety of domains provide different information.

## BIAS-VARIANCE TRADEOFF

Results in either OVERFITTING or UNDERFITTING a model.

Solutions: TRAINING DATA. TEST DATA. K-FOLD CROSS VALIDATION.
