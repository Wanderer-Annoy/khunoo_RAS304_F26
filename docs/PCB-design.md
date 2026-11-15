---
title: PCB Design
---

# PCB Design

## Overview

This page documents the PCB design, verification, and manufacturing files for the **Data Collection Board** developed for RAS 304 Embedded Systems.

The PCB was designed using **KiCad** and implements the finalized Data Collection subsystem schematic. The completed layout was verified using the KiCad Design Rules Checker (DRC) before generation of the manufacturing files.

---

## PCB Layout

**Figure 1. Final Data Collection Board PCB layout.**

<!-- Replace the filename below with your PCB layout image. -->

![Final PCB Layout](PCB_Layout.png)

---

## PCB 3D View

**Figure 2. 3D view of the completed Data Collection Board.**

<!-- Replace the filename below with your KiCad 3D Viewer image. -->

![PCB 3D View](PCB_3D.png)

---

## Design Verification

### KiCad Design Rules Check

The final PCB layout was verified using the **KiCad Design Rules Checker (DRC)**.

**Final DRC Result: 0 errors**

**Figure 3. KiCad DRC results for the final PCB.**

<!-- Replace the filename below with your DRC screenshot. -->

![KiCad DRC Results](PCB_DRC.png)

The DRC was used to verify the PCB for issues including:

- Short circuits
- Copper clearance violations
- Track-to-pad clearance
- Unconnected pads
- Track connectivity
- Board-edge clearance
- Solder-mask conflicts

The final PCB passed the required electrical design-rule checks before the manufacturing files were generated.

---

## Design for Manufacturing Check

The generated PCB manufacturing files were checked using **JLCDFM** before fabrication.

**Figure 4. JLCDFM PCB preview and DFM analysis.**

<!-- Replace the filename below with your JLCDFM screenshot. -->

![JLCDFM Verification](PCB_DFM.png)

The JLCDFM check provides additional verification that the generated PCB manufacturing files can be successfully interpreted and fabricated.

---

## ECAD Project Files

The complete KiCad project is available below.

<!-- Replace this filename with your actual KiCad ZIP filename. -->

[**Download KiCad ECAD Project**](Data_Collection_Board_KiCad.zip)

The ECAD archive contains the editable KiCad project files for the Data Collection Board.

---

## Gerber Manufacturing Files

The final Gerber manufacturing package is available below.

<!-- Replace this filename with your actual Gerber ZIP filename. -->

[**Download Gerber Files**](Data_Collection_Board_Gerbers.zip)

The Gerber package contains the PCB fabrication layers and drill information required for manufacturing.

---

## Final Design Files

| File | Description |
|:---|:---|
| [KiCad ECAD Project](Data_Collection_Board_KiCad.zip) | Complete editable KiCad project |
| [Gerber Manufacturing Files](Data_Collection_Board_Gerbers.zip) | PCB fabrication and drill files |
| [PCB Layout](PCB_Layout.png) | Final PCB layout image |
| [PCB 3D View](PCB_3D.png) | KiCad 3D representation |
| [DRC Verification](PCB_DRC.png) | KiCad DRC showing zero errors |
| [JLCDFM Verification](PCB_DFM.png) | Manufacturing DFM verification |

---

## Final Verification

Before release of the manufacturing files, the PCB design was reviewed for:

- Complete electrical connectivity
- Correct component footprints
- Power and ground routing
- Signal routing and clearances
- Connector orientation and accessibility
- Component placement
- Board-edge clearance
- Silkscreen placement
- KiCad DRC compliance
- Gerber generation
- Manufacturing DFM verification

The final Data Collection Board was prepared for fabrication after completing these verification steps.
