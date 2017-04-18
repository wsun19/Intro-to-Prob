---
title: Midterm 2 Study Guide
author:
    - William Sun
geometry: margin=2.5cm
header-includes:
    - \usepackage{setspace}
    - \doublespacing
---
# Random Variables
- $X : \Omega \rightarrow \mathbb{R}$ can be discrete or continuous
- If $X$ is a discrete random variable, we will associate it with a *probability mass function (pmf)* $P_X$
    - $P_X(x) > 0$ $\forall$ $x \in$ {values of $X$}
    - $\sum_x P_X(x) = 1$, where the sum is over all the possible values of $X$
    - Used to calculate some probabilities: $P(X \in A) = \sum_{x \in A}P_X(x)$

# Functions of Random variables
- With pmf of $X$ and $Y = g(X)$:
$$ P_Y(y) = \sum\limits_{x : g(x) = y}P_X(x)$$

# Expected Value and Variance of a Discrete Random Variable
- $\mathbb{E}$: also the mean, weighted average, or center of mass
$$\mathbb{E}(X) = \sum\limits_x x P_X(x)$$
- The variance of an random variable: $Var(x) = (x - \mu)^2$, where $\mu = \mathbb{E}(X)$
	- So $\mathbb{E}( \{X - \mu\}^2) := Var(X)$
- A form of the $Var(X)$ more amenable to calculations: $\bf{Var(X) = \mathbb{E}(X^2) - \mathbb{E}(X)^2}$

# Cumulative Distribution Function (CDF)
- $F(X) = P(X \leq x)$
    #) $F : \mathbb{R} \rightarrow [0, 1]$
    #) If $x < y$, $F(x) \leq F(y)$
- Notation: Left-limit notation $F(c-) = lim_{x \rightarrow c-}F(x)$
- If we know the CDF,
    - $P(a < x \leq b) = F(b) - F(a)$
    - $P(a \leq x \leq b) = F(b) - F(a-)$
    - $P(a \leq x < b) = F(b-) - F(a-)$
    - $P(a < x < b) = F(b-) - F(a)$
    - General rule: If near "<", $a \rightarrow - F(a)$, $b \rightarrow F(b-)$
        - "a < b" ... so if "<" is near $a$, the "-" is on the left; "-" is on the right for $b$

# Law of the Unconscious Statistician
- If $X$ is discrete and $G: \mathbb{R} \rightarrow \mathbb{R}$, then
	- $\bf{\mathbb{E}(g(X)) = \sum_x g(x) P(X = x)}$ when the expectation exists
- Used when we know $G(X)$ and the distribution of $X$ but not the distribution of $G(X)$
- Some consequences:
	- Linearity of Expectation #1
		- $\mathbb{E}(aX + b) = a\mathbb{E}(X) + b$
	- Linearity of Expectation #2
		- $\mathbb{E}(X_1 + X_2 + \dots + X_n) = \mathbb{E}(X_1) + \mathbb{E}(X_2) + \dots + \mathbb{E}X_n)$
		- Expectation of a sum is the sum of the individual expected values
		- For any random variables for which $\mathbb{E}(X_i)$ exists for all $i$
		- *To be proved later*
