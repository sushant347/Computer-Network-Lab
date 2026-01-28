# 📝 Lab Report: Ethernet Cabling and Network Termination

## 🎯 1. Learning Objectives
The primary goals of this laboratory session were to:
* **Master** the physical construction of Ethernet cables used in LAN environments.
* **Differentiate** between End Devices (e.g., PCs) and Network Nodes (e.g., Switches) regarding signal transmission.
* **Apply** TIA/EIA wiring standards to terminate twisted-pair cables correctly.
* **Utilize** cable testing tools to verify continuity and troubleshoot wiring faults.

## 🧰 2. Equipment & Tools
To complete the termination and testing, the following components were utilized:

* **Cable:** Unshielded Twisted Pair (UTP) - Category 5e or Category 6.
    [Image of Cat5e unshielded twisted pair cable structure]
* **Connectors:** RJ-45 (8P8C) modular plugs.
    [Image of RJ45 connector pinout]
* **Tools:** Modular Crimping Tool (Crimper) and Wire Stripper.
* **Testing:** Network LAN Cable Tester.

---

## 📘 3. Theoretical Framework

Ethernet connectivity relies on twisted-pair cabling to transmit data signals. These cables consist of 8 copper conductors twisted into 4 pairs to cancel out electromagnetic interference (crosstalk). The arrangement of these wires inside the RJ-45 connector is governed by the **TIA/EIA-568** standards.

### 🔄 Device Classifications & Pin Usage
Devices transmit (TX) and receive (RX) data on specific pins. Understanding this distinction is vital for choosing the right cable.

* **Category A (End Devices):** Workstations, Laptops, Routers.
    * *Transmits on:* Pins 1 & 2
    * *Receives on:* Pins 3 & 6
* **Category B (Network Intermediaries):** Switches, Hubs.
    * *Transmits on:* Pins 3 & 6
    * *Receives on:* Pins 1 & 2

> **💡 Key Concept:** For communication to occur, the TX pins of one device must connect to the RX pins of the other.

---

## ⚡ 4. Wiring Standards and Cable Types

There are two standard color codes used for terminating cables: **T568A** and **T568B**.

[Image of T568A vs T568B wiring color code diagram]

### A. Straight-Through Cable
**Usage:** Connecting *dissimilar* devices (e.g., Computer ➡ Switch).
**Setup:** Both ends of the cable use the **same** standard (usually T568B on both ends).

**🎨 Standard T568B Color Code:**
1.  ⚪🟠 White-Orange
2.  🟠 Orange
3.  ⚪🟢 White-Green
4.  🔵 Blue
5.  ⚪🔵 White-Blue
6.  🟢 Green
7.  ⚪🟤 White-Brown
8.  🟤 Brown

### B. Crossover Cable
**Usage:** Connecting *similar* devices (e.g., Switch ➡ Switch, or PC ➡ PC).
**Setup:** One end is wired as **T568A**, and the other end is wired as **T568B**. This physically crosses the TX and RX lines.

**🎨 Standard T568A Color Code (Side A):**
1.  White-Green
    2.  Green
    3.  White-Orange
    4.  Blue
    5.  White-Blue
    6.  Orange
    7.  White-Brown
    8.  Brown

---

## ⚖️ 5. Comparative Analysis

| Feature | Straight-Through | Crossover |
| :--- | :--- | :--- |
| **Wiring Config** | Identical on both ends (B-to-B) | Swapped ends (A-to-B) |
| **Device Match** | Different Categories (PC ➡ Switch) | Same Category (PC ➡ PC) |
| **Signal Logic** | TX goes to RX (handled by port) | TX physically crosses to RX inside cable |
| **Primary Use** | Standard LAN infrastructure | Direct linking or cascading switches |

---

## 🔎 6. Observations & Testing Results
After crimping the RJ-45 connectors, the cables were inserted into the Network LAN Tester.

* **Procedure:** The main unit and remote unit were connected to opposite cable ends.
* **Success Indicator:** LEDs 1 through 8 lit up in sequential order for the Straight-Through cable. For the Crossover cable, the LEDs corresponded to the swapped pairs (1-3, 2-6, etc.).
* **Troubleshooting:** Initial attempts showed a missed connection on Pin 4. The connector was re-crimped to ensure the copper blades fully pierced the wire insulation.

## 💡 7. Discussion
The lab highlighted that while modern devices often support *Auto-MDIX* (automatically detecting cable type), understanding the physical difference between Straight-Through and Crossover is fundamental for network engineering. Straight-through is the industry standard for connecting endpoints to the network, while crossover is reserved for specific peer-to-peer scenarios.

## 🚀 8. Conclusion
This session provided essential hands-on experience in network layer 1 technologies. By manually terminating cables, we verified the importance of the TIA/EIA-568 color standards. We successfully demonstrated that:

1.  Precision is required when arranging wires into the RJ-45 connector.
2.  Proper tools (crimper/tester) are necessary to certify cable reliability.
3.  Selecting the correct cabling scheme is critical based on the devices being connected.