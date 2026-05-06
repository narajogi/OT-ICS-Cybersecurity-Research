# OT Protocol Security Gap Analysis
## BACnet, Modbus/TCP, and OPC-UA Vulnerability Assessment

Date: May 2026
Researcher: Narasimha Jogi

---

## BACnet (Building Automation and Control Networks)

### Protocol Overview
- Developed: 1987 (ASHRAE Standard 135)
- Primary use: HVAC, lighting, access control, 
  fire safety in commercial buildings
- Estimated deployment: 100,000+ facilities 
  in the United States

### Security Limitations
1. No native authentication mechanism
2. No encryption of communications
3. Device discovery broadcasts expose 
   network topology
4. Who-Is/I-Am service enables reconnaissance
5. WriteProperty service allows unauthorized 
   control without authentication

### Detection Gap
Current tools monitor BACnet traffic volume 
but cannot establish behavioral baselines 
for normal device communication patterns.
Anomalous command sequences (e.g., abnormal 
WriteProperty frequency) go undetected.

---

## Modbus/TCP

### Protocol Overview
- Developed: 1979 (Modicon)
- Primary use: Industrial automation, 
  manufacturing, energy systems
- Estimated deployment: Most widely used 
  industrial protocol globally

### Security Limitations
1. No authentication — any device can 
   send commands
2. No encryption
3. No authorization — all clients have 
   equal access
4. Function code abuse enables reconnaissance 
   and manipulation
5. No session management

### Detection Gap
Modbus function code sequences follow 
predictable patterns in normal operation.
Deviations indicating reconnaissance 
(FC 01/02/03/04 sweeps) or manipulation 
(FC 05/06/15/16 anomalies) are not 
detected by current commercial tools 
at the protocol-behavior level.

---

## OPC-UA (OPC Unified Architecture)

### Protocol Overview
- Developed: 2006 (OPC Foundation)
- Primary use: Industrial data exchange, 
  modern SCADA systems
- Growing deployment in smart manufacturing 
  and Industry 4.0

### Security Limitations
1. Complex security model often misconfigured
2. Certificate management frequently neglected
3. Anonymous endpoints commonly left enabled
4. Session hijacking vulnerabilities
5. Node browsing enables system reconnaissance

### Detection Gap
OPC-UA has security features but they are 
rarely properly implemented. Behavioral 
monitoring of OPC-UA session patterns, 
subscription anomalies, and method call 
sequences is largely absent from current 
commercial tools.

---

## Research Implications

The common thread across all three protocols 
is the absence of behavioral baseline monitoring.
Current tools rely on:
- Known vulnerability signatures
- Network traffic volume thresholds
- IT-derived threat intelligence

None of these approaches capture protocol-level 
behavioral anomalies — the earliest and most 
reliable indicator of OT-specific attacks.

This gap defines the core research direction:
ML-driven behavioral baselining specific to 
OT protocol communication patterns.

---

*Last updated: May 2026*
*This analysis is part of independent research 
into protocol-aware OT cybersecurity.*
