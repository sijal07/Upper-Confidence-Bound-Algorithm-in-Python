# Upper-Confidence-Bound-Algorithm-in-Python



# Upper Confidence Bound (UCB) for Online Ads Optimization

This project demonstrates the use of the **Upper Confidence Bound (UCB)** algorithm to solve the *Multi-Armed Bandit Problem* for online advertisement selection.  

The algorithm balances **exploration** (trying out different ads) and **exploitation** (choosing the best-performing ads) to maximize the click-through rate (CTR).

---

## 📌 Project Overview
- **Dataset**: `Ads_CTR_Optimisation.csv`  
  Contains simulated click-through data for 10 different ads.  
- **Algorithm Used**: Upper Confidence Bound (UCB).  
- **Goal**: Identify the ad with the highest CTR while minimizing wasted impressions.  

---

## ⚙️ How It Works
1. At each round:
   - For each ad, the algorithm computes:
     - **Average Reward** (observed CTR so far).  
     - **Confidence Interval (delta)**, which decreases as an ad is selected more often.  
   - The ad with the **highest upper bound** is selected.  
2. This ensures:
   - **Exploration**: Ads with fewer trials are given a higher confidence interval.  
   - **Exploitation**: Ads with higher rewards are selected more often as confidence grows.  

---

## 📊 Visualization
The code plots a histogram of how many times each ad was selected during the simulation:
📈 Results

The histogram shows which ad performs best.

The algorithm converges to the ad with the highest click-through rate.

Total Reward reflects the number of successful clicks obtained.

🔮 Future Improvements

Compare UCB with Thompson Sampling.

Apply on larger real-world datasets.

Extend to contextual bandits for personalized ad recommendations.
