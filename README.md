**Overview:**

This repository contains a SimPy-based Discrete Event Simulation (DES) model of a real-life coffee shop. The simulation models customer arrivals, queue dynamics, and service processes, incorporating agent-based decision-making where customers can balk (leave upon arrival), reneg (leave after waiting), or stay in line for service. The purpose of this project is to analyze how different factors, such as the number of baristas and the proportion of rushed customers, affect customer experience and overall business performance.

**Simulaton Features:**
  - Service times are drawn from an exponential distribution with a minimum of 1 minute, a mean of 2 minutes, and a maximum of 5 minutes.
  - Balking: Customers leave if the line is too long (higher number of people in the queue than their predefined maximum).
  - Reneging: Customers leave after waiting too long (longer wait time than their predefined maximum).
  - Event logging tracks the full customer journey (arrival, wait time, service start, departure).

**Findings:**

After running multiple simulations with varying parameters, the most significant insights include:
  - More baristas = Better service: Increasing the number of baristas significantly reduced waiting times, decreased customer reneging, and increased the number of customers served.
  - More rushed customers = More balking, less reneging: A higher percentage of rushed customers led to more customers choosing not to join the line at all, but fewer customers leaving mid-wait.
  - Optimizing staff allocation matters: Adding a second barista had the biggest return in terms of efficiency and revenue potential, while adding a third barista had less of an impact.

