# Stochastic-Computational-Modeling


This project focuses on the implementation and analysis of stochastic models using Python. It covers the transition of discrete states, the simulation of continuous-time random walks, and high-dimensional optimization techniques.

---

## 🧩 Project Components

### 1. Markov Chain Modeling
I analyzed an absorbing Markov chain to understand how a system transitions toward stability. 
* **Key Discovery:** By calculating the Fundamental Matrix $N$, I determined the expected "life expectancy" of a process before it falls into an absorbing state (B or D).
* **Mathematical Tools:** Canonical form, Matrix inversion, Row-stochastic verification.

### 2. Generalised Random Walk (SDEs)
I simulated a random walk governed by a Stochastic Differential Equation (SDE) using the **Euler-Maruyama method**.
* **Key Discovery:** Identified that numerical noise must scale with $\sqrt{dt}$ to maintain physical accuracy. 
* **Parameters:** Custom drift and diffusion coefficients based on Student ID ($\alpha=3.46, \beta=0.12$).

### 3. Metropolis-Hastings Optimization
I optimized a complex 4D "Himmelblau-style" function to find its global maximum.
* **Key Discovery:** Corrected a common "greedy" algorithm by implementing a stochastic acceptance criterion, allowing the solver to escape local maxima and find the true peak.
* **Logic:** Leveraged MCMC to navigate high-dimensional space efficiently where traditional grid search fails.

---

## 🛠 Tech Stack
* **Language:** Python 3.12
* **Libraries:** NumPy (Matrix Algebra), SciPy (Statistical Testing), Matplotlib (Visualization), Pandas (Data Formatting)

---

## 📊 Sample Visualizations
*(Note: These are generated during the notebook execution)*
- **Trace Plots:** Showing MCMC convergence to the maximum.
- **Histograms:** Analyzing the non-normal distribution of random walk end-points.
- **Transition Maps:** Visualizing the flow of probability in Markov Chains.
