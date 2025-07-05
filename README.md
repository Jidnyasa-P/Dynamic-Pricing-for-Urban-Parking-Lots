# 🚗 Dynamic Pricing for Urban Parking Lots

> A real-time intelligent pricing system for 14 urban parking spaces using live data streams, built as part of the **Summer Analytics 2025 Capstone Project** hosted by the Consulting & Analytics Club × Pathway.

---

## 🧠 Overview

Urban parking spaces often suffer from inefficient fixed pricing models. To optimize utilization and reduce congestion, this project implements a **dynamic, data-driven pricing engine** that adjusts parking fees based on:
- Real-time occupancy and queue length
- Environmental and event-based signals (traffic, special days)
- Vehicle type
- Nearby competitor pricing

The system is simulated in real-time using **Pathway**, with models written from scratch using only **NumPy, Pandas, and Python**.

---

## ⚙️ Tech Stack

| Tool/Library      | Purpose                               |
|------------------|----------------------------------------|
| **Python**        | Core programming language              |
| **Pandas / NumPy**| Data processing, math operations       |
| **Pathway**       | Real-time data streaming & ingestion   |
| **Bokeh**         | Real-time visualizations               |
| **Google Colab**  | Development & simulation environment   |
| **GitHub**        | Code collaboration and documentation   |
| **Mermaid**       | Architecture diagram                   |

---

## 🧱 Architecture Diagram
![Untitled diagram _ Mermaid Chart-2025-07-05-120722](https://github.com/user-attachments/assets/c19fa8db-1fde-4ad1-ac07-3a034c686c70)

## 🏗️ Project Architecture & Workflow

### 🔄 Data Stream Simulation

* The CSV file simulates 73 days of parking activity across 14 lots at 30-min intervals.
* We replay the data using `Pathway.replay_csv()` to simulate real-time streaming input.

### 🧠 Pricing Models

1. **Model 1 – Baseline Linear**

   * Price increases linearly with occupancy
   * Acts as a simple benchmark

2. **Model 2 – Demand-Based**

   * Adds factors like queue length, traffic, special day, and vehicle type
   * Calculates a normalized demand score to scale price

3. **Model 3 – Competitive Pricing**

   * Incorporates lat-long proximity using Haversine distance
   * Adjusts price based on nearby competitor prices (simulated)
   * Can optionally suggest rerouting when full

### 📊 Real-Time Visualization

* Bokeh plots show real-time pricing over time.
* Visual feedback confirms model responsiveness.

---

## 🚀 How to Run

1. Clone the repo
2. Open `Model_1.ipynb`, `Model_2.ipynb`, or `Model_3.ipynb` in Google Colab
3. Upload `dataset.csv` (provided)
4. Run the notebook to stream and visualize the pricing engine

---

## 📂 Folder Structure

```
📦 urban-parking-pricing
├── dataset.csv
├── Model_1.ipynb
├── Model_2.ipynb
├── Model_3.ipynb
├── README.md
└── problem statement.pdf (optional)
```

---

## 📄 Additional Documentation

* [Pathway Docs](https://pathway.com/developers/)
* [Bokeh for Real-Time Plotting](https://docs.bokeh.org/)
* [Summer Analytics 2025](https://www.caciitg.com/sa/course25/)

---

## 🏁 Final Notes

This project demonstrates how **machine learning + real-time systems** can address real-world urban issues using simple but powerful algorithms. All models are interpretable and built from scratch — no black-box ML libraries used.

> For any questions, contact [Jidnyasa Patil](mailto:jidnyasapatil019@gmail.com)
