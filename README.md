# Machine Learning Reference

A compact reference of the core equations and loss functions behind common machine
learning models — the page to check when you need the exact form of an objective,
not a tutorial.

![License](https://img.shields.io/badge/license-MIT-green.svg)
![Topic](https://img.shields.io/badge/-machine%20learning-05122A?style=flat)
![LaTeX](https://img.shields.io/badge/-LaTeX-05122A?style=flat&logo=latex&logoColor=white)

**Formats:** rendered below · [PDF](machine-learning-models.pdf) · [LaTeX source](machine-learning-models.tex)

**Notation:** $x$ input · $y$ target · $\hat{y}$ prediction · $w$ weights · $b$ bias · $\lambda$ regularization strength · $\eta$ learning rate

---

## I. Supervised learning

### Linear regression

$$\hat{y} = w^T x + b$$

$$\mathcal{L}(w, b) = \frac{1}{n} \sum_{i=1}^n (y_i - \hat{y}_i)^2$$

### Logistic regression

$$\hat{y} = \frac{1}{1 + e^{-w^T x - b}}$$

$$\mathcal{L}(w, b) = -\frac{1}{n} \sum_{i=1}^n \left[ y_i \log(\hat{y}_i) + (1 - y_i) \log(1 - \hat{y}_i) \right]$$

### Ridge regression (L2)

$$\mathcal{L}(w, b) = \frac{1}{n} \sum_{i=1}^n (y_i - \hat{y}_i)^2 + \lambda \|w\|^2$$

### Lasso regression (L1)

$$\mathcal{L}(w, b) = \frac{1}{n} \sum_{i=1}^n (y_i - \hat{y}_i)^2 + \lambda \|w\|_1$$

### Support vector machine

$$\hat{y} = \text{sign}(w^T x + b)$$

$$\mathcal{L}(w) = \frac{1}{n} \sum_{i=1}^n \max(0,\, 1 - y_i(w^T x_i + b)) + \lambda \|w\|^2$$

### Decision tree

$$\text{Gini} = 1 - \sum_{k} p_k^2$$

$$\text{Entropy} = -\sum_{k} p_k \log(p_k)$$

### Random forest

$$\hat{y} = \frac{1}{T} \sum_{t=1}^{T} \hat{y}^{(t)}$$

### Gradient boosting

$$\hat{y}_i^{(t)} = \hat{y}_i^{(t-1)} + \eta f_t(x_i)$$

$$\mathcal{L}^{(t)} = \sum_{i=1}^n l(y_i, \hat{y}_i^{(t)}) + \sum_{t=1}^T \Omega(f_t)$$

---

## II. Unsupervised learning

### K-means clustering

$$\min_{C} \sum_{k=1}^{K} \sum_{x_i \in C_k} \|x_i - \mu_k\|^2$$

### Principal component analysis

$$\text{maximize} \quad \text{Var}(Xw) \quad \text{s.t.} \quad \|w\| = 1$$

### Gaussian mixture models

$$P(x) = \sum_{k=1}^{K} \pi_k \mathcal{N}(x \mid \mu_k, \Sigma_k)$$

---

## III. Deep learning

### Feedforward network

$$a^{(l)} = f(W^{(l)} a^{(l-1)} + b^{(l)})$$

### Convolutional network

$$S(i, j) = (X * K)(i, j) = \sum_m \sum_n X(i+m, j+n) \cdot K(m,n)$$

### Recurrent network

$$h_t = f(W x_t + U h_{t-1} + b)$$

### Transformer — self-attention

$$\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V$$

---

## IV. Reinforcement learning

### Q-learning

$$Q(s, a) \leftarrow Q(s, a) + \alpha \left[ r + \gamma \max_{a'} Q(s', a') - Q(s, a) \right]$$

### Policy gradient

$$\nabla J(\theta) = \mathbb{E}_{\pi_\theta} \left[ \nabla_\theta \log \pi_\theta(a \mid s) R \right]$$

---

## Also in this repository

**[Unlocking the Power of Generative AI with LangChain](generative-ai-langchain.pdf)** — 4 pages, August 2025

A practical guide to working around the limits of raw language models: hallucination,
static knowledge, no real-time data access, and weak context retention. Covers
retrieval-augmented generation, fact-checking, summarization strategies, memory
integration, deployment and monitoring, and ethical considerations including bias
mitigation and regulatory compliance.

---

## References

- Hastie, Tibshirani & Friedman (2009), *The Elements of Statistical Learning*
- Goodfellow, Bengio & Courville (2016), *Deep Learning*

## Contributing

Spotted an error in a formula? Open an issue — corrections are welcome.

## Author

Saad Tadjaoui — AI/ML engineering, Casablanca.
[Portfolio](https://saadtadja.github.io) · [GitHub](https://github.com/SaadTadja)

## License

MIT — see [LICENSE](LICENSE).
