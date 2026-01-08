# Cloud Hybrid Lab (On-Prem + Cloud Simulation)

## Overview

This project demonstrates a **realistic hybrid cloud architecture** by simulating an on-premises environment using **VirtualBox** and integrating it with cloud infrastructure.

The goal is to replicate common enterprise scenarios where organizations must operate across **on-prem and cloud environments simultaneously**, rather than assuming a clean, cloud-only starting point.

---

## Why VirtualBox?

In real-world environments, on-prem systems often include:

- Legacy Active Directory  
- Custom DNS configurations  
- Applications tightly coupled to local infrastructure  
- Limited ability to “lift and replace”  

VirtualBox is used in this project to:

- Simulate an on-prem data center environment  
- Control networking, DNS, and identity behavior  
- Introduce realistic constraints and failure modes  
- Enable repeatable, local testing without external dependencies  

This allows the hybrid design to reflect **actual migration and integration challenges**, not idealized demos.

---

## Problem Statement

Most organizations cannot fully migrate to the cloud in a single step due to:

- Legacy identity systems  
- Compliance requirements  
- Operational risk  
- Network dependencies  
- Cost constraints  

This project explores how to **securely and reliably integrate on-prem systems with cloud platforms**, while maintaining identity, connectivity, and operational visibility.

---

## Architecture Overview

**High-level view of the hybrid system**

**Key components:**
- On-prem Active Directory (VirtualBox)  
- On-prem DNS  
- Site-to-site VPN  
- Cloud virtual networks  
- Hybrid identity integration  
- Centralized monitoring  

---

## Key Design Decisions

- Why site-to-site VPN instead of a private circuit  
- Why centralized identity over cloud-only IAM  
- Why hub-and-spoke networking  
- Why DNS integration is critical in hybrid environments  

Expanded details can be found in:  
➡️ `docs/design-decisions.md`

---

## Repository Structure

```text
on-prem/        → VirtualBox-based on-prem simulation  
connectivity/   → VPN and routing  
cloud/          → Cloud-side resources (Azure & AWS)  
docs/           → Learning paths and design rationale  
diagrams/       → Architecture visuals  
