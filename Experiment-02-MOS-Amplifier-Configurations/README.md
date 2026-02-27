# Experiment 02  
## Performance Analysis of CMOS Amplifier Configurations (180nm Technology)

---

## Objective

To design and analyze three CMOS amplifier configurations using 180nm technology in LTSPICE and evaluate their performance in terms of gain, bandwidth, output swing, and power consumption.

---

## Design Specifications

- Technology: 180nm CMOS
- Simulation Tool: LTSPICE
- Supply Voltage (VDD): 1.8 V
- Load Capacitance (CL): 1 pF
- Bias Voltages: As per design requirements

---

## Circuit Configurations

Three amplifier topologies were implemented and analyzed:

### Configuration (a)
## Configuration (a): PMOS Active Load with Source Degeneration

### Circuit Schematic
![Schematic](images/config-a-schematic.png)

### DC Operating Point
![DC Analysis](images/config-a-dc.png)

### Transient Analysis
![Transient](images/config-a-transient.png)

### AC Analysis (No Load)
![AC No Load](images/config-a-ac-no-load.png)

### AC Analysis (CL = 1pF)
![AC With 1pF](images/config-a-ac-1pf.png)

### Configuration (b)
Common-source amplifier with active load for improved gain.  
(Schematic: configuration-b.png)

### Configuration (c)
Modified / Cascoded configuration to enhance output resistance and voltage gain.  
(Schematic: configuration-c.png)

---

## DC Operating Point Analysis

DC simulation was performed to:

- Ensure all MOSFETs operate in saturation region.
- Extract drain current (ID), VGS, and VDS.
- Verify proper biasing.
- Calculate total power dissipation.

Power Consumption:
P = VDD × I_total

(Refer: dc-analysis.png)

---

## Transient Analysis

Transient simulation was carried out using a small-signal sinusoidal input to:

- Verify linear amplification.
- Measure voltage gain (Av = Vout / Vin).
- Determine maximum output swing.
- Observe signal distortion (if any).

(Refer: transient-analysis.png)

---

## AC Small-Signal Analysis

AC sweep analysis was performed to extract:

- Midband Gain
- 3dB Bandwidth
- Unity Gain Bandwidth (UGB)
- Gain roll-off characteristics
- Effect of load capacitance on frequency response

(Refer: ac-analysis.png)

---

## Theoretical Calculations

Small-signal parameters such as gm and ro were calculated.

Theoretical Gain Approximation:
Av ≈ -gm × ro

Detailed hand calculations are provided in:
`calculations.md`



## Conclusion

The three CMOS amplifier configurations were successfully designed and analyzed using 180nm technology in LTSPICE.  
A trade-off between gain, bandwidth, power consumption, and output swing was observed.  
The results were compared with theoretical expectations to validate the design.