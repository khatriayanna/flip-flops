#  Flip-Flops & Shift Registers in Verilog

##  Overview
This project covers the Verilog design, simulation, and verification of **D, T, and JK Flip-Flops**, along with a **4-bit Shift Register**.  
Each flip-flop is modeled using both **Behavioral** and **Structural (Hierarchical)** design styles.

---

##  Features
- D Flip-Flop (Behavioral)
- T Flip-Flop (Structural, using D-FF)
- JK Flip-Flop (Behavioral)
- 4-bit Serial Shift Register
- Includes simulation testbenches & timing waveforms
- Synthesis reports showing delay and area

---

###  Flip-Flop
A flip-flop stores one bit of data and changes output on a **clock edge**.

**Example – D Flip-Flop**
\[
Q_{next} = D
\]

**Example – T Flip-Flop**
\[
Q_{next} = T \oplus Q
\]

###  Shift Register
A shift register is a chain of flip-flops that shifts data serially with each clock pulse.

---

##  Design Summary

| Circuit | Modeling Style | Description |
|----------|----------------|--------------|
| D Flip-Flop | Behavioral | Using `always @(posedge clk)` |
| T Flip-Flop | Structural | Built using internal D-FF |
| JK Flip-Flop | Behavioral | Implements classic JK logic |
| 4-bit Shift Register | Behavioral | Uses 4 D-FFs in series |

---

## Simulation Results

###  Waveforms
**D Flip-Flop:**
![DFF Waveform](../sim/waveform_dff.png)

**T Flip-Flop:**
![TFF Waveform](../sim/waveform_tff.png)

**4-bit Shift Register:**
![Shift Register Waveform](../sim/waveform_shiftreg.png)

---

##  Synthesis & RTL Analysis

### Example Vivado Report
| Module | LUTs | FFs | Delay (ns) |
|:--------|:------|:-----|:------------|
| D Flip-Flop | 2 | 1 | 1.8 |
| T Flip-Flop | 3 | 1 | 2.1 |
| JK Flip-Flop | 3 | 1 | 2.4 |
| 4-bit Shift Register | 8 | 4 | 2.8 |

**RTL Schematic Example:**

---

##  Tools Used
- **HDL:** Verilog  
- **Simulator:** ModelSim / Vivado  
- **Waveform Viewer:** GTKWave  
- **Synthesis Tool:** Vivado  

---

##  Files
| Folder | Description |
|---------|-------------|
| `/src` | Verilog source codes (`d_ff.v`, `t_ff.v`, `jk_ff.v`, `shift_register.v`) |
| `/tb` | Testbench files for all circuits |
| `/sim` | Simulation screenshots and `.vcd` files |
| `/docs` | RTL schematic and synthesis reports |

---

##  Learning Outcome
- Understand **edge-triggered sequential logic**  
- Implement **modular and hierarchical design** in Verilog  
- Gain exposure to **timing, propagation delay, and setup analysis**

---

** Designed by:** *Ayanna Khatri*  
**Field:** *VLSI / Digital System Design*
