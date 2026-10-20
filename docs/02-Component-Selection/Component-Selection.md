---
title: Component Selection
---

## Data Collection Board

**Team:** 105 — Phoenix Phorce  
**Project:** Handheld LiDAR Accessibility Aid[cite: 2]  
**Member:** Khun Oo[cite: 2]  
**Subsystem:** Data Collection Board[cite: 1]  

## Overview

The Data Collection Board is responsible for coordinating LiDAR scan data, scan position information, and trigger information before sending the collected data to the Interpretation Board[cite: 1].

The current design uses a **PIC18F57Q43 Curiosity Nano** as the main microcontroller[cite: 1, 2]. The board communicates with the Trigger Board, Laser / Scanning Board, and Interpretation Board through UART connections[cite: 3].

The Data Collection Board receives power from the team Power Board through the **P1 power connection**[cite: 1, 3]. Power and communication are kept separate in the team architecture[cite: 1].

---

## Power Budget Analysis

The power budget for the Data Collection Board is summarized in the sections below, detailing major component current consumption, power rails, external source connections from the team Power Board, and calculated battery life[cite: 1].

### Part 1: Main Components and +12V Rail
![Data Collection Power Budget Part 1](https://raw.githubusercontent.com/Wanderer-Annoy/khunoo_RAS304_F26/main/02-Component-Selection/DCPB.png)

### Part 2: +5V, +3.3V Rails, and External Power Source 1
![Data Collection Power Budget Part 2](https://raw.githubusercontent.com/Wanderer-Annoy/khunoo_RAS304_F26/main/02-Component-Selection/DCPB2.png)

### Part 3: External Power Source 2, Battery Life, and Notes
![Data Collection Power Budget Part 3](https://raw.githubusercontent.com/Wanderer-Annoy/khunoo_RAS304_F26/main/02-Component-Selection/DCPB3.png)

---

## Major Component Selection

### Microcontroller

**PIC18F57Q43 Curiosity Nano**[cite: 1, 2]

| Specification | Selection |
| --- | --- |
| Component | PIC18F57Q43 Curiosity Nano[cite: 1, 2] |
| Part Number | DM164150 |
| Quantity | 1 |
| Logic Level | 3.3 V[cite: 2] |
| Communication | UART[cite: 3] |
| Power Source | Team Power Board[cite: 1, 3] |
| Power Connection | P1 — VLOGIC / GND[cite: 1, 3] |

**Purpose:**  
The PIC18F57Q43 Curiosity Nano coordinates incoming trigger and scanning information, buffers collected scan samples, and communicates with the other embedded-system boards[cite: 1, 2].

### Communication Connections

| Connector | Connected Board | Interface | Purpose |
| --- | --- | --- | --- |
| J1 | Trigger Board[cite: 3] | UART TX/RX[cite: 3] | Receives scan requests and trigger information[cite: 3] |
| J2 | Laser / Scanning Board[cite: 3] | UART TX/RX[cite: 3] | Exchanges LiDAR and scanning information[cite: 3] |
| J3 | Interpretation Board[cite: 3] | UART TX/RX[cite: 3] | Sends collected information for interpretation[cite: 3] |

The Laser / Scanning Board documentation specifies **3.3 V UART signals** for the J2 connection to the Data Collection Board[cite: 2]. Therefore, 3.3 V logic is currently used as a design assumption for the Data Collection Board.

> **Note:** The microcontroller was selected for the project and therefore does not require a three-option component-selection comparison[cite: 6, 12]. It is still included in the power budget because it consumes power[cite: 7].

---

## Power Architecture

The Data Collection Board does not contain its own battery or primary system power source[cite: 1]. Power is supplied by the team's Power Board[cite: 1, 3].

The Power Board contains the battery pack, protection and switching circuitry, voltage regulation, and power distribution circuitry.

The Data Collection Board receives power through[cite: 1, 3]:

- **P1 — VLOGIC**[cite: 1, 3]
- **P1 — GND**[cite: 1, 3]

The UART ribbon cables **J1, J2, and J3** are used for communication and are separate from the primary power connection[cite: 1, 3].

### VLOGIC Power Rail

| Component | Part Number | Supply | Quantity | Maximum Current |
| --- | --- | --- | ---: | ---: |
| PIC18F57Q43 Curiosity Nano[cite: 1, 2] | DM164150 | 3.3 V logic[cite: 2] | 1 | TBD[cite: 2] |

A **25% safety margin** is applied to the total required current[cite: 7].

**Power budget calculation:**

`Required VLOGIC Current = Subtotal Current × 1.25`[cite: 7]

The final absolute-maximum current is currently marked **TBD** because it must be supported by the appropriate component datasheet rather than estimated from a connector or regulator current rating[cite: 2, 7].

---

## Power Source

| Specification | Current Selection |
| --- | --- |
| Source | Team Power Board[cite: 1, 3] |
| Connection | P1[cite: 1, 3] |
| Rails | VLOGIC / GND[cite: 1, 3] |
| Local Battery | None[cite: 1] |
| Local Primary Regulator | None currently specified[cite: 1] |
| Available P1 Current | TBD[cite: 2] |
| Final VLOGIC Voltage | TBD by team power design[cite: 2] |

The team Power Board distributes dedicated power connections to each subsystem[cite: 1]. **P1** is assigned to the Data Collection Board[cite: 1].

The final available current and finalized VLOGIC specification will be updated after the Power Board design is completed[cite: 2].

---

## Power Budget

The Data Collection Board power budget is provided below.

[**Download Data Collection Power Budget.xlsx**](https://github.com/Wanderer-Annoy/khunoo_RAS304_F26/raw/refs/heads/main/02-Component-Selection/Data%20Collection%20Power%20Budget.xlsx)

The power budget includes[cite: 7]:
- Major powered components[cite: 7]
- Component quantities[cite: 7]
- Supply voltage[cite: 7]
- Maximum current[cite: 7]
- VLOGIC power rail[cite: 1, 7]
- 25% current safety margin[cite: 7]
- Power Board P1 connection[cite: 1, 7]
- External power source information[cite: 7]
- Remaining-current calculations[cite: 7]

Values marked **TBD** will be updated as the schematic, component selections, and Power Board specifications are finalized[cite: 2].

---

## Design Notes

The current design keeps the Data Collection Board focused on data coordination[cite: 1]. Its primary purpose is to receive, organize, buffer, and transmit information between the other embedded-system boards[cite: 1].

The LiDAR, scan motor, audio system, vibration motor, battery, and main voltage regulators belong to other team subsystems and therefore are not included as loads in the Data Collection Board power budget.

The current architecture will be updated as the PCB schematic, component selections, and final team power specifications are developed[cite: 2].
