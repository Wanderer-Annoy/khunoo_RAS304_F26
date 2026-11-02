---
title: Bill of Materials
---
## Overview

This Bill of Materials (BOM) identifies the components required to construct the **Data Collection Board** for the ASU RAS 304 Embedded Systems project.

The board is designed around the **KNO PIC18F57Q43 Curiosity Nano** microcontroller. Its power system accepts a +9V input and regulates it to +5V using an LM7805 linear voltage regulator. Additional components support circuit protection, debugging, and external communication interfaces.

All component selections are based on the supplied KiCad schematic. DigiKey is the selected vendor for component sourcing.

The BOM includes planning quantities for breadboard prototyping, final PCB assembly, and spare components.

## Bill of Materials

**Table 1.** Component list for the RAS 304 Data Collection Board.

| Part Name / Description | Qty. | Unit Cost | Total Cost | Manufacturer | Manufacturer Part Number | Vendor Link | Datasheet Link | Schematic Reference |
|:---|:---:|---:|---:|:---|:---|:---:|:---:|:---:|
| PIC18F57Q43 Curiosity Nano Development Board | 2 | TBD | TBD | Microchip | DM164150 | [DigiKey](https://www.digikey.com/en/products/detail/microchip-technology/DM164150/11586705)) | [Datasheet](https://www.microchip.com/en-us/development-tool/DM164150) | U2 |
| 5V Linear Voltage Regulator, TO-220 | 3 | $1.08 | $3.24 | STMicroelectronics | L7805CV | [DigiKey](https://www.digikey.com/en/products/detail/stmicroelectronics/L7805CV/585964) | [Datasheet](https://www.st.com/resource/en/datasheet/l78.pdf) | U1 |
| 500 mA Fast-Acting Surface Mount Fuse, 63V, 1206 | 3 | $1.47 | $4.41 | Littelfuse | 0437.500WR | [DigiKey](https://www.digikey.com/en/products/detail/littelfuse-inc/0437-500WR/1905895) | [Datasheet](https://www.littelfuse.com/assetdocs/fuse-437-datasheet?assetguid=7efbf979-42bb-4da1-b7b4-e1ec5d2b3789) | F1 |
| 0.1 µF Ceramic Capacitor, 50V, X7R, 0805 | 3 | $0.51 | $1.53 | KEMET | C0805X104K5RACAUTO | [DigiKey](https://www.digikey.com/en/products/detail/kemet/C0805X104K5RACAUTO/3314987) | [Datasheet](https://www.kemet.com/) | C1 |
| 330 Ω Resistor, 1%, 1/8W, 0805 | 3 | $0.10 | $0.30 | YAGEO | RC0805FR-07330RL | [DigiKey](https://www.digikey.com/en/products/detail/yageo/RC0805FR-07330RL/727866) | [Datasheet](https://www.yageo.com/) | R1 |
| 10 kΩ Resistor, 1%, 1/8W, 0805 | 3 | $0.10 | $0.30 | Stackpole | RMCF0805FT10K0RES | [DigiKey](https://www.digikey.com/en/products/filter/chip-resistor-surface-mount/0805/52) | [Datasheet](https://www.seielect.com/) | R2 |
| Red Indicator LED (Candidate) | 3 | $0.20 | $0.60 | Inolux | INL-5AR30 | [DigiKey](https://www.digikey.com/en/products/detail/inolux/INL-5AR30/7604627) | [Datasheet](https://www.inolux-corp.com/) | D1 |
| Omron B3FS Tactile Push Button | 3 | $0.75 | $2.25 | Aratas (formerly Omron) | B3FS-1000P | [DigiKey](https://www.digikey.com/en/products/detail/aratas-america-llc/B3FS-1000P/277814) | [Datasheet](https://omronfs.omron.com/) | SW1 |

## Cost Summary

**Table 2.** Estimated component purchasing cost.

| Description | Estimated Cost |
|:---|---:|
| Voltage Regulator (U1) | $3.24 |
| Ceramic Capacitor (C1) | $1.53 |
| 330 Ω Resistors (R1) | $0.30 |
| 10 kΩ Resistors (R2) | $0.30 |
| Debug LED (D1) | $0.60 |
| Push Button (SW1) | $2.25 |
| **Subtotal** | **$8.22** |

*Note: The subtotal excludes the microcontroller development board, fuse, shipping, and applicable taxes. Prices are estimates and may change depending on DigiKey availability and order quantity.*

## Component Selection and Verification

The following considerations apply before finalizing the hardware order:

- **U2 – Microcontroller:** The Microchip PIC18F57Q43 Curiosity Nano is the primary controller. Confirm whether this development board is already supplied by ASU before purchasing.
- **U1 – Voltage Regulator:** The STMicroelectronics L7805CV is a candidate for the LM7805 circuit. Verify its package, pin configuration, and PCB footprint.
- **F1 – Fuse:** The schematic identifies a fuse but does not specify its current rating, voltage rating, or physical package. Final selection requires verification.
- **C1 – Capacitor:** A 0.1 µF ceramic capacitor is retained as specified in the schematic. The 0805 package is a proposed footprint.
- **R1 and R2 – Resistors:** The original resistance values of 330 Ω and 10 kΩ are retained. The 0805 package is proposed for PCB assembly.
- **D1 – Debug LED:** The selected red LED is a candidate. Verify its color, dimensions, polarity, and PCB footprint.
- **SW1 – Debug Button:** The B3FS-1000P is a candidate for the specified Omron B3FS switch. Verify the exact footprint before ordering.

## External Interfaces

The schematic also provides three external communication interfaces:

| Interface | Connections | Purpose |
|:---|:---|:---|
| Trigger | RX, TX, GND | Trigger communication |
| Laser / Scanning | RX, TX, GND | Laser and scanning communication |
| Interpretation | RX, TX, GND | External interpretation interface |

These interfaces are represented by signal connections in the current schematic. Physical connectors, mating cables, and mounting hardware must be selected once their footprints and connection requirements are finalized.

## Purchasing and Assembly Notes

The quantities in this BOM are preliminary planning quantities.

For standard discrete components, the proposed quantity of three accounts for:

1. One component for breadboard prototyping.
2. One component for the final PCB.
3. One additional component as a spare.

The development board quantity includes one primary unit and one spare.

All components should be checked against the final KiCad footprints and electrical requirements before submitting the purchase request.

**Vendor:** DigiKey

**Project:** ASU RAS 304 – Data Collection Board

**Primary Controller:** KNO PIC18F57Q43 Curiosity Nano

**Power Input:** +9V

**Regulated Output:** +5V
