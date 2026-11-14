---
title: Bill of Materials
---

## Overview

This Bill of Materials (BOM) identifies the remaining components required to purchase for the **Data Collection Board** in the ASU RAS 304 Embedded Systems project, updated to match the KiCad footprint assignments.

The board is designed around the **KNO PIC18F57Q43 Curiosity Nano** microcontroller. Its power system accepts a +9V input and regulates it to +5V using an LM2596S-5 switching voltage regulator circuit. Previously acquired components (microcontroller, fuse, capacitors, resistors, LEDs, and push button) have been removed from the purchasing list.

All remaining component selections and package sizes match the assigned KiCad footprints. DigiKey is the selected vendor for component sourcing.

## Bill of Materials

**Table 1.** Remaining components to order for the RAS 304 Data Collection Board.

| Part Name / Description | KiCad Footprint | Qty. | Unit Cost | Total Cost | Manufacturer | Manufacturer Part Number | Vendor Link | Datasheet Link | Schematic Reference |
|:---|:---|:---:|---:|---:|:---|:---|:---:|:---:|:---:|
| 5V Switching Voltage Regulator, TO-263-5| `Package_TO_SOT_SMD:TO-263-5_TabPin3` | 3 | $3.88 | $11.64 | Texas Instruments | LM2596S-5.0/NOPB | [DigiKey](https://www.digikey.com/en/products/detail/texas-instruments/LM2596S-5.0-NOPB/334842) | [Datasheet](https://www.ti.com/product/LM2596) | U1 |
| 68 µH Shielded Power Inductor, 1.65A (12x12mm SMD) | `Inductor_SMD:L_Bourns_SRR1260` (Suggested) | 3 | $1.34 | $4.02 | Bourns | SRR1260-680M | [DigiKey](https://www.digikey.com/en/products/detail/bourns-inc/SRR1260-680M/1638201) | [Datasheet](https://www.bourns.com/docs/Product-Datasheets/SRR1260.pdf) | L1 |
| 5A, 40V Schottky Diode, DO-201AD Axial | `Diode_THT:D_DO-201AD_P15.24mm_Horizontal` | 3 | $0.58 | $1.74 | ON Semiconductor | 1N5825 | [DigiKey](https://www.digikey.com/en/products/detail/onsemi/1N5825/1475511) | [Datasheet](https://www.onsemi.com/pdf/datasheet/1n5823-d.pdf) | D5|
| 2x5 Pin IDC Box Header, 2.54mm Pitch, Vertical | `Connector_IDC:IDC-Header_2x05_P2.54mm_Vertical` | 9 | $0.65 | $5.85 | Amphenol CS | 68020-210HLF | [DigiKey](https://www.digikey.com/en/products/detail/amphenol-cs-fci/68020-210HLF/1878492) | [Datasheet](https://www.amphenol-cs.com/) | J1, J2, J3 |

## Cost Summary

**Table 2.** Estimated component purchasing cost.

| Description | Estimated Cost |
|:---|---:|
| Switching Voltage Regulator (U1) | $11.64 |
| 68 µH Power Inductor (L1) | $4.02 |
| Schottky Diode (D5) | $1.74 |
| 2x5 IDC Headers (J1, J2, J3) | $5.85 |
| **Subtotal** | **$23.25** |

## External Interfaces

| Interface | Schematic Pins | Assigned KiCad Footprint | Purpose |
|:---|:---|:---|:---|
| Trigger| 8-pin (TX, RX, GPIO1–5, GND) | `IDC-Header_2x05_P2.54mm_Vertical` (10-pin) | Trigger communication |
| Laser / Scanning | 8-pin (TX, RX, GPIO1–5, GND) | `IDC-Header_2x05_P2.54mm_Vertical` (10-pin)| Laser and scanning communication |
| Interpretation | 8-pin (TX, RX, GPIO1–5, GND) | `IDC-Header_2x05_P2.54mm_Vertical` (10-pin) | External interpretation interface |
