# F1Tenth-MC-Scheduling
Google Colab implementation of physics-informed mixed-criticality scheduling for F1Tenth cars, replicating and extending RTAS 2025. Includes EDF scheduler with mode switching, simplified 2D vehicle and LiDAR simulation, crash probability analysis, and visualizations.
------

# Physics-Informed Mixed-Criticality Scheduling for F1Tenth Cars

This repository contains a **Google Colab implementation** that replicates and extends the research paper:

> *Physics-Informed Mixed-Criticality Scheduling for F1Tenth Cars with Preemptable ROS 2 Executors (RTAS 2025)*

The project demonstrates how **real-time scheduling** directly impacts the **safety of cyber-physical systems** like autonomous cars.  
It is designed to showcase my ability to **understand, implement, and extend cutting-edge research** in **real-time systems and autonomous vehicles**.

---

## 🚗 Key Features
- **Preemptive EDF Scheduler** with **mode switching** (low vs high criticality).
- **Task set replication** (Driver, Health, Dummy tasks) based on RTAS 2025.
- **2D Vehicle Simulation** with simplified kinematics.
- **LiDAR-based hazard detection** to trigger physics-informed mode switching.
- **Monte Carlo Safety Analysis** comparing crash probability with vs without switching.
- **Visualizations** for publication-ready figures.

---

## 📊 Results

### 1. Task Scheduling (Gantt Chart)
EDF schedules the Driver, Health, and Dummy tasks.  
With mode switching, the Driver period shrinks and Dummy1 is dropped → faster reaction time.

![Gantt Chart Example]

<img width="4800" height="1800" alt="gantt_schedule" src="https://github.com/user-attachments/assets/07b248fc-803a-4107-afe0-d57aa3771f5b" />

---

### 2. Vehicle Trajectory
Car path on a 2D corridor.  
- Without switching → delayed reaction → higher crash chance.  
- With switching → car adapts, stays safe.

![Trajectory Comparison]
<img width="3000" height="1800" alt="car_trajectory" src="https://github.com/user-attachments/assets/48ad2b5b-5532-45c1-82ca-bdb11e6db034" />

---

### 3. Crash Probability (Monte Carlo Simulation)
Statistical safety evaluation.  
Mode switching significantly reduces crashes. (Numbers depend on simulation seeds.)

![Crash Probability]
<img width="2400" height="1800" alt="monte_carlo_crash_probability_from_func" src="https://github.com/user-attachments/assets/6eb02c36-d2e3-4e21-a27c-d4c86c5afadb" />

---

## 🛠️ How to Run
1. Open the Colab Notebook.
2. Run all cells (runtime < 10 minutes for N=50, 10s per episode).
3. Generated figures are saved in the `figures/` folder.

---

## 🔮 Extensions
- Multi-core EDF scheduling.
- Comparison with fixed-priority scheduling.
- GPU-accelerated inference (PyTorch dummy model).
- Varying dummy task loads to stress-test schedulability.

---

## 🎯 Why This Matters
This project illustrates the **core principle** of the RTAS 2025 paper:  
> *Bridging the gap between computational scheduling and physical safety in cyber-physical systems.*

By replicating and extending the results, I demonstrate ability in:
- Real-time systems  
- Embedded/autonomous systems  
- Safety-critical scheduling and verification  

---

## 📧 Contact
*Md. Mehedi Hasan*  
Prospective PhD Student – Real-Time Systems & Cyber-Physical Systems  
Email: [mehedi.hasan.ict@mbstu.ac.bd]  
Portfolio: [Link](https://md-mehedi-hasan-resume.vercel.app/)  
