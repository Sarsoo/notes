---
title: 'Supervised Learning'
tags:
  - ai
  - classification
---

# Gaussian Classifier
- With $T$ labelled data
$$q_t(i)=
\begin{cases}
    1 & \text{if class } i \\
    0 & \text{otherwise}
\end{cases}$$
- Indicator function

- Mean parameter
$$\hat m_i=\frac{\sum_tq_t(i)o_t}{\sum_tq_t(i)}$$
- Variance parameter
$$\hat v_i=\frac{\sum_tq_t(i)(o_t-\hat m_i)^2}{\sum_tq_t(i)}$$

- Distribution weight
	- Class prior
	- $P(N_i)$
$$\hat c_i=\frac 1 T \sum_tq_t(i)$$

$$\hat \mu_i=\frac{\sum_{t=1}^Tq_t(i)o_t}{\sum_{t=1}^Tq_t(i)}$$
$$\hat\sum_i=\frac{\sum_{t=1}^Tq_t(i)(o_t-\mu_i)(o_t-\mu_i)^T}{\sum_{t=1}^Tq_t(i)}$$
- For K-dimensional