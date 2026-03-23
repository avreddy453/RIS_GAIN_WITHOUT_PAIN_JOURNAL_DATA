# RIS-Assisted 5G NR Experimental Dataset

This repository contains experimental data collected from an OpenAirInterface (OAI) 5G NR system integrated with a Reconfigurable Intelligent Surface (RIS). The dataset is intended to support analysis and validation of RIS-assisted wireless communication performance.

---

## 📁 Dataset Description

### 1. RIS ON
- **Single UE Throughput**
  - UE throughput when RIS beamforms toward the same UE
  - UE throughput when RIS beamforms toward the other UE
  - UE throughput when RIS sweeps between two directions  
    - All combinations of switching interval (**Ts**) and averaging window (**Tc**)

- **Dual UE Throughput**
  - Throughput of both UEs when RIS sweeps between two directions  
    - All combinations of **Ts** and **Tc**

---

### 2. RIS OFF
- **Single UE Throughput**
- **Dual UE Throughput**
  - Evaluated across all **Tc** values

---

### 3. RIS Removed
- UE throughput measured at the same UE positions as in RIS ON/OFF scenarios

---

### 4. Grid-Based UE Placement

#### RIS ON
- **00 Configuration**
  - Both UEs are outside RIS beam directions  
  - Evaluated at three distances: D1, D2, D3

- **01 / 10 Configuration**
  - One UE aligned with RIS beam, the other not  
  - Evaluated at three distances: D1, D2, D3

- **11 Configuration**
  - Both UEs aligned with RIS beam directions  
  - Evaluated at three distances: D1, D2, D3

#### RIS OFF
- Same UE positions as RIS ON case  
- Same three distances: D1, D2, D3

---

## 🧾 Notes

1. Folder and file names are self-explanatory and indicate the corresponding dataset.
2. Grid notation (00 / 01 / 10 / 11):
   - RIS alternates between two beam directions, staying **Ts seconds** in each direction.
   - `00` → Neither UE is in RIS beam direction  
   - `01 / 10` → One UE is aligned, the other is not  
   - `11` → Both UEs are aligned with RIS beam directions  

3. Distance definitions:
   - D1 < D2 < D3 (angular distance from RIS)

4. System setup:
   - Two UEs: **UE1** and **UE2**
   - UE1 positioned at **30°**
   - UE2 positioned at **60°**

5. Parameters:
   - **Ts (RIS switching interval in seconds)**: {1, 3, 5, 9, 15}
   - **Tc (EWMA throughput window size in slots)**: {200, 2000, 20000}

---

## 🎯 Purpose

This dataset is provided to enable reproducible research and deeper analysis of RIS-assisted communication systems in practical 5G NR environments.
