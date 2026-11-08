# 32-CH EEG Magnetic Sensing Prototype (REV 1.2) - Hardware Specification
# Stückliste & System-Spezifikationen (Build Cost: 1485 EUR)

---

## 🇩🇪 Deutsch / 🇬🇧 English

### System Architecture Block Diagram
```text
[32x EEG COILS (CH1-CH32)] 
         │
         ▼
[32x INA128 AMPLIFIER ARRAY (Low Noise, Gain ~1000x)]
         │
         ▼
[ADS1115 16-BIT ADC MODULES (I²C Bus, 860 SPS)]
         │
         ▼
[ESP32-WROOM MAIN CONTROLLER (Wi-Fi/BLE, 240 MHz Dual-Core)]
         │
         ▼
[DUAL GPU CLUSTER O1/O2 (Edge Processing)]
         │
         ▼
[DUAL CPU CORE Fp1/Fp2 (ARM Cortex-M7 Signal Compute)]
         │
         ▼
[SYSTEM RAM P3/P4 (16GB DDR4 SDRAM)] ──► [DATA OUT / SD LOGGING]
Bill of Materials (BOM) / StücklisteComponent / BauteilSpecifications / DetailsQty / Anz.Unit Cost (€)Total (€)EEG Coil Assemblies20cm diameter, 1000 turns Cu wire3215.00480.00$\Psi$ Sensor Array3-Axis Magnetometer ($\Psi_x, \Psi_y, \Psi_z$)3120.00360.00INA128 Instrumentation AmpLow-noise IC, gain adjustable ~1000x320.8126.00ADS1115 ADC Board16-Bit ADC, 4-Channel, $I^2C$ interface81.7514.00ESP32-WROOM BoardWi-Fi/BLE, dual-core micro-controller116.0016.00Edge GPU Modules (O1/O2)Edge processing GPU acceleration units2190.00380.00ARM Cortex-M7 CPUsFp1/Fp2 signal processing cores255.00110.00DDR4 SDRAM Modules8GB DDR4 RAM (P3/P4 channels)242.0084.00PCB, Passives & ConnectorsMultilayer PCB, shielding, structural enclosure1115.00115.00TOTAL BUILD COSTRev 1.2 Full Prototype Build----1485.00 €Hardware ParametersSampling Rate: 250 SPS per channel (24-bit effective resolution via ADS1115 oversensing pipeline).Primary Field Vectoring: 3-Axis magnetic sensing via $\Psi_{x,y,z}$ coils measuring dynamic state transitions across threshold $\Lambda_{crit}$.Connectivity: MicroSD local buffering, Wi-Fi telemetry, USB-C raw stream out.