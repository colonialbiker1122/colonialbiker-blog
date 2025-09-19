+++
date = '2025-09-19T20:07:59+05:30'
draft = false
title = 'MODBUS'
+++
- One master many slaves
- Master broadcast to all devices. Only assigned recipient will read, other slaves will reject the message
- MODBUS commands can instruct an RTU to change a value in its registers, control or read an I/O port and commanding device to send back one or more values contained in its registers
- MODBUS defines a protocol data unit (PDU) which is independent of the underlying communication layers
- MODBUS RTU: Addressing before PDU. CRC appended at the end.
- MODBUS ASCII: Representation of PDU in all printable characters
- MODBUS TCP: Addressing before PDU. CRC left upto TCP layer to deal with
- MODBUS Serial: RS232, RS485, serial line between master and slave
- MODBUS plus: RS485, HDLC (high level data link control)
- MODBUS TCP : Ethernet physical layer. Ethernet data link layer, etc
- Information in slave device is stored in 4 different tables
- Each table has 9999 data points storing different values
- Each coil is 1 bit and given data address between x0000 & x9999
- Each register = 2 bytes = 1 word and also has data address between x0000 and x9999
- Each device in a network is assigned a byte value from 0 to 255
- When master requests for data, first byte it sends is Slave ID
- MODBUS map (list) should have following information:
  - What kind of data the device reads and stores (temperature, pressure etc)
  - At what address the data is stored (voltage at 40001)
  - Format in which the data is stored (bits, UINT16, SINT16)
  - Device is ADU addressing or PDU addressing

- Modbus Error Checking
  - Parity checking: Even parity, Odd parity, No parity
  - Frame checking: Cyclical redundancy check in RTU mode. Longitudinal redundancy in ASCIT mode

- First byte sent : slave ID : : Second byte sent : function code

- Function codes:
  - x01 : Read : Discrete output coils
  - x02 : Read : Discrete input contacts
  - x03 : Read : Analog output holding registers
  - x04 : Read : Analog input registers
  - x05 : Write (single) : Discrete output coil
  - x06 : Write (single) : Analog output holding registers
  - x10 : Write (multiple) : Analog output holding registers
  - x0F : Write (multiple) : Discrete output coils

- Coils are single bit. 0s : OFF :: 1s : ON
- Coils represent the state of discrete input/output (is the light on or off)
- Input Registers: Report state of an external value. eg: Voltage or Temperature will get assigned a value between 0 to 65535
- Holding Registers: Temporarily store program data for Modbus devices
- Third byte sent: Starting address which is the index into the data area in the modbus device
- Bit length specifies how many point to read or write
- Word count specifies how many registers to read or write
- Byte count: No of bytes included in request/response
- Response code: Indicates completion of request
