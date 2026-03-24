# RIS-Assisted 5G NR Experimental Dataset

This repository contains experimental data collected from an OpenAirInterface (OAI) 5G NR system integrated with a Reconfigurable Intelligent Surface (RIS). The dataset is designed to support analysis and validation of RIS-assisted wireless communication systems.

---

## 📁 Dataset Organization

The dataset is divided into two main scenarios:
- **Single User Scenario**
- **Two User Scenario**

Each scenario contains:
- 📄 Log files  
- 📊 Throughput (throughput) files  

---

## 🔬 Experimental Cases

### 1. RIS ON

#### Single User Scenario
- UE performance when RIS beamforms toward the same UE  
- UE performance when RIS beamforms toward another direction  
- UE performance when RIS sweeps between two directions  
  - Includes all combinations of **Ts** and **Tc**

#### Two User Scenario
- Performance of both UEs when RIS sweeps between two directions  
  - Includes all combinations of **Ts** and **Tc**

---

### 2. RIS OFF

#### Single User Scenario
- UE performance without RIS

#### Two User Scenario
- Performance of both UEs  
  - Evaluated across all **Tc** values

---

### 3. RIS Removed

#### Single User Scenario
- UE performance at the same position as RIS ON/OFF cases

---

### 4. Grid-Based UE Placement

#### RIS ON

- **00 Configuration**
  - Both UEs are outside RIS beam directions  
  - Distances: D1, D2, D3  

- **01 / 10 Configuration**
  - One UE aligned with RIS beam, the other not  
  - Distances: D1, D2, D3  

- **11 Configuration**
  - Both UEs aligned with RIS beam directions  
  - Distances: D1, D2, D3  

#### RIS OFF
- Same UE placements as RIS ON  
- Same distances: D1, D2, D3  

---

## 📏 Experimental Geometry

- Distance between **RIS and Base Station**: **170 cm**  
- Distance between **RIS and UE1**: **152 cm**  
- Distance between **RIS and UE2**: **162 cm**

### Grid-Based Distances

Distances are defined for each UE as follows:

- **D1**
  - UE1: 122 cm  
  - UE2: 132 cm  

- **D2**
  - UE1: 152 cm  
  - UE2: 162 cm  

- **D3**
  - UE1: 182 cm  
  - UE2: 192 cm  

---

## 🧾 Notes

1. Folder and file names indicate the corresponding scenario and configuration.
2. Grid notation (00 / 01 / 10 / 11):
   - RIS switches between two beam directions, staying **Ts seconds** in each direction.
   - `00` → Neither UE in RIS beam direction  
   - `01 / 10` → One UE aligned, one not  
   - `11` → Both UEs aligned  

3. Distance definition:
   - D1 < D2 < D3 (angular distance from RIS)

4. System setup:
   - Two UEs: **UE1 (30°)** and **UE2 (60°)**

5. Parameters:
   - **Ts (RIS switching interval in seconds)**: {1, 3, 5, 9, 15}  
   - **Tc (EWMA throughput window size in slots)**: {200, 2000, 20000}  

---

## 🎯 Purpose

This dataset enables reproducible research and performance evaluation of RIS-assisted communication in practical 5G NR systems.
