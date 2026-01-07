This is a simulation I created  to learn about various elements such as LTspice, LLC converters, ZVS, Heatsink calculations, EMI filters, Inrush current limiting and FFT analysis.

Synchronous rectifiers can be used instead of diodes to increase efficiency. Additionally, inrush current can be limited by using a thyristor instead of a soft starter.

# Technical Specifications

Input Voltage:  115V AC (RMS) - (3-Phase, 400 Hz)

DC Bus Voltage: 265V (Nominal) , (1V Peak to Peak Ripple)

Output Voltage: 28V DC (Nominal) , (150mV Peak to Peak Ripple)

Output Power: 750 W

Efficiency: %86 ( No Synchronous rectification ) 

Power Factor(PF): %93.33

Resonant Frequency: 100 kHz

Switching Frequency: 100 kHz

Transformer Ratio: 3.66

Soft-Start Delay: 50 ms

Switching Delay: 100 ms

# Key Features

*3-Phase 400Hz Input Stage:* Includes a comprehensive EMI/EMC protection layer with a Varistor, X/Y safety capacitors, and a Common Mode Choke (CMC).

*Active Soft-Starter:* A MOSFET-based bypass circuit limits inrush current during the initial charging of the bulk capacitor.

*Precision LLC Tank:* Designed with an $10\mu\text{H}$ resonant inductor ($L_r$) and a $250\text{nF}$ resonant capacitor ($C_r$) to achieve Zero Voltage Switching (ZVS) at $100\text{kHz}$.

*High-Power Rectification:* Utilizes STTH30R06 ultra-fast recovery diodes in a center-tapped secondary configuration for high-current handling.

*Multi-Stage Output Filtering:* Employs an $L-C-L$ filter structure to drastically reduce high-frequency switching ripple on the $28\text{V}$ output rail.

*Integrated Performance Analytics:* Built-in .measure scripts automatically calculate Efficiency, Power Factor (PF), and Active/Reactive Power directly within LTspice.

# Simulation Results

The simulation demonstrates the transition from a non-loaded state to a full-load operation starting at 100ms

*Input Stability:* The 25mH input inductor and 330uF bulk capacitor provide significant damping, though they exhibit a low-frequency resonance during the step-load transition.

*Ripple Performance:* The added 2uH and 1uH output inductors effectively "thin out" the switching noise, providing a clean DC voltage for sensitive electronics.

*Efficiency:* Measured using the ratio of P_load to P_Vin after the system reaches a steady state.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Vout
<img width="2531" height="630" alt="Vout" src="https://github.com/user-attachments/assets/77693d38-1f01-4523-acd5-7059d7f99801" />

