# enterprise-cloud-iam-homelab

Enterprise Cloud & IAM Security Home Lab

🔎 Overview

This repository documents my enterprise-style hybrid cloud and identity security lab built to simulate real-world:

	•	Identity & Access Management (IAM)
	•	Zero Trust remote access
	•	Infrastructure hardening
	•	Containerized service deployment
	•	SIEM monitoring
	•	Secure network architecture
	•	Hybrid virtualization (Proxmox + Linux)

This lab is designed to mirror modern enterprise environments supporting cloud, IAM, and security engineering roles.

⸻

🧠 Objectives

	•	Design a Zero Trust home infrastructure
	•	Implement secure remote access without port forwarding
	•	Deploy containerized services securely
	•	Simulate IAM and security monitoring workflows
	•	Practice infrastructure documentation at enterprise standards

⸻

🏗 Architecture Overview

High-Level Flow

Internet
↓

ISP Router (Bridge Mode Planned)
↓

Future Firewall (pfSense or UniFi)
↓

Managed Switch
↓

Proxmox Hypervisor
↓

Ubuntu Server (HomeCore)
↓

Dockerized Security Services

⸻

🖥 Infrastructure Components

Hypervisor

	•	Proxmox VE

	•	32GB RAM

	•	Multiple VMs for isolation testing

Core Server (HomeCore)

	•	Ubuntu Server
	•	Docker
	•	16GB RAM
	•	512GB NVMe

⸻

🔐 Security Design

	•	Zero Trust access using Tailscale
	•	No exposed inbound ports
	•	DNS filtering via AdGuard
	•	Containerized service isolation
	•	Centralized logging with Wazuh (planned/active)
	•	Remote access restricted to authenticated devices only

⸻

🧱 Core Services

1️⃣ Tailscale (Zero Trust Remote Access)

	•	Installed on:
	•	HomeCore
	•	Proxmox
	•	T14
	•	iPhone
	•	Enables secure remote dashboard access
	•	Eliminates need for port forwarding

⸻

2️⃣ AdGuard (Network DNS Filtering)

	•	Docker deployment
	•	LAN-wide DNS resolution
	•	Custom blocklists
	•	Malware/phishing domain blocking

⸻

3️⃣ Wazuh (SIEM & Monitoring)

	•	Host-level monitoring
	•	Log collection
	•	Security event visibility
	•	Foundation for SOC simulation

⸻

4️⃣ Portainer

	•	Docker container management
	•	Image lifecycle visibility
	•	Simplified service orchestration

⸻

5️⃣ Dozzle

	•	Real-time Docker log monitoring
	•	Lightweight visibility tool

⸻

6️⃣ Homepage Dashboard

	•	Centralized service navigation
	•	Clean internal admin interface
	•	Accessible via Tailscale only

⸻

🧠 IAM Simulation Strategy

Future phases include:

	•	Active Directory VM
	•	Role-based access testing
	•	Conditional access scenarios
	•	Service account simulation
	•	Privileged access segmentation
	•	Identity lifecycle automation testing

This aligns with enterprise IAM workflows used in Azure, AWS, and hybrid environments.

⸻

🚀 Roadmap Phases

Phase 1 – Core Infrastructure

	•	Proxmox deployment
	•	Ubuntu Server
	•	Dockerized services
	•	Tailscale setup

Phase 2 – Network Hardening

	•	VLAN segmentation
	•	Firewall rules
	•	DNS enforcement
	•	Switch-level configuration

Phase 3 – Identity Layer

	•	Active Directory lab
	•	IAM testing
	•	Privilege escalation scenarios
	•	Logging & auditing

Phase 4 – Cloud Integration

	•	Azure/AWS hybrid identity simulation
	•	Conditional access testing
	•	MFA enforcement
	•	Logging integration

⸻

🧠 Lessons Learned

	•	Zero Trust removes need for port forwarding
	•	DNS misconfiguration can disrupt routing
	•	Service isolation improves troubleshooting
	•	Documentation prevents configuration drift
	•	Enterprise design principles apply even at home scale
