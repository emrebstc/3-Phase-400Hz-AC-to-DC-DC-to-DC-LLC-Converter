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

*Precision LLC Tank:* Designed with an 10uH resonant inductor Lr and a 250nF resonant capacitor Cr to achieve Zero Voltage Switching (ZVS) at 100kHz.

*High-Power Rectification:* Utilizes STTH30R06 ultra-fast recovery diodes in a center-tapped secondary configuration for high-current handling.

*Multi-Stage Output Filtering:* Employs an $L-C-L$ filter structure to drastically reduce high-frequency switching ripple on the $28\text{V}$ output rail.

*Integrated Performance Analytics:* Built-in .measure scripts automatically calculate Efficiency, Power Factor (PF), and Active/Reactive Power directly within LTspice.

# Simulation Results

The simulation demonstrates the transition from a non-loaded state to a full-load operation starting at 100ms

*Input Stability:* The 25mH input inductor and 330uF bulk capacitor provide significant damping, though they exhibit a low-frequency resonance during the step-load transition.

*Ripple Performance:* The added 2uH and 1uH output inductors effectively "thin out" the switching noise, providing a clean DC voltage for sensitive electronics.

*Efficiency:* Measured using the ratio of P_load to P_Vin after the system reaches a steady state.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
1)Circuit
<img width="2484" height="804" alt="Devre" src="https://github.com/user-attachments/assets/b268c074-e3d6-447b-a576-471f09ab45da" />
2)Results
<img width="1097" height="355" alt="Data" src="https://github.com/user-attachments/assets/a910afa8-62ec-4a41-ab46-f15312fb4067" />
3)Vout
<img width="2531" height="630" alt="Vout" src="https://github.com/user-attachments/assets/77693d38-1f01-4523-acd5-7059d7f99801" />
4)Vin
<img width="2536" height="630" alt="Vin" src="https://github.com/user-attachments/assets/63e4e0ff-e290-4671-9690-96c69c2c7f9f" />
5)Soft-Switching
<img width="2492" height="628" alt="SoftSwitch" src="https://github.com/user-attachments/assets/51e1569b-09a8-4491-83c5-30ec872b1290" />
6)Current of Primary Coil and LLC Circuit
<img width="2499" height="635" alt="I_Primer" src="https://github.com/user-attachments/assets/863ff1e3-2e4f-4f03-a00b-08aa46b2547a" />
7)V-I Characteristic Graph of the L1
<img width="2534" height="632" alt="V-I-L1" src="https://github.com/user-attachments/assets/f19c4d96-bd87-4004-b9df-9ee64d5cbae7" />
8)Vout FFT
<img width="2040" height="884" alt="Vout_FFT" src="https://github.com/user-attachments/assets/ed0beb14-283e-4c69-bb52-bd4540a172c7" />
9)L1 FFT
<img width="2081" height="881" alt="L1_FFT" src="https://github.com/user-attachments/assets/859a5235-a933-452e-83ee-8b42f1d74ace" />
