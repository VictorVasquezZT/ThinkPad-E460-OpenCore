# ThinkPad-E460-OpenCore

This repository contains the OpenCore configuration for the **Lenovo ThinkPad E460**.  
The purpose is to document macOS compatibility on this laptop and provide a starting point for installation.

---

## 📌 Laptop Specifications

- **Model:** Lenovo ThinkPad E460  
- **CPU:** Intel Core i7-6500U (2C/4T, 2.5 GHz, Skylake)  
- **iGPU:** Intel HD Graphics 520  
- **dGPU:** AMD Radeon R7 M360 (2 GB DDR3)  
- **RAM:** 8 GB DDR3  
- **Storage:** Kingston SSD 512 GB  
- **Wi-Fi:** Intel (fully working with [AirportItlwm](https://github.com/OpenIntelWireless/itlwm))  
- **Fingerprint Sensor:** Present (not configured, not necessary at the moment)  

---

## ⚙️ macOS Compatibility Status (with OpenCore)

| Component           | Status          | Notes |
|---------------------|-----------------|-------|
| CPU (i7-6500U)      | ✅ Working       | Native Skylake support |
| Intel HD 520 iGPU   | ✅ Working       | Full graphics acceleration |
| AMD R7 M360 dGPU    | ⚠️ Not supported | macOS does not support this GPU |
| Wi-Fi (Intel)       | ✅ Working 100%  | Fully functional with AirportItlwm |
| Audio               | ✅ Working       | With AppleALC |
| Keyboard / Trackpad | ✅ Working       | With VoodooPS2 |
| Battery             | ✅ Working       | With SMCBatteryManager |
| Webcam              | ✅ Working       | Native |
| Bluetooth           | ✅ Working       | With IntelBluetoothFirmware |
| Fingerprint Sensor  | ⚠️ Not tested    | Hardware present but not configured |

---

## 🚀 Recommendations

- **Disable the R7 M360 dGPU** in BIOS to avoid issues (macOS will only use the Intel HD 520).  
- Keep OpenCore and kexts up to date.  
- AirportItlwm provides stable Wi-Fi support, but for native macOS features like **AirDrop/Handoff**, a **Broadcom card** is still recommended.  

---
