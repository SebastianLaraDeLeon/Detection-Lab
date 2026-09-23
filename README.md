# Detection Lab

## Objective
[Brief Objective - Remove this afterwards]

The Detection Lab project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen understanding of network security, attack patterns, and defensive strategies.

### Skills Learned
[Bullet Points - Remove this afterwards]

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used
[Bullet Points - Remove this afterwards]

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Steps
## Lab Architecture

<p align="center">
  <img src="https://github-production-user-asset-6210df.s3.amazonaws.com/135392452/656865970-25f442ec-840e-4725-af04-3b1e63dfe2bc.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20260923%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20260923T005000Z&X-Amz-Expires=300&X-Amz-Signature=9e5af00395a6e01e89e29b9b6adae37960481d27c3dae01a27bb3599d36041ab&X-Amz-SignedHeaders=host&response-content-type=image%2Fpng" alt="Detection Lab network architecture" width="900">
</p>

<p align="center"><em>Figure 1. Detection Lab network topology and telemetry sources.</em></p>

This Detection Lab simulates a small enterprise network protected by pfSense, with a `192.168.1.0/24` LAN. The environment includes an Active Directory domain controller (`192.168.1.10`), a Windows 10 endpoint (`192.168.1.100`), a Splunk SIEM server (`192.168.1.20`), and a Zeek/Suricata sensor (`192.168.1.30`). A Kali Linux host (`192.168.1.250`) is used to generate controlled test activity.

The lab forwards endpoint and domain-controller telemetry to Splunk through the Universal Forwarder, while the Zeek/Suricata sensor provides network telemetry for analysis. pfSense connects the lab LAN to the NAT-connected WAN (`10.0.0.152`) and serves as the network gateway.

