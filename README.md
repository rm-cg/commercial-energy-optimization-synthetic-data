# Commercial Energy Optimization Synthetic Data
A synthetic data model and Python generator simulating commercial energy consumption using thermodynamic principles.

# Abstract
Commercial real estate infrastructure accounts for a massive portion of global energy consumption, but proprietary restrictions make high-fidelity data scarce. This project introduces a rigorous mathematical framework and a highly scalable Python-based synthetic data generator to simulate realistic commercial energy consumption across a diverse portfolio of buildings. The resulting datasets allow for advanced machine learning research and infrastructure optimization without relying on confidential operational data.

# The Mathematical Framework
To ensure strict physical realism, this data generator was programmed using first-principles physics and economic algorithms:

**Diurnal Weather Engine**: Uses a solar-synchronized sine wave to accurately model 24-hour ambient temperature fluctuations.

**Probabilistic Occupancy:** Instead of uniform distributions, human arrivals are mathematically constrained using a capacity-bounded Poisson distribution to simulate the bursty, clustered nature of real-world commercial traffic.

**Thermodynamic Heat Load:** Strictly adheres to ASHRAE thermal comfort standards by calculating the 100 Watts of sensible heat generated per human occupant.

**Thermal Velocity (dT/dt):** A custom calculus-based parameter that measures how fast the temperature is rising to simulate the massive "HVAC kinetic overdrive" (Pull-down load) required to overcome a building's thermal inertia.

# Real-World Messiness & Omitted Variable Bias
To transcend theoretical perfection, continuous randomized Gaussian noise (±2% standard deviation) was applied to all simulated meter readings to mimic imperfect real-world sensors.

Crucially, the dataset was injected with two intentional "Omitted Variable Biases" that were permanently deleted from the final datasets prior to export:

**Faulty Insulation Multiplier:** A hidden penalty multiplying total energy consumption by 1.15 to 1.30 for 20% of older buildings to simulate undetected infrastructure degradation.

**Unreported Overtime Multiplier:** A hidden variable that secretly increases energy consumption by 20% between 18:00 and 21:00 to simulate employees staying late without logging it.

# Business Value & Optimization
By training a predictive linear regression model strictly on observed features (weather and occupancy), this project established a distinct prediction ceiling. Because the model cannot "see" the deleted insulation data, its massive prediction failures accurately flag the hidden anomalies.

This demonstrates how facilities managers can use intentional prediction residual errors as an Automated Anomaly Detection tool to find degraded infrastructure, and leverage Real-Time Pricing constraints to optimize peak load shifting.
