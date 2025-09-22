# Microwatt + SERDES High-Speed Link

## 📌 Overview
The **Microwatt + SERDES High-Speed Link** project extends the [Microwatt](https://github.com/antonblanchard/microwatt) open-source PowerISA CPU by integrating a **Serializer/Deserializer (SERDES)** block.  
This enables **multi-Gbps chip-to-chip communication**, addressing the limitations of parallel buses such as high pin count, skew, and signal integrity issues.  
The project demonstrates a custom FPGA interconnect bus using SERDES.

---

## 📝 Problem Statement
Microwatt currently lacks a high-speed serial communication interface. Parallel buses are limited by:  
- Excessive pin count for wide data buses.  
- Clock skew and synchronization challenges at high frequency.  
- Signal integrity degradation over long distances.  

These limitations make it difficult to achieve **high-speed chip-to-chip communication** or multi-core SoC interconnects. Incorporating a SERDES interface solves these issues by converting parallel data into high-speed serial streams, enabling reliable, scalable, and efficient data transfer.

---

## 🎯 Project Proposal
This project aims to design and integrate a **SERDES block with the Microwatt CPU core** to enable **high-speed chip-to-chip communication** for FPGA or SoC applications.  

### Objectives
- Design a functional SERDES IP core with serializer, deserializer, and clock recovery.  
- Integrate the SERDES block into the Microwatt SoC via memory-mapped registers.  
- Demonstrate stable FPGA-to-FPGA communication at multi-Gbps rates.  
- Provide an open-source, reusable IP for research and education.

### Methodology
1. **SERDES Design**  
   - Build serializer and deserializer modules.  
   - Implement clock multiplication (PLL) and clock recovery (CDR).  
   - Add optional encoding/decoding (8b/10b) and error checking.  

2. **Integration with Microwatt**  
   - Connect SERDES as a peripheral on the Microwatt bus.  
   - Provide control and status registers for configuration and monitoring.  

3. **Testing & Validation**  
   - Loopback testing for bit error rate (BER).  
   - FPGA-to-FPGA communication test for data transfer.  
   - Latency and throughput measurement to validate performance.



## 🏗️ Architecture
