+++
date = '2025-08-06T19:22:45+05:30'
draft = false
title = 'Know Your Industrial Control Systems'
+++
## Common Terminologies
- SCADA: Supervisory control and data acquisition system. It grew out of telemetry systems developed for space program. Initially, all the components were hard wired, then came the role of microprocessor based digital telemetry systems.
- DCS: Distributed control systems. These are typically installed within the plant premises.
- SCADA systems also support remote functionalities.
- 2 basic components of SCADA: 
  - RTU: Remote Terminal Unit or smart devices. These devices provide local control.
 - Central station computer
- MODBUS: Serial communications
- IEC 61850: Electric Utility Substation Communications
- HMI: Human-machine interface : Window
- Distributed control system (DCS): Process control (continuous/batch)
- Programmable logic controller (PLC): Discrete/ sequence control
- SCADA: Remote monitoring and dispatch
- SIS: Safety instrumental system : Life safety/ personnel protection
- OT: Operational technology = ICS (Industrial Control Systems) + CPS(Cyber Physical Systems) + others
- Purdue model: Structural / segmentation model for ICS security
- DCS topology:
  - Smart transmitters and valves: HART / Bus protocol
  - Ladder logic
- SCADA implementation in geographically dispersed areas
- Common SCADA mode communications: Microwave, satellite, cellular, dial-up mod

## ICS Protocols
- Traditional ICS protocols acquire measurement values via polling. Periodically request the state. Period determined by throughput/ latency requirements.
- MODBUS
  - Added features beyond basic capabilities in MODBUS
  - Define more data types to enhance inter-operability
  - Bandwidth minimization for SCADA systems: send only deltas.
- Publisher-subscriber based protocols: IEC 61805 GOOSE or UDP multicast in IP 
- Industry  specific models: 
  - ODVA’s CIP: Motion control, synchronization etc
  - IEC 61850: Electric Power Industry
- DCS protocols: OPC, Siemens S7, MODBUS, HART, Profibus, IP 
- SCADA protocols: DNP3, ICCP, IEC 60870-5-104
- Issues with major ICS Protocols:
  - Insecure by design
  - Insecure by implementation
- Can be secured by using techniques such as TLS etc.
- Modern Wrappers: SSP21

