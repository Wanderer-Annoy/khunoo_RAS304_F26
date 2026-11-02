# Bill of Materials — RAS 304 Data Collection Board

**Vendor:** DigiKey  
**Source:** `Data Collection Board.kicad_sch` and its supplied schematic PDF.  
**Design:** KNO PIC18F57Q43 Curiosity Nano data collection board.

| Ref. | Schematic value | Component / specification | Planning qty. | DigiKey part / candidate |
|---|---|---|---:|---|
| U2 | `KNO_PIC18F57Q43_Curiosity_Nano` | PIC18F57Q43 Curiosity Nano board | 2* | [Microchip DM164150](https://www.digikey.com/en/products/detail/microchip-technology/DM164150/) |
| U1 | `LM7805_KNO` | 5 V linear regulator; TO-220 candidate | 3 | [ST L7805CV](https://www.digikey.com/en/products/detail/stmicroelectronics/L7805CV/585964) |
| F1 | `Fuse` | Fuse; rating/package unspecified — **HOLD** | TBD | Do not order until specified |
| C1 | `0.1 uF` | 0.1 µF, 50 V, X7R, 0805 proposed | 3 | [KEMET C0805X104K5RACAUTO](https://www.digikey.com/en/products/detail/kemet/C0805X104K5RACAUTO/3314987) |
| R1 | `330 Ω` | 330 Ω, 1%, 1/8 W, 0805 proposed | 3 | [YAGEO RC0805FR-07330RL](https://www.digikey.com/en/products/detail/yageo/RC0805FR-07330RL/727866) |
| R2 | `10k Ω` | 10 kΩ, 1%, 1/8 W, 0805 proposed | 3 | [Stackpole RMCF0805FT10K0RES](https://www.digikey.com/en/products/filter/chip-resistor-surface-mount/0805/52) |
| D1 | `DEBUG LED` | Indicator LED; red 5 mm through-hole is a **candidate only** | 3* | [Inolux INL-5AR30](https://www.digikey.com/en/products/detail/inolux/INL-5AR30/7604627) |
| SW1 | `DEBUG Button` / `SW_Omron_B3FS` | Omron B3FS tactile switch; suffix/footprint must be checked | 3 | [Aratas (formerly Omron) B3FS-1000P](https://www.digikey.com/en/products/detail/aratas-america-llc/B3FS-1000P/277814) |

## Important verification notes

- **No schematic materials or values have been changed.** The DigiKey selections are candidate purchasable parts where the schematic does not specify a full manufacturer part number.
- **F1:** The schematic only says `Fuse`. It does not give current rating, voltage rating, time-delay/fast-blow characteristic, size, or holder. This line cannot be responsibly completed or ordered yet.
- **D1:** The schematic only says `DEBUG LED`. Color and package are unspecified. The red 5 mm part is only a candidate.
- **SW1:** The schematic identifies the Omron B3FS family. Verify the exact B3FS suffix and PCB footprint before purchase.
- **U1:** The schematic uses a custom `LM7805_KNO` symbol and has no footprint. The L7805CV is a 5 V 7805-family TO-220 candidate; verify pin order and footprint.
- **C1, R1, R2:** Footprints are blank. 0805 packages are proposed as a minimum-size planning choice; verify against your PCB.
- **U2:** Confirm whether the Curiosity Nano board is already supplied by the course/team before ordering.

\* Quantities are planning estimates. For discrete components, 3 = one prototype/breadboard part, one final PCB part, and one spare. For U2, 2 = one board plus one spare. Confirm quantities and availability at checkout.

**Not included as BOM components:** Trigger, Laser/Scanning, and Interpretation are net labels/interfaces in the supplied schematic, not separate connector symbols with defined part numbers or footprints. Add physical connectors only after selecting their actual footprints and mating cable requirements.
