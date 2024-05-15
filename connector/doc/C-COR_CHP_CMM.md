---
uid: Connector_help_C-COR_CHP_CMM
---

# C-COR CHP CMM

The **C-COR CHP CMM** connector is an SNMP-based connector that can be used to monitor and configure the **C-COR CHP CMM.**

## About

This connector provides a monitoring interface for the **C-COR CHP CMM** module. It is automatically generated by the parent connector **C-COR CHP SMM**.

### Product Info

| Range     | Device Firmware Version          |
|------------------|----------------------------------|
| 2.0.0.x          | Boot v002.003, Download v002.004 |

## Installation and configuration

### Creation

This connector is used by DVEs that are automatically created by the parent element. No user input is required.

## Usage

### General

This page displays general information about the card: **Physical State**, **Name**, **Address**, **Module State** and **Local Control**.

### CMM

On this page, you can among others find information about the voltage and temperature, as well as alarm information.

The page contains the following page buttons:

- **Device Info**: Displays information about the device, such as the **Module**, **Firmware and Hardware version**, **Serial Number**, etc.
- **Internal Threshold:** Contains the major and minor voltage thresholds **(12V, 5V, 3.3V and -5V)** and **internal temperature thresholds**.

### Fans

This page displays the **Fans Alarm Status** and **Fans Current**.

It contains two page buttons that provide access to **Fans Information** and **Fans Thresholds (Fan Current)**.