# Drone_SoC_2.0

<img width="1018" height="422" alt="image" src="https://github.com/user-attachments/assets/7ae0f510-6fc7-44ce-9bac-eae65200d323" />
<img width="793" height="814" alt="image" src="https://github.com/user-attachments/assets/acbdefca-9116-459d-8169-3aace5ed9811" />
<img width="551" height="491" alt="image" src="https://github.com/user-attachments/assets/1e4b128d-6dd3-4955-be96-76eeb00d9a57" />
<img width="540" height="510" alt="image" src="https://github.com/user-attachments/assets/0c9f6eeb-18a6-4980-b0ca-5415cda0852b" />

## High-Level Address Partitioning

0x0000_0000 – 0x0FFF_FFFF   Internal IMEM / Boot ROM

0x1000_0000 – 0x1FFF_FFFF   Internal DMEM / On-chip SRAM

0x3000_0000 – 0x3FFF_FFFF   SoC Peripheral Register Space

0x4000_0000 – 0x4FFF_FFFF   External SPI Flash Memory

0x6000_0000 – 0x6FFF_FFFF   External SDRAM

## Peripheral Address Map (v1 – Frozen)

0x3000_0000 – 0x3000_0FFF  Global Control & System Registers

0x3000_1000 – 0x3000_1FFF  SPI Master (IMU / Sensor Interface)

0x3000_2000 – 0x3000_2FFF  UART (GPS / Debug)

0x3000_3000 – 0x3000_3FFF  PWM Motor Controller

0x3000_4000 – 0x3000_4FFF  Hardware Timer

0x3000_5000 – 0x3000_5FFF  Watchdog & Failsafe Logic

| Interrupt | Source                               |
| --------- | ------------------------------------ |
| IRQ0      | Hardware Timer (Control Loop Timing) |
| IRQ1      | SPI / IMU Interface                  |
| IRQ2      | UART (GPS / Debug)                   |
| NMI       | Watchdog / Failsafe                  |
