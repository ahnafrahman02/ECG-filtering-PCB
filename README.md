# Wearable Smart Glasses ECG — 4-Layer Mixed-Signal PCB

A compact, manufacturing-ready 4-layer PCB designed in **KiCad** for a wearable smart glasses ECG monitoring system. The board integrates an **ESP32-S3-MINI-1** wireless MCU with a **Texas Instruments ADS1292** analog front-end inside a strict wearable form factor.

![3D Render of the PCB](media/3d_render_front.png)

## Key Specifications
| Parameter | Value |
| :--- | :--- |
| **Dimensions** | 51.0 mm × 19.3 mm × 1.6 mm |
| **Layer Stackup** | 4-Layer FR4 (Dedicated internal Power & Ground planes) |
| **MCU / Wireless** | ESP32-S3-MINI-1 (2.4 GHz Wi-Fi / BLE) |
| **ECG Front-End** | TI ADS1292 (24-bit ADC) |
| **Power Architecture** | Modular external 3.3V regulated rail via 3-pin THT header |
| **Verification Status** | 0 Errors (ERC & DRC Passed) — Ready for Fabrication |

## Engineering Highlights
* **Mixed-Signal Isolation:** Separated noisy digital SPI/RF domains from microvolt-level analog ECG traces using a 4-layer stackup and a ferrite bead choke on the 3.3V analog rail.
* **RF Antenna Optimization:** Positioned the ESP32-S3 module with a full PCB edge overhang so the 2.4 GHz antenna radiates in free air without ground-plane detuning.
* **Low-Impedance Grounding:** Applied a solid copper ground pour directly to the ADS1292 exposed thermal pad (Pin 33) to maximize analog noise immunity.
* **DFM Compliance:** Enforced 0.25 mm copper-to-edge clearance, 45° trace routing, and mechanically anchored through-hole headers for wearable durability.

## Repository Contents
* `/hardware` — Native KiCad 8/9 schematic and PCB layout files.
* `/manufacturing` — Fabrication-ready Gerber (`.gbr`), Excellon Drill (`.drl`), and `.gbrjob` archive.
* `/docs` — High-resolution schematic PDF, 2D copper layer renders, and 0-error ERC/DRC reports.

https://github.com/user-attachments/assets/d7e15759-4539-47e6-963b-ab400f9db16c





