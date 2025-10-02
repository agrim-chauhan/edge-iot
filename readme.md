# Exploring Edge–IoT Integration with Future Telecommunication Networks for Optimized Latency

## 📌 Overview
This project investigates the integration of **Edge Computing** and the **Internet of Things (IoT)** within **future telecommunication networks (5G/6G)** to optimize latency.  
The study explores three key research questions (RQs):  

1. **Device Orchestration Patterns** – Can IoT devices be clustered based on latency and throughput performance?  
2. **Latency Drivers / Workload–Resource Tradeoffs** – Which factors (CPU, memory, task size, offload location) most strongly influence latency?  
3. **Security–Privacy Trade-offs** – Do different security schemes (TLS, DTLS, Blockchain, etc.) significantly affect latency?  

---

## 📊 Dataset
- **Entries:** 1000 synthetic records  
- **Features:**  
  - CPU usage (%)  
  - Memory usage (%)  
  - Task size (KB)  
  - Offload location (local / edge / hybrid)  
  - Latency (ms)  
  - Throughput (Mbps)  
  - Energy consumption (J)  
  - Security scheme (none, TLS, DTLS, secure element, blockchain-enabled)  

The dataset was generated to simulate realistic **edge–IoT environments**, enabling analysis of orchestration, resource management, and security trade-offs.  

---

## ⚙️ Methodology
The study used a **mixed quantitative methodology**:  

1. **K-Means Clustering** (RQ1)  
   - Latency vs Throughput used as features  
   - Devices grouped into performance clusters  
   - Identified optimized nodes, intermediate nodes, and extreme outliers  

2. **Random Forest Regression** (RQ2)  
   - Features: CPU, memory, task size, offload location  
   - Target: Latency  
   - Metrics: R², MAE  
   - Feature importance analysis to determine strongest latency drivers  

3. **One-Way ANOVA** (RQ3)  
   - Groups: Security schemes (none, TLS, DTLS, secure element, blockchain)  
   - Tested if latency means differ significantly across schemes  
   - Boxplots used for visualization  

---

## 📈 Results
- **Clustering:** Four clusters identified, with outliers showing latency > 3000 ms and near-zero throughput.  
- **Feature Importance:** Memory usage, task size, and CPU utilization explained >90% of latency variation; offload location had minimal effect.  
- **Security Trade-offs:** ANOVA confirmed significant latency differences; blockchain-based security introduced the highest delays.  

---

## 🖼️ Visualizations
1. **Device-Orchestration Clusters**  
   ![clusters](clusters.jpeg)  

2. **Feature Importance for Latency**  
   ![feature importance](feature_importance.jpeg)  

3. **Latency vs Security Scheme**  
   ![security boxplot](security_boxplot.jpeg)  

---

## 📚 References
This study is based on 30 peer-reviewed papers (2020–2025) covering **edge computing, IoT integration, 5G/6G, and security frameworks**.  
Citations follow the **IEEE numeric style**.  

---

## 🌍 Relevance to UN SDGs
The study aligns with multiple **Sustainable Development Goals (SDGs):**  
- **SDG 7 (Clean Energy):** Promotes energy-efficient IoT deployments  
- **SDG 9 (Industry & Infrastructure):** Enables resilient digital ecosystems  
- **SDG 11 (Sustainable Cities):** Supports smart city applications with low-latency IoT  
- **SDG 16 (Strong Institutions):** Ensures secure and trustworthy IoT infrastructures  

---

## 🛠️ How to Reproduce
1. Clone this repository.  
2. Open the Jupyter Notebook and run the provided Python scripts.  
3. Use `plt.savefig()` to export plots.  
4. Upload plots into Overleaf and insert using LaTeX (`\includegraphics`).  

---

## ✨ Conclusion
The project demonstrates that **optimized latency** in edge–IoT systems requires:  
- Intelligent orchestration (cluster detection of bottlenecks)  
- Efficient resource–workload management at device level  
- Security protocols optimized for both **trust** and **responsiveness**  

This work bridges academic research with practical system design for **5G/6G-enabled IoT**, ensuring scalable, secure, and sustainable deployments.  
