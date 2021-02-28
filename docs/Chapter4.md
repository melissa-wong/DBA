# Bayes' Rule

## Exercise 4.1
Given $P(\theta = disease) = 0.001$, $P(+ | disease) = 0.99$ and $P(+ | no disease) = 0.05$


\begin{align*}
  P(disease | +) &= \frac{0.99 * 0.001}{0.99 * 0.001 + 0.05 * 0.999} \\
                &= 0.019
\end{align*}

## Exercise 4.2

\begin{align*}
  P(disease | -,+) &= \frac{P(- | disease) * 0.019)}{P(-)} \\
                   &= \frac{0.01 * 0.019}{0.01 * 0.001 + 0.95 * 0.999} \\
                   &= 0.0002
\end{align*}

## Exercise 4.3

### Part a

|     | disease | no disease |
|-----|---------|------------|
| D=+ | 99      | 4995       |
| D=- | 1       | 94905      |
|     | 100     | 99900      |

### Part b

$P(disease | +) = \frac{99}{99 + 4995} = 0.019$

### Part c

1st stage:

Number of people with disease who test postive: 10000 * 0.99 = 9900

Number of people without disease who test positive: 9990000 * 0.05 = 499500

2nd stage - Retest those with positive tests

Number of people with disease who test negative 2nd time: 9900 * 0.01 = 99

Number of people without disease who test negative 2nd time:  499500 * 0.95 = 474525

### Part d

$P(disease | -, +) = \frac{99}{99 + 474525} = 0.0002$

## Exercise 4.4

\begin{align*}
  P(D | -) &= \frac{P(-|D)P(D)}{P(-)} \\
           &= \frac{0.01 * 0.001}{0.01 * 0.001 + 0.95 * 0.999} \\
           &= 1.054* 10^{-5}
\end{align*}

\begin{align*}
  P(D | +, -) &= \frac{P(+|D) * 1.054*10^{-5}}{P(+)} \\
              &= \frac{0.99 * 1.054*10^{-5}}{0.99*0.001 + 0.05 * 0.999} \\
              &= 0.0002
\end{align*}

The result is the same as Part d.  In other words, the order of the tests doesn't change the conclusion which is consistent with the assumption that the tests are independent.

## Exercise 4.5

Given $P(Language Study) = 0.5$, then

\begin{align*}
  P(Language Study | ROI) &= \frac{P(ROI|Language Study) P(Language Study)}{P(ROI)}\\
                          &= \frac{166/(166+703) * 0.5}{0.5*(166/(166+703) + 199/(199+2154))} \\
                          &= 0.69
\end{align*}

## Exercise 4.6


```r
theta <- c(0.25, 0.5, 0.75)
prior <- c(0.25, 0.5, 0.25)
likelihood <- theta^3 * (1-theta)^9

num <- prior * likelihood
den <- sum(num)

post <- num/den

knitr::kable(tibble::tibble(theta = theta, posterior = post))
```



| theta| posterior|
|-----:|---------:|
|  0.25| 0.7054333|
|  0.50| 0.2935990|
|  0.75| 0.0009677|

## Exercise 4.7

$P(D) = P(D|\theta=0.25)*0.25 + P(D|\theta=0.5) * 0.5 + P(D|\theta=0.75) * 0.25$ which is the same as the sum of the likelihood * prior calculated in exercise 4.6.
