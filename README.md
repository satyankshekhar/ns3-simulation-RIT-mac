# ns3-simulation-RIT-mac

> ⚠️ **Project Status: Work In Progress**
>
> This project is part of an academic mini-project and is currently under development. The full source code will be uploaded once it has been evaluated as part of the semester examination. Thank you for your patience!

---

## ns-3 Implementation of RIT-compliant Receiver-Initiated MAC Framework

This repository contains a self-implementation of the research paper:

> *"An ns-3 Evaluation Framework for Receiver-Initiated MAC Protocols with Configurable Enhancement Modules Across Various Network Scenarios"*

---

## 📌 Project Overview

This project focuses on implementing and evaluating the **Receiver-Initiated Transmission (RIT)** mechanism, as defined in the **IEEE 802.15.4e** standard, using the **ns-3** network simulator.

Unlike traditional sender-initiated protocols, in RIT the **receiver** initiates the communication by periodically broadcasting a beacon.

The goal of this implementation is to provide a **unified and reproducible platform** to compare various enhancement strategies for receiver-initiated MAC protocols under realistic network conditions.

---

## ✨ Key Features

- **RIT-compliant MAC Layer:** A complete implementation of the IEEE 802.15.4e RIT procedure in ns-3.
- **Modular Enhancement Options:** Includes toggleable modules for:
  - **Selectable Channel Access:** Support for CSMA/CA, Pre-CS (from F-RIT), and No Carrier Sense for both beacons and data.
  - **Beacon Interval Control:** Options for Fixed intervals or Randomized intervals (to prevent synchronization).
  - **Beacon ACK:** A mechanism where the sender replies with a short ACK before data transmission to save energy.
  - **Compact Beacon Frame:** Optimized 14-byte beacon format to reduce overhead.
- **Realistic Simulation Setup:** Models for clock drift, rank-based multi-hop routing, and diverse node placement patterns (Edge and Central).

---

## 🛠 Tech Stack

| Component | Details |
|-----------|---------|
| **Simulator** | ns-3 (Network Simulator 3) |
| **Language** | C++ (core protocol logic), Python (log parsing & visualization) |
| **Protocol Base** | IEEE 802.15.4 Low-Rate Wireless Personal Area Networks (LR-WPANs) |

---

## 📊 Evaluation Metrics

The framework evaluates protocol performance based on:

- **PDR (Packet Delivery Ratio):** Percentage of successfully delivered packets.
- **Wake-Up Ratio:** Percentage of time a node stays awake (energy efficiency metric).
- **End-to-End Latency:** Time taken from packet generation to successful reception.

---

## 📝 Note

This is a self-initiated implementation based on the architectural details and methodologies described in the referenced paper. It aims to support fair comparison and future research in **energy-harvesting** and **low-power wireless sensor networks (WSNs)**.