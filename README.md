# Quadrature Down Converter (QDC)

A Quadrature Down Converter (QDC) designed and simulated using operational amplifiers, MOSFET-based mixers, and RC low-pass filters to perform frequency translation and recover in-phase (I) and quadrature-phase (Q) intermediate frequency (IF) signals.

---

## Authors

- Shreya Vinoj (2025102046) — shreya.vinoj@students.iiit.ac.in  
- Ardra P (2025102106) — ardra.p@students.iiit.ac.in  
- Sayana Sajan (2025102094) — sayana.sajan@students.iiit.ac.in  

---

## Abstract

This project presents the design and implementation of a Quadrature Down Converter (QDC) using a quadrature oscillator, switching MOSFET mixers, and RC low-pass filters. The system generates 90° phase-shifted local oscillator signals, performs frequency translation of an input RF signal, and extracts intermediate-frequency components. The design is validated using LTspice simulations and laboratory measurements.

---

## Objective

- Generate in-phase (I) and quadrature-phase (Q) local oscillator signals  
- Perform frequency downconversion of an input RF signal  
- Extract IF components using low-pass filtering  
- Validate system behavior through simulation and hardware results  

---

## System Overview

The QDC consists of three main stages:

- Quadrature Oscillator → Generates 90° phase-shifted LO signals  
- Mixer Stage → Performs frequency translation using MOSFET switching  
- Low-Pass Filter → Extracts difference frequency (IF signal)  

Final outputs:
- IF Final (In-phase component)
- QF Final (Quadrature component)

---

## Quadrature Oscillator

- Implemented using an op-amp based double-integrator topology  
- Generates sine and cosine outputs with 90° phase difference  
- Designed for oscillation frequency ≈ 150 kHz  

### Key Parameters
- R = 1 kΩ  
- C = 1 nF  
- Oscillation frequency: ~150 kHz  

### Result
- Frequency obtained: ~151 kHz  
- Phase difference: ~90° (approx. 100° observed in practice)

---

## Mixer Stage

- MOSFET-based switching mixer  
- Multiplies input RF signal with LO signal  
- Produces sum and difference frequency components  

### Key Parameters
- Rbias = 100 kΩ  
- Vbias = 0.9 V  
- Vosc = 1 V  
- Vin = 1 V  
- RL = 1 kΩ  
- MOSFET: 0.18 µm, Vth ≈ 0.4 V  

### Output
- Frequency components observed at |fosc − fin|  
- Verified through FFT analysis in LTspice and hardware

---

## Low-Pass Filter

- RC filter used to remove high-frequency components  
- Passes only the IF signal after mixing  

### Design Values
- R = 50 Ω  
- C = 1 µF  
- Cutoff frequency: ~3 kHz  

### Result
- Low frequencies passed with minimal attenuation  
- High-frequency components suppressed successfully  

---

## Final System Output

The complete QDC system produces:

- IFFinal → In-phase IF signal  
- QFFinal → Quadrature IF signal  

### Observations
- Output frequency: |fosc − fin|  
- Phase difference: ~90°  
- Successful frequency downconversion achieved  

---

## Tools Used

- LTspice (simulation)
- MOSFET switching model
- Operational amplifier circuits
- RC analog filter design

---

## Key Results

- Quadrature oscillator successfully generates 90° phase-shifted signals  
- Mixer performs correct frequency translation  
- Low-pass filter extracts IF components  
- Final system validates quadrature downconversion principle  

---

## Applications

- Wireless communication receivers (Wi-Fi, Bluetooth, WLAN)  
- Direct conversion receivers  
- RF signal processing systems  
- I/Q demodulation systems  

---

## References

- Sedra & Smith – Microelectronic Circuits  
- Texas Instruments – Op-amp oscillator design notes  
- A. A. Abidi – Direct Conversion Receivers  
- Lecture notes (Analog Electronics Circuits, IIIT Hyderabad)  
- Holzel – Quadrature Oscillator Design  

---

## Acknowledgement

We thank IIIT Hyderabad, the Analog Electronics Circuits faculty, and teaching assistants for their guidance and support in completing this project.

---

## Result Summary

A fully functional quadrature down converter was successfully designed and verified using simulation and circuit analysis, demonstrating proper frequency translation and I/Q signal generation.
