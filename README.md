# server-performance-hypothesis-testing
# Server-Ops Analytics: Statistical Benchmarking of Next-Gen Infrastructure

## 📌 Project Overview
In modern cloud infrastructure, even minor latencies in server response times can degrade user experience, trigger customer churn, and impact business revenue. This project delivers a data-driven performance benchmark comparing an old legacy server (**Team-A**) against a newly deployed next-generation server (**Team-B**).

By applying **Inferential Statistics (Independent Two-Sample T-Test)** in Python, this analysis scientifically validates whether the upgrade provides a statistically superior performance enhancement or if the observed speed differences are merely random operational fluctuations.

---

## 📊 Business Problem & Hypothesis Framework
The DevOps and Infrastructure teams required mathematical validation before completely decommissioning the legacy architecture. 

* **Null Hypothesis ($H_0$):** There is no significant difference between the average response times of the legacy server and the next-gen server ($\mu_A = \mu_B$).
* **Alternative Hypothesis ($H_1$):** The average response time of the next-gen server is significantly different (faster) than the legacy server ($\mu_A \neq \mu_B$).
* **Significance Level ($\alpha$):** 0.05 ($5\%$)

---

## 🛠️ Tech Stack & Statistical Methodologies
* **Programming Language:** Python
* **Key Libraries:** NumPy, SciPy (Stats sub-module), Seaborn, Matplotlib
* **Core Concepts Implemented:**
  * **Descriptive Statistics:** Evaluation of sample means, variance, and sample sizes ($n=20$).
  * **Inferential Statistics:** Manual algebraic execution of the Independent T-Test formula alongside programmatic validation.
  * **Critical Value Mapping:** Utilizing the Percent Point Function (`stats.t.ppf`) to determine exact rejection thresholds based on Degrees of Freedom ($df = 38$).
  * **Data Visualization:** Mapping probability density using Kernel Density Estimation (KDE).

---

## 📈 Visualizing the Performance Profiles
The project utilizes a high-fidelity **Kernel Density Estimation (KDE) Plot** to visually contrast the spread, variance, and density of server response times:

* **Red Dashed Line ($--$):** Represents the historical mean response time of the Legacy Server (Team-A).
* **Green Dashed Line ($--$):** Represents the optimized mean response time of the Next-Gen Server (Team-B).

The visual separation between the distribution curves confirms a clear behavioral shift in operational efficiency.

---

## 🔑 Key Findings & Decision Framework
* **Calculated T-Statistic ($t_{cal}$):** $\approx -5.196$ (The negative sign indicates that Team-B's response times are heavily shifted toward the accelerated/lower-latency zone).
* **Two-Tailed Critical Threshold:** $\pm 1.729$
* **Statistical Conclusion:** Since the absolute value of our calculated statistic ($| -5.196 | = 5.196$) vastly exceeds the critical boundary ($1.729$), we **Reject the Null Hypothesis ($H_0$)**.

### 💼 Data-Driven Business Impact
The performance variance between the two environments is statistically significant and highly reproducible. The next-generation server guarantees a genuine upgrade in execution speed. This statistical proof provides corporate leadership with the green light to confidently allocate budget for full-scale infrastructure migration and legacy decommissioning.

---

## 🚀 How to Run & Replicate
1. Clone this repository to your local environment.
2. Install the required data science packages:
   ```bash
   pip install numpy scipy seaborn matplotlib
