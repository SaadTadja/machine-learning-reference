# Machine Learning Reference

Two short technical documents I wrote while studying and building ML systems.

![License](https://img.shields.io/badge/license-MIT-green.svg)
![Topic](https://img.shields.io/badge/-machine%20learning-05122A?style=flat)
![LaTeX](https://img.shields.io/badge/-LaTeX-05122A?style=flat&logo=latex&logoColor=white)

---

## 1. Machine Learning Models

**[machine-learning-models.pdf](machine-learning-models.pdf)** — 2 pages, July 2025

A compact reference of the key equations and loss functions behind the models
you actually reach for. Written to be the page you check when you need the exact
form of an objective, not a tutorial.

**Covers**

| Area | Models |
|---|---|
| Linear models | Linear regression (MSE), logistic regression (cross-entropy), Ridge and Lasso penalties |
| Non-linear models | Decision trees (Gini, entropy), random forests, gradient boosting |
| Unsupervised | K-means objective, PCA |
| Deep learning | Feedforward pass and activations, 2D convolution |
| Reinforcement learning | Q-learning update, policy gradient |

Notation is fixed up front — inputs, targets, predictions, weights, regularization
strength — so the formulas stay consistent across sections.

References: Hastie et al., *The Elements of Statistical Learning* (2009);
Goodfellow et al., *Deep Learning* (2016).

---

## 2. Unlocking the Power of Generative AI with LangChain

**[generative-ai-langchain.pdf](generative-ai-langchain.pdf)** — 4 pages, August 2025

A practical guide to using LangChain to work around the limits of raw language
models: hallucination, static knowledge, no real-time data access, and weak
context retention across long conversations.

**Covers**

- What distinguishes generative models from classification and prediction models
- Retrieval-augmented generation (RAG) and fact-checking approaches
- Summarization strategies and memory integration
- Customizing, deploying and monitoring an assistant
- Ethical considerations: bias mitigation, transparency, regulatory compliance

---

## Why these are here

Both started as LinkedIn articles. Putting them in a repository makes them
searchable, citable, and correctable — if you find an error, open an issue.

## Author

Saad Tadjaoui — AI/ML engineering, Casablanca.
[Portfolio](https://saadtadja.github.io) · [GitHub](https://github.com/SaadTadja)

## License

MIT — see [LICENSE](LICENSE).
