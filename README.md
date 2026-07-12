# Hey, I'm Yash.

CS student building ML systems from first principles — currently working through what's underneath the tools everyone else treats as black boxes.

CSE @ Manipal University Jaipur · ML Engineering Intern @ Nippon India Mutual Fund · Head of AI/ML, IEEE RAS MUJ

---

## Aurelius — a deep learning framework, from scratch, in C++

A neural network framework built entirely by hand in modern C++ — no PyTorch, no autograd, no ML libraries. Just Eigen and the chain rule.

- **Backpropagation derived by hand and verified against numerical finite-difference gradients.** If the analytical gradient and the numerical one disagree, the math is wrong — and I wanted to know, not assume.
- **Activation abstraction born from a real bug.** A silent Leaky ReLU gradient mismatch shipped without any visible failure — just slower convergence. The fix wasn't a patch; it was restructuring activations so a forward function and its derivative live in the same class and cannot drift apart.
- Softmax + cross-entropy with numerical stability handling; mini-batch SGD; configurable architectures; early stopping.
- **94.45% test accuracy on MNIST** (v0.2.0). He initialization on the v0.3 branch takes it to **96.95%** in a fraction of the epochs.

`C++` · `Eigen` · `CMake`

**In progress (v0.3):** activation hierarchy → optimizer abstraction (SGD + Adam) → L2 regularization → LR scheduling → Dropout → GELU

---

## Production agentic ML — Nippon India Mutual Fund

Built and shipped internally (code is proprietary):

- **A company-wide tool-calling agent** for Outlook and Teams automation — Microsoft Graph API, OAuth2, Claude on AWS Bedrock via boto3.
- **A multi-agent investment research pipeline** in LangGraph — a ReAct orchestrator coordinating market-data, news, and writer agents.
- **A KYC document analysis system** with a cost-tiered multi-model architecture (Haiku for extraction, Sonnet for reasoning), designed for 150,000+ forms per month.

---

## Algorithmic Trading Backtester

Python system for testing trading strategies against historical market data, comparing rule-based signals with ML models.

- Moving-average and logistic-regression strategies
- Measured performance: ML strategy Sharpe **0.99**, max drawdown **−34.7%** vs. buy-and-hold **−60.9%**

`Python` · `Pandas` · `Scikit-learn`

---

## Also working on

- Deeper C++ and systems fundamentals · CUDA next
- DSA in C++ and Python
- Momentum— a habit tracker in Flutter, because not everything has to be a gradient

---

<sub>Arch + Hyprland · terminal-first · <a href="https://www.linkedin.com/in/yashovardhan-jha-1703701b5">LinkedIn</a> · yashovardhan20@gmail.com</sub>

<sub><i>Dive beneath the abstractions. Reach for the sun.</i></sub>
