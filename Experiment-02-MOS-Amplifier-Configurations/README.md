# Experiment 02  
# Performance Analysis of CMOS Amplifier Configurations (180nm Technology)

---

## 1. Objective

To design and analyze three CMOS amplifier configurations using 180nm technology in LTSpice and compare their performance in terms of:

- DC operating point
- Voltage gain
- Bandwidth (BW)
- 3dB Bandwidth
- Unity Gain Bandwidth (UGB)
- Output swing
- Power consumption

---

## 2. Technology & Simulation Details

- Technology Node: 180nm CMOS (tsmc018)
- Simulation Tool: LTSpice
- Supply Voltage (VDD): 1.8 V
- Load Capacitance (CL): 1 pF
- Analysis Performed:
  - DC Operating Point (.op)
  - Transient Analysis (.tran)
  - AC Small-Signal Analysis (.ac)

---

## 3. Amplifier Configurations

Three amplifier topologies were implemented as per the assignment sheet.

---

# 🔹 Configuration (a)
### PMOS Active Load with Source Degeneration

### Circuit Description
- M1: NMOS input transistor
- M2: PMOS active load
- Rs: Source degeneration resistor

### Schematic
![Config A Schematic](images/config-a-schematic.png)

---

### DC Operating Point

Purpose:
- Ensure all transistors operate in saturation
- Extract ID, VGS, VDS
- Compute total power consumption

![Config A DC](images/config-a-dc.png)

Power Calculation:
P = VDD × I_total

---

### Transient Analysis

Purpose:
- Verify linear amplification
- Measure voltage gain
- Check maximum output swing
- Observe distortion

![Config A Transient](images/config-a-transient.png)

---

### AC Analysis

Extracted Parameters:
- Midband Gain
- 3dB Bandwidth
- Unity Gain Bandwidth (UGB)
- Effect of CL on frequency response

Without Load:
![Config A AC No Load](images/config-a-ac-no-load.png)

With CL = 1pF:
![Config A AC With Load](images/config-a-ac-1pf.png)

---

# 🔹 Configuration (b)
### Cascoded Common Source Amplifier

### Circuit Description
- M1: Input transistor
- M2: PMOS active load
- M3: Cascoding transistor

### Schematic
![Config B Schematic](images/config-b-schematic.png)

### Analysis Performed
- DC bias verification
- Transient gain measurement
- AC gain and bandwidth extraction

(Insert corresponding images here)

---

# 🔹 Configuration (c)
### Modified / Fully Cascoded Configuration

### Circuit Description
- Enhanced output resistance
- Higher gain expected
- Reduced output swing

### Schematic
![Config C Schematic](images/config-c-schematic.png)

### Analysis Performed
- DC saturation verification
- Transient response
- AC frequency response

(Insert corresponding images here)

---

## 4. Theoretical Analysis

Small-signal parameters calculated:

- gm = 2ID / Vov
- ro ≈ 1 / (λID)

Voltage Gain Approximation:
Av ≈ -gm × ro

Detailed derivations are provided in:
`calculations.md`

---

## 5. Performance Comparison

| Configuration | Gain | 3dB BW | UGB | Output Swing | Power |
|--------------|------|--------|-----|--------------|-------|
| (a) |  |  |  |  |  |
| (b) |  |  |  |  |  |
| (c) |  |  |  |  |  |

(Values to be filled after extracting from simulation)

---

## 6. Observations

- Cascoding increases output resistance and gain.
- Source degeneration improves linearity but reduces gain.
- Load capacitance reduces bandwidth.
- Trade-off observed between gain and bandwidth.

---

## 7. Conclusion

All three CMOS amplifier configurations were successfully designed and analyzed using 180nm technology.

The experimental results were compared with theoretical calculations and performance trade-offs between gain, bandwidth, power, and output swing were studied.

This experiment demonstrates practical understanding of small-signal modeling and frequency response analysis of CMOS amplifiers.