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