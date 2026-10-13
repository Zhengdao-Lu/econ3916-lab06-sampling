# econ3916-lab06-sampling
# Sampling for Machine Learning — Train-Test Splits

## Objective

I studied how sampling design and data leakage affect the reliability of machine-learning evaluation.

## Methodology

- I explored survival patterns for 891 passengers in the Titanic dataset.
- I compared naive and stratified train-test splits.
- I checked whether stratification preserved the survival rate in both sets.
- I identified and corrected data leakage in the StandardScaler and SimpleImputer steps.
- I wrote `split_by_share()` to split a table using a test share and seed.
- I simulated the 1936 Literary Digest polling failure using 10 million voters.
- I compared a biased sample of 4,382,503 responses with a random sample of 50,000.
- I calculated Meng’s data defect correlation.
- I ran 100 replications comparing biased and random sampling.

## Key Findings

I found that stratification kept the survival rate consistent between the training and test sets. I also learned that preprocessing must be fitted only on the training data because using test-set information creates data leakage and makes the evaluation misleading.

In the polling simulation, the biased sample of 4,382,503 responses was less accurate than the random sample of 50,000. A data defect correlation of 0.1475 produced an error of 8.3 percentage points. This showed me that sample design can matter more than sample size.
