# A Free Space Optical Communication PCB Units

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

## Shared Library:
### Pre-built Components Verfication:

Verificate Symbol and Footprint compatibility: 

1. RP2354A  ✓
2. AP2112K-3.3  ✓
3. SN74AHCT1G125DBVR  ✓
4. TPS22919DCKR  ✓
5. USBLC6-2SC6  ✓

### Costumed Components (in library):

1. ASTX-H11 
