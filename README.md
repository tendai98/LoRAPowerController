# LoRaWAN Basestation Power Monitoring 📡⚡

This project aims to monitor power usage on a basestation utilizing LoRaWAN technology. It employs LoRa communication, power monitoring, and relay control to monitor and manage the power system remotely.

## Project Structure 🗂️

```
- lora.h
- LoRAPowerController.ino
- power.h
- relay_control.h
```

## Code Overview 💻

### LoRAPowerController.ino

The main code file integrates functionalities from different headers:

- **🛠️ `setup()`:** Initializes LoRa communication, ACS power monitoring, and relay controls. Functions used: `initLoRA()`, `initACS()`, `initControlRelays()`.

- **🔄 `loop()`:** Listens for LoRa data, gathers power readings, sends data, and controls relays based on received commands. Functions used: `sendRawData()`, `recvRawData()`, `currentReading()`, `systemControl()`, `controlRelay()`.

### lora.h (LoRa Communication) 🌐

Contains functions for LoRa communication:

- **📡 `initLoRA()`:** Initializes the LoRa device with a specified baud rate.

- **📩 `sendRawData()`:** Sends data through the LoRa device.

- **📥 `recvRawData()`:** Receives data from the LoRa device.

### power.h (Power Monitoring) ⚡

Handles power monitoring functionalities:

- **🔌 `initACS()`:** Initializes the ACS712 sensor for current sensing.

- **📊 `currentReading()`:** Reads and returns the current value based on the selected mode (AC or DC).

- **🔧 `systemControl()`:** Controls the system mode based on received commands.

### relay_control.h (Relay Control) 🎛️

Manages relay controls:

- **🔘 `initControlRelays()`:** Initializes relay pins and sets initial states.

- **🔀 `controlRelay()`:** Controls the relays based on received commands.
