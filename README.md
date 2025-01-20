# **FIR Filter Design**

**Author:** MADHAVI ARADHYULA  
**Company:** CODTECH IT SOLUTIONS  
**ID:** CT08DOW  
**Domain:** VLSI  
**Duration:** Dec 2024 to Jan 2024  
**Mentor:** SRAVANI GOUNI

---

## **Overview**

The **FIR (Finite Impulse Response) Filter** is a type of digital filter widely used in various applications such as signal processing, audio systems, and communication systems. It processes input signals by applying a finite number of coefficients (taps) and performs multiplication and summation of input data with the corresponding tap values. The design presented here implements a 15-tap **Low Pass Filter (LPF)** using **Xilinx Vivado**.

This design uses a **circular buffer** to store input samples and perform the necessary computations for each tap. It is optimized to work with a clock frequency of **1MSps** and a **cutoff frequency of 400kHz**.

---

## **Features**

- **15-tap FIR Filter:** Implements a 15-tap low pass filter (LPF).
- **Clocked Operation:** Operates on a clock signal and produces a filtered output on each clock cycle.
- **Parallel Computation:** Implements parallel accumulation and multiplication for efficient FIR computation.
- **Flexible Inputs:** Takes input samples as signed 16-bit data and outputs the filtered results as 32-bit data.
- **Control Signals:**
  - `s_axis_fir_tvalid`: Input data valid signal.
  - `m_axis_fir_tvalid`: Output data valid signal.
  - `s_axis_fir_tready`: Input ready signal.
  - `m_axis_fir_tready`: Output ready signal.
  - `s_axis_fir_tlast`: Input last signal indicating the end of data.
  - `m_axis_fir_tlast`: Output last signal indicating the end of data.

---

## **Tools Used**

- **Xilinx Vivado**: An FPGA design suite used to implement and simulate the FIR filter design.
- **Verilog**: The hardware description language used to design the FIR filter module.
- **EDA Playground**: Used for code simulation (optional).

---

## **Functional Block Diagram**

1. **Input Interface**: Receives a stream of signed 16-bit input data samples.
2. **Circular Buffer**: Stores the last 15 input samples for processing.
3. **Tap Coefficients**: Hardcoded 15 filter taps for the low-pass filter response.
4. **Multiplication Stage**: Each buffer value is multiplied by its corresponding tap coefficient.
5. **Accumulation**: The results of the multiplication are accumulated to produce the output.
6. **Output Interface**: Sends the processed data out as a 32-bit signed output, ready for the next stage.

---

##Simulation Results

![image](https://github.com/user-attachments/assets/7ce16976-e1a4-4621-8e13-e0047051d503)

