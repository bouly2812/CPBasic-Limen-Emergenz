# ⚡ Signal Pipeline Specification (REV 1.2)
> **Datenfluss und Signalverarbeitung der 32-Kanal EEG/Psi-Messapparatur.**  
> *Data flow and signal processing pipeline for the 32-channel EEG/Psi sensing apparatus.*

---

## 🇩🇪 Deutsch

### Architektur des Signalpfads
Der Hardware-Aufbau des REV 1.2 Prototypen verarbeitet elektromagnetische Feldänderungen und bio-elektrische Resonanzen über einen deterministischen, rauscharmen Pfad von der Sensorik bis zur digitalen Prozessierung.

```text
[ 32x EEG COILS ] ---> [ INA128 Amplifiers ] ---> [ ADS1115 (16-bit ADC) ] ---> [ ESP32 / GPU Cluster ] ---> [ ARM Cortex-M7 CPU ] ---> [ RAM / DATA OUT ]