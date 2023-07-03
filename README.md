# CANmaster-HW

This is the hardware for the CANMaster USB to CAN adaptor.

See [CANmaster-FW](https://github.com/TL-Embedded/CANmaster-FW) for programming instructions and behavior description.

Hardware is done via KiCad. The processor is a STM32F072.

# USB
The STM32's native USB is used.

# CAN
The can interface is provided by either a `MCP2551-I/SN` or a `MAX33011EASA+`.
The MAX330 has better input protection, and reports error codes. The presense of the MAX330 shall be indicated by fitting 0R on R8.

The bus terminator is enabled in software via optoisolator.

The CAN bus is exposed via phoenix connector:

| Pin | Function |
| --- | -------- |
| 1   | CANL     |
| 2   | CANH     |
| 3   | GND      |

# Programming
Programming is done via a 6 pin TC2030 SWD interface.

