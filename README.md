# OT/ICS Cybersecurity Research
## Protocol-Aware Threat Detection for Operational Technology Networks

**Researcher:** Narasimha Jogi  
**Focus Area:** Industrial Control Systems Security  
**Protocols:** BACnet, Modbus/TCP, OPC-UA  
**Status:** Active Research — Phase 1

---

## The Problem

U.S. critical infrastructure relies on operational 
technology (OT) protocols designed in the 1990s 
without cybersecurity consideration. These protocols 
control:

- 6,100+ hospitals and healthcare facilities
- 15,000+ electricity generation facilities
- 1,400+ water treatment plants
- 50,000+ commercial data centers

**Current gap:** Existing security tools (Claroty, 
Nozomi, Dragos) provide IT-OT convergence monitoring 
but lack protocol-specific behavioral analysis for 
BACnet, Modbus/TCP, and OPC-UA environments.

**National exposure:**
- 1 cybersecurity breach every 39 seconds (CISA, 2024)
- $4.88M average cost per breach (IBM, 2024)
- 75% of building management systems have known 
  exploited vulnerabilities (Industry Analysis, 2025)

---

## Proposed Research

Development of a protocol-aware cybersecurity platform 
for OT/ICS environments featuring:

### Core Components

**1. Passive Network Traffic Mirroring**
- Non-disruptive monitoring of OT network traffic
- Read-only operation preserving system reliability
- Compatible with legacy devices and protocols

**2. Protocol-Specific Behavioral Baselines**
- Machine learning models for BACnet normal behavior
- Modbus/TCP communication pattern analysis
- OPC-UA anomaly detection framework
- No signature-based detection — purely behavioral

**3. Automated Response Workflows**
- Protocol-aware VLAN segmentation templates
- Incident response scripts safe for OT environments
- Containment without disrupting physical operations

**4. Deployment Architecture**
- Self-contained hardware appliance option
- SaaS-based cloud deployment option
- Compatible with existing OT infrastructure

---

## Why This Matters

Current commercial solutions fail to address 
protocol-specific behavior in OT environments:

| Capability | Claroty | Nozomi | Dragos | This Research |
|-----------|---------|--------|--------|---------------|
| Passive detection | ✓ | ✓ | ✓ | ✓ |
| BACnet behavioral baseline | ✗ | Partial | ✗ | ✓ |
| Modbus/TCP protocol rules | Partial | ✗ | ✗ | ✓ |
| OPC-UA anomaly detection | ✗ | ✗ | ✗ | ✓ |
| Building automation systems | ✗ | ✗ | ✗ | ✓ |
| ML-driven (no signatures) | ✗ | ✗ | ✗ | ✓ |

---

## Research Phases

### Phase 1: Research & Validation (Months 1-12)
- [ ] OT traffic data collection methodology
- [ ] BACnet behavioral baseline ML model
- [ ] Modbus/TCP protocol-specific detection rules
- [ ] OPC-UA anomaly detection framework
- [ ] VLAN segmentation automation scripts
- [ ] Simulation environment validation

### Phase 2: Product Development (Months 13-24)
- [ ] Hardware appliance architecture
- [ ] SaaS platform development
- [ ] Pilot deployment with partner facilities
- [ ] Performance validation and refinement
- [ ] Commercial launch preparation

---

## Research Background

This research is informed by 7.5 years of hands-on 
experience deploying and standardizing industrial 
control systems in critical infrastructure environments, 
including work on large-scale electrical power 
management systems across multiple data center builds.

The research is conducted independently and all 
findings will be publicly disseminated through:
- Academic publications (IEEE Transactions on 
  Industrial Informatics target)
- Conference presentations (S4, SANS ICS Summit)
- Open-source tooling published in this repository
- CISA Coordinated Vulnerability Disclosure 
  participation

---

## National Policy Alignment

This research directly supports:
- Executive Order 14306: Improving Critical 
  Infrastructure Cybersecurity
- CISA Strategic Plan 2023-2025: Critical 
  Infrastructure Cyber Defense
- NIST SP 800-82 Rev 3: Guide to ICS Security
- NSF Cybersecurity Innovation for Cyber 
  Infrastructure Campaign

---

## Repository Structure (In Progress)
