marp_content = """

---
marp: true

theme: gaia

paginate: true
---

# **Coffee Shop Simulation**
### A Discrete Event Simulation Strategy

**Team Members:**
Julia O Keeffe, Paul Yaginuma, Graham Lovell, Su Hyun Byeon, & Jacob Zott

![Latte Art](https://upload.wikimedia.org/wikipedia/commons/thumb/9/98/Latte_with_winged_tulip_art.jpg/440px-Latte_with_winged_tulip_art.jpg)


---

# **Introduction**
## Why Simulate a Coffee Shop?

- Coffee shops handle **volatile variable demand** throughout each day.
- Customers have different **rushed levels** and **ordering preferences**.
- Baristas and **queue dynamics**impact service times.
- **Discrete Event Simulation (DES)** helps us analyze and optimize performance.

---

# **Problem**
## What Are We Trying to Accomplish?

We are trying to build a **realistic coffee shop simulation** that models the following:
- Customer **arrival patterns** (rush hours vs slow hours)
- Queue behavior: **joining the line, balking, or reneging**
- **Mean Service Times** based on the number of baristas working
- The **impact of baristas available** on wait times and served customers

---

# **Model Setup**
## Key Variables and Assumptions Made

- **Inter Arrival Times:** When customers arrived and determined by "peak" or "slow" demand
- **Service Times:** How long it takes a barista to serve a customer
- **Items:** Different coffee items that vary in the time it takes to make them (americano vs latte)
- **Customer Behavior:** Will a customer join the line and receive their order, join and leave, or never join
- **Percent Rushed (Prushed):** How does a customer being rushed determine their behavior?

---

# **Logic Used in the Simulation**
## How Does the Model Work?

Using **SimPy**, we defined the following:
1. **Customer Arrivals:** Customers enter based on inter-arrival time distribution
2. **Queue Decisions:** A customer will **join the line, balk, or reneg** based on conditions
3. **Service:** The barista(s) serves the next customer in line
4. **Event Logging:** Every action is recorded so we can analyze performance

---

# **Results**
## Our Results and Findings

- **Queue Length Significantly Impacts Balking and Reneging:**
  - Long lines led to **increased number of customers balking or reneging**
- **Barista Availability Affects Wait Times:**
  - Adding extra baristas **decreases average wait times**

---

# **Recommendations**
## How Can We Improve the System?

- **Adjust Staffing to Account for Peak Hours:** More baristas during peak hours would reduce wait times and improve served customer numbers
- **Add Menu Items for More Realistic Results:** Lattes take more time to create and serve than an americano for example. Adding variables for menu items would provide more realistic results
- **Customer Management Improvements:* Provide estimated wait time to reduce reneging.

---

# **Challenges**
## Key Issues

- **Balking and Reneging Metrics:**
  - Initial resuls did not produce realistic metrics in consumer behaviors
- **Data Analysis and Debugging:**
  - We spent a large amount of effort and time on the debugging and stress testing analysis
  - Eventually solved the issue in the balking logic, but it took many attempts to solve this

---

# **Conclusion**

- **Simulation is a near-realistic coffee shop simulation**
- **Queue management and barista availability significantly impact all metrics**
- **Mean Service Time in relation to menu items and several other key variables could refine the model further**

Thank you!

---

"""