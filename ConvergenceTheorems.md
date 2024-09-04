layout: page
title: "Convergence Theorems"
permalink: /convergence_theorems

### 1. **Everywhere Convergence / Sure Convergence**

**Notation:** 
$$
X_n \xrightarrow{S} X
$$
**Explanation:** 
Sure convergence (or pointwise convergence) means that for each $\omega \in \Omega$, the sequence $X_n(\omega)$ converges to $X(\omega)$ as $n \to \infty$. Formally, this means:

$$
\forall \omega \in \Omega, \lim_{n \to \infty} X_n(\omega) = X(\omega)
$$

**Example:** 
Consider $X_n(\omega) = \frac{1}{n} \cdot \omega$ for $\omega \in [0,1]$. As $n \to \infty$, $X_n(\omega) \rightarrow 0$ for every $\omega$, hence $X_n \xrightarrow{S} 0$.

### 2. **Almost Sure Convergence**

**Notation:** 
$$
X_n \xrightarrow{a.s.} X
$$
**Explanation:** 
Almost sure convergence means that there exists a set $S \subseteq \Omega$ with $\mathbb{P}(S) = 1$ such that for all $\omega \in S$, $X_n(\omega)$ converges to $X(\omega)$ as $n \to \infty$. Formally:

$$
\mathbb{P}\left(\lim_{n \to \infty} X_n = X \right) = 1
$$

**Example:** 
Consider a sequence of i.i.d. random variables $X_n$ uniformly distributed over $[0, 1]$. Define $X = 0$. Then $X_n(\omega)$ will converge to 0 almost surely as $n \to \infty$, so $X_n \xrightarrow{a.s.} 0$.

### 3. **Convergence in Probability**

**Notation:** 
$$
X_n \xrightarrow{P} X
$$
**Explanation:** 
Convergence in probability means that for every $\epsilon > 0$, the probability that $X_n$ deviates from $X$ by at least $\epsilon$ tends to zero as $n \to \infty\. Formally:

$$
\lim_{n \to \infty} \mathbb{P}(|X_n - X| \geq \epsilon) = 0
$$

**Example:** 
Consider $X_n = \frac{1}{n}$ and $X = 0$. Then $\mathbb{P}(|X_n - 0| \geq \epsilon)$ for any fixed $\epsilon > 0$ will approach 0 as $n \to \infty$, hence $X_n \xrightarrow{P} 0$.

### 4. **Convergence in Distribution**

**Notation:** 
$$
X_n \xrightarrow{d} X
$$
**Explanation:** 
Convergence in distribution means that the cumulative distribution function (CDF) of $X_n$ converges to the CDF of $X$ at all points where the CDF of $X$ is continuous. Formally:

$$
\lim_{n \to \infty} F_{X_n}(x) = F_X(x) \quad \text{for all } x \text{ where } F_X(x) \text{ is continuous}
$$

**Example:** 
Consider $X_n$ to be normally distributed with mean $0$ and variance $\frac{1}{n}$. As $n \to \infty$, $X_n$ converges in distribution to a point mass at 0. Hence $X_n \xrightarrow{d} 0$.

### 5. **Convergence in Quadratic Mean (Mean-Square Convergence)**

**Notation:** 
$$
X_n \xrightarrow{m.s.} X
$$
**Explanation:** 
Convergence in quadratic mean (or mean-square convergence) means that the expected value of the squared difference between $X_n$ and $X$ tends to zero as $n \to \infty$. Formally:

$$
\lim_{n \to \infty} \mathbb{E}[(X_n - X)^2] = 0
$$

**Example:** 
Consider $X_n = \frac{1}{n} + \epsilon_n$, where $\epsilon_n$ is a sequence of random variables with $\mathbb{E}[\epsilon_n^2] = \frac{1}{n^2}$. As $n \to \infty$, $\mathbb{E}[(X_n - 0)^2] = \frac{1}{n^2} + \frac{1}{n^2}$ tends to zero, so $X_n \xrightarrow{m.s.} 0$.

### Central Limit Theorem (CLT)

**Statement:**

For a sequence of i.i.d. random variables $X_1, X_2, \ldots$ with mean $\mu$ and variance $\sigma^2$, the normalized sum of these random variables converges in distribution to a standard normal random variable:

$$
\frac{\overline{X}_n - \mu}{\sigma / \sqrt{n}} \xrightarrow{d} \mathcal{N}(0,1)
$$

**Explanation:** 
The CLT states that as the sample size $n$ becomes large, the distribution of the sample mean $\overline{X}_n$ (after appropriate normalization) will approach a normal distribution, regardless of the original distribution of the $X_i$.

**Example:** 
Suppose you draw $X_i$ from a uniform distribution $\text{Unif}(0,1)$. Even though $X_i$ is not normally distributed, the sum $S_n = \sum_{i=1}^{n} X_i$, when properly normalized, will approximate a normal distribution as $n$ grows large.

### Strong Law of Large Numbers (SLLN)

**Statement:**

If $X_1, X_2, \ldots$ are i.i.d. random variables with $\mathbb{E}[X_i] = \mu$ and $\text{Var}(X_i) < \infty$, then:

$$
\overline{X}_n \xrightarrow{a.s.} \mu
$$

**Explanation:** 
The SLLN guarantees that the sample mean $\overline{X}_n$ converges almost surely to the expected value $\mu$.

**Example:** 
If $X_i$ are the outcomes of rolling a fair six-sided die, then the sample mean $\overline{X}_n$ will almost surely converge to the expected value $\mu = 3.5$ as $n$ increases.

### Weak Law of Large Numbers (WLLN)

**Statement:**

If $X_1, X_2, \ldots$ are i.i.d. random variables with $\mathbb{E}[X_i] = \mu$ and $\text{Var}(X_i) < \infty$, then:

$$
\overline{X}_n \xrightarrow{P} \mu
$$

**Explanation:** 
The WLLN states that the sample mean $\overline{X}_n$ converges in probability to the expected value $\mu$.

**Example:** 
Continuing with the fair die, the sample mean $\overline{X}_n$ converges in probability to $\mu = 3.5$ as $n$ increases, though not as strongly as in the SLLN.

---

### 1. **Everywhere Convergence / Sure Convergence**

**Example:**
Consider the sequence of random variables $X_n(\omega) = \frac{1}{n} \cdot \omega$ where $\omega$ is a fixed number in the interval $[0,1]$. 

- **Detailed Explanation:** Here, the random variable $X_n$ is explicitly defined as a function of $\omega$, which is the outcome of some underlying probability experiment. Since $X_n(\omega)$ is simply the product of $\omega$ and the decreasing sequence $\frac{1}{n}$, as $n$ increases, $X_n(\omega)$ becomes smaller and smaller, converging to 0. This convergence happens for every single value of $\omega$, hence it is a pointwise convergence (or sure convergence).

- **Justification:** 
For any $\omega \in [0,1]$, we have:
$$
\lim_{n \to \infty} X_n(\omega) = \lim_{n \to \infty} \frac{1}{n} \cdot \omega = 0
$$
Thus, $X_n \xrightarrow{S} 0$ because the convergence is valid for all $\omega$ in the probability space $[0, 1]$.

### 2. **Almost Sure Convergence**

**Example:**
Consider a sequence of random variables $X_n$ defined as $X_n(\omega) = \frac{1}{n}$ if $\omega$ is a rational number in $[0,1]$, and $X_n(\omega) = 1$ if $\omega$ is irrational.

- **Detailed Explanation:** 
In this example, as $n$ increases, $X_n(\omega)$ converges to 0 for rational $\omega$ and remains 1 for irrational $\omega$. The set of irrational numbers has full measure (i.e., it is uncountably infinite and has probability 1 under the uniform distribution on $[0,1]$), while the set of rational numbers has measure zero (countably infinite and hence zero probability). 

- **Justification:** 
Because the set of irrational numbers (where $X_n(\omega) = 1$) has full measure, the sequence $X_n$ does not converge to 0 on that set. However, on the set of rational numbers (measure zero), $X_n(\omega)$ converges to 0. Since almost sure convergence only requires the sequence to converge on a set of full measure, and it does converge for the vast majority (irrationals), we have $X_n \xrightarrow{a.s.} 0$.

### 3. **Convergence in Probability**

**Example:**
Consider $X_n = \frac{1}{n}$ and $X = 0$.

- **Detailed Explanation:** 
The sequence $X_n$ is deterministic, not random, and it is equal to $\frac{1}{n}$ for all $\omega$. As $n$ increases, $X_n$ gets closer to 0. We are interested in the probability that $X_n$ deviates from $X = 0$ by more than a fixed $\epsilon > 0$.

- **Justification:** 
For any fixed $\epsilon > 0$:
$$
\mathbb{P}(|X_n - 0| \geq \epsilon) = \mathbb{P}\left(\frac{1}{n} \geq \epsilon\right)
$$
Since $\frac{1}{n}$ decreases as $n$ increases, there exists a sufficiently large $n_0$ such that for all $n \geq n_0$, $\frac{1}{n} < \epsilon$. Therefore:
$$
\lim_{n \to \infty} \mathbb{P}\left(\frac{1}{n} \geq \epsilon\right) = 0
$$
Thus, $X_n \xrightarrow{P} 0$, indicating convergence in probability.

### 4. **Convergence in Distribution**

**Example:**
Consider $X_n$ to be normally distributed with mean $0$ and variance $\frac{1}{n}$, i.e., $X_n \sim \mathcal{N}(0, \frac{1}{n})$.

- **Detailed Explanation:** 
As $n$ increases, the variance of $X_n$ decreases, making the distribution more concentrated around the mean $0$. We are interested in the limit distribution of $X_n$ as $n$ tends to infinity.

- **Justification:** 
The cumulative distribution function (CDF) of $X_n$ is given by:
$$
F_{X_n}(x) = \mathbb{P}(X_n \leq x) = \frac{1}{2} \left[1 + \text{erf}\left(\frac{x}{\sqrt{2/n}}\right)\right]
$$
As $n \to \infty$, the variance $\frac{1}{n} \to 0$, so the distribution of $X_n$ becomes a point mass at 0:
$$
\lim_{n \to \infty} F_{X_n}(x) = 
\begin{cases} 
0 & \text{if } x < 0 \\
1 & \text{if } x \geq 0
\end{cases}
$$
This is the CDF of a Dirac delta distribution centered at 0, implying $X_n \xrightarrow{d} 0$.

### 5. **Convergence in Quadratic Mean (Mean-Square Convergence)**

**Example:**
Let $X_n = \frac{1}{n} + \epsilon_n$, where $\epsilon_n$ is a sequence of random variables with $\mathbb{E}[\epsilon_n^2] = \frac{1}{n^2}$.

- **Detailed Explanation:** 
Here, $X_n$ is the sum of a deterministic term $\frac{1}{n}$ and a random term $\epsilon_n$. Mean-square convergence means that the expected value of the squared difference between $X_n$ and 0 (our limiting value) should go to 0 as $n$ increases.

- **Justification:** 
First, calculate the mean square difference:
$$
\mathbb{E}[(X_n - 0)^2] = \mathbb{E}\left[\left(\frac{1}{n} + \epsilon_n\right)^2\right]
$$
Expand the square:
$$
= \mathbb{E}\left[\frac{1}{n^2} + 2\frac{\epsilon_n}{n} + \epsilon_n^2\right]
$$
Since $\mathbb{E}[\epsilon_n] = 0$, the cross term disappears:
$$
= \frac{1}{n^2} + \mathbb{E}[\epsilon_n^2] = \frac{1}{n^2} + \frac{1}{n^2} = \frac{2}{n^2}
$$
As $n \to \infty$, $\frac{2}{n^2} \to 0$, so $X_n \xrightarrow{m.s.} 0$.

### Central Limit Theorem (CLT)

**Example:**
Let $X_i$ be i.i.d. random variables drawn from a uniform distribution on $[0,1]$, $X_i \sim \text{Unif}(0,1)$. Consider the sum $S_n = \sum_{i=1}^{n} X_i$.

- **Detailed Explanation:**
The sum $S_n$ is simply the sum of $n$ independent uniform random variables. According to the CLT, regardless of the original distribution, the distribution of the normalized sum $\frac{S_n - n\mu}{\sigma\sqrt{n}}$ will approach a normal distribution as $n$ grows large.

- **Justification:**
For $X_i \sim \text{Unif}(0,1)$, we have:
$$
\mu = \mathbb{E}[X_i] = \frac{1}{2}, \quad \sigma^2 = \text{Var}(X_i) = \frac{1}{12}
$$
The CLT states:
$$
\frac{S_n - n\mu}{\sigma \sqrt{n}} \xrightarrow{d} \mathcal{N}(0, 1)
$$
which, for large $n$, means that the distribution of the sum $S_n$ will approximate a normal distribution with mean $n\mu$ and variance $n\sigma^2$.

### Strong Law of Large Numbers (SLLN)

**Example:**
If $X_i$ are the outcomes of rolling a fair six-sided die, then the sample mean $\overline{X}_n = \frac{1}{n} \sum_{i=1}^{n} X_i$ will almost surely converge to the expected value $\mu = 3.5$.

- **Detailed Explanation:** 
Here, each $X_i$ is a discrete random variable taking values in $\{1, 2, 3, 4, 5, 6\}$ with equal probability. The expectation $\mu = \mathbb{E}[X_i] = 3.5$. The SLLN states that as we roll the die more and more times, the average outcome (sample mean) will almost surely converge to $\mu = 3.5$.

- **Justification:** 
According to the SLLN:
$$
\overline{X}_n \xrightarrow{a.s.} 3.5
$$
The reason for this convergence is that the sample mean $\overline{X}_n$ is an unbiased estimator of the true mean $\mu = 3.5$, and the SLLN guarantees that with enough trials, the effect of randomness will be averaged out, leaving only the true mean.

### Weak Law of Large Numbers (WLLN)

**Example:**
For the same fair die rolling experiment, the sample mean $\overline{X}_n = \frac{1}{n} \sum_{i=1}^{n} X_i$ will converge in probability to the expected value $\mu = 3.5$.

- **Detailed Explanation:**
In this case, instead of almost sure convergence, we are considering convergence in probability. This means that as the number of rolls $n$ increases, the probability that the sample mean deviates from the expected value by any fixed amount $\epsilon$ tends to zero.

- **Justification:**
The WLLN asserts that for any $\epsilon > 0$:
$$
\lim_{n \to \infty} \mathbb{P}(|\overline{X}_n - 3.5| \geq \epsilon) = 0
$$
This is because the variance of the sample mean $\text{Var}(\overline{X}_n) = \frac{\sigma^2}{n}$ decreases as $n$ increases, making the sample mean increasingly concentrated around the expected value $3.5$.

In summary, each of these examples illustrates a different mode of convergence for sequences of random variables, and the justifications are grounded in the fundamental properties of probability distributions and expectations. Each mode of convergence provides a different lens through which to view the behavior of random sequences, making them crucial tools in both theoretical and applied probability.
