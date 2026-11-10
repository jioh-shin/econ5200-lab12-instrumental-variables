# Instrumental Variables: Weak Instruments, Compliers and the Exclusion Restriction

## Objective
In this lab, I explored how instrumental variables work, how weak instruments affect 2SLS estimates, and why the exclusion restriction matters.

## Methodology
- I simulated a weak instrument and compared OLS and 2SLS estimates with the true treatment effect.
- I examined how instrument strength affects the accuracy and statistical significance of 2SLS estimates.
- I replicated Card's (1995) study using college proximity as an instrument for schooling to estimate returns to education.
- I tested how a small direct effect of the instrument on the outcome changes the 2SLS estimate and violates the exclusion restriction.
- I wrote my own two-stage least squares function using two OLS regressions and compared the results with the `linearmodels` package.

## Key Findings
- **Weak instruments:** When the true effect was 1.0 and the median first-stage F-statistic was 0.5, the median 2SLS estimate was 2.038, compared with the median OLS estimate of 1.998. I found that statistically significant 2SLS estimates were often far from the true effect.
- **Card (1995) replication:** The first-stage F-statistic was 16.7. The estimated return to schooling was 0.0740 using OLS and 0.1323 using 2SLS.
- **Exclusion restriction:** I found that even a small direct effect of the instrument on the outcome can change the 2SLS estimate, showing why the exclusion restriction is important.
- **Manual 2SLS:** I implemented 2SLS using two OLS regressions and checked my implementation against the `linearmodels` package.
