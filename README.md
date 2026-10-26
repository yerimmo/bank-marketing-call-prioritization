# Who Should We Call First?

A bank has more eligible customers than its staff can call. This project ranks customers by how likely they are to subscribe to a term deposit, so the call team starts with the people most likely to say yes.

📊 **[View the slides](Slides.pdf)** | 📓 **[View the notebook](Analysis.ipynb)**

## Business Problem

Call capacity is limited, so the real question is not "who will subscribe?" but "who should be on the top of the list?" We evaluated every model on the same business metric: how many subscribers it captures in the top 10% of the call list.

## Data

[UCI Bank Marketing dataset](https://archive.ics.uci.edu/dataset/222/bank+marketing): 41,176 phone campaign records from a Portuguese bank, with client, campaign, and economic indicators.

## Results

- **Logistic Regression** found **550 subscribers** in the top 10% of the test set (precision 66.75%).
- That is a **2.17x lift** over random calling, about **116.5% more subscribers** for the same number of calls.
- Logistic Regression outperformed k-NN and Decision Tree on this metric.

## My Role

I led **business understanding, EDA, and data preparation**, including:

- **Removing call-duration leakage.** Call duration is only known after the call ends, so it cannot be used to decide who to call.
- **Recoding `pdays`.** The value 999 means "never contacted before," not a real number of days, so it was recoded instead of treated as a large number.

## Team

Team 10 "High Five": Daniel Li, Yerim Mo, Celeste Wang, Chrissy Wang, Yuri Yang

## Tools

Python · pandas · scikit-learn

*Final project for ISOM 672 Introduction to Business Analytics, Emory University, Fall 2026.*
