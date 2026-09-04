# A Free Space Optical Communication PCB Units

This project implements a free-space optical communication link using two separate KiCad-designed boards: a transmitte and a receiver. The transmitter uses an RP2354A microcontroller to frame arbitrary digital payloads into packets and generate 100 kbit/s RZ-OOK modulation for a 650 nm laser module through a level-shifting buffer and independent hardware safety chain. The receiver uses a BPW34 photodiode, OPA320 transimpedance amplifier, and TLV3201 comparator to recover the optical pulses and feed them back into an RP2354A for decoding, CRC verification, and delivery to the host system. Both boards include USB, UART, SWD, a 12 MHz crystal, and a 10 MHz TCXO reference, with the initial target being a stable optical link over approximately 5 meters.
## Architecture

Two separate 4-layer boards:
- TX: RP2354A + USB-C + host I/O + 12 MHz crystal + 10 MHz TCXO + laser module.
- RX: RP2354A + USB-C + host I/O + 12 MHz crystal + 10 MHz TCXO + BPW34/OPA320/TLV3201 optical receiver + ADC monitor.

### TX
- TX_ROOT
- TX_POWER_USB
- TX_MCU_CLOCK
- TX_HOST_IO
- TX_LASER

### RX
- RX_ROOT
- RX_POWER_USB
- RX_MCU_CLOCK
- RX_HOST_IO
- RX_OPTICAL_AFE
- RX_MONITOR

## Project tree:

FSOC_KiCad/
1.  FSOC_TX
    ├── FSOC_TX.kicad_pro
    ├── FSOC_TX.kicad_sch
    ├── FSOC_TX.kicad_pcb
    ├── sym-lib-table
    └── fp-lib-table
2.  FSOC_RX
    ├── FSOC_RX.kicad_pro
    ├── FSOC_RX.kicad_sch
    ├── FSOC_RX.kicad_pcb
    ├── sym-lib-table
    └── fp-lib-table

3.  Shared_Library
    ├── FSOC_Symbols.kicad_sym
    └── FSOC_Footprints.pretty/

4. Soruces (official documentations for costumed components)
    ├── ASTX_H11
    

### Pre-built Components Verfication:

Verificate Symbol and Footprint compatibility: 

1. RP2354A  ✓
2. AP2112K-3.3  ✓
3. SN74AHCT1G125DBVR  ✓
4. TPS22919DCKR  ✓
5. USBLC6-2SC6  ✓

### Costumed Components (in library):

1. ASTX-H11 
