---
title: "CamCommand: Garmin to Lumix BLE Camera Remote"
tags:
  - software
  - garmin
  - ble
  - hardware
  - wip
---

# CamCommand (`camcmd`)

> *Status: In Active Development (WIP) — Reverse-Engineering Panasonic Lumix BLE Protocol*

![[garmin-camcmd-launcher-icon.png]]
*CamCommand Garmin Connect IQ application icon for Instinct 3 Solar.*

**CamCommand** is a custom Garmin Connect IQ application for the **Garmin Instinct 3 Solar (45mm)** designed to provide direct, phone-free Bluetooth Low Energy (BLE) remote control and 1 Hz GPS geotagging for a **Panasonic Lumix DC-G95 (`G95D`)** mirrorless camera.

---

## The Vision

When shooting outdoors or vlogging, taking out an iPhone to trigger camera record or wait for the clunky Panasonic Image App to sync is slow and cumbersome.

The goal of `camcmd` is to let the Garmin Instinct 3 Solar act as an always-accessible wrist remote:
- **`[START]` button**: Start / stop video recording with wrist haptic confirmation.
- **Photo Shutter**: Single shutter release with focus lock.
- **1 Hz GPS Geotagging**: Continuously stream watch GPS coordinates directly into the camera's EXIF metadata stream via BLE (`DAFF1BC0`).
- **Zero Phone Dependency**: Connects directly between the watch and the camera over BLE without the Garmin Connect Mobile bridge.

---

## The Reverse-Engineering Challenges

Panasonic cameras use a proprietary, undocumented BLE GATT handshake that expects the official Panasonic Image App on iOS/Android. Reverse-engineering this for Garmin's constrained Connect IQ runtime has required extensive packet sniffing and experimental trials:

### 1. GATT Discovery Collisions
The camera firmware sends an internal GAP query around $t + 300\text{ ms}$ after initial connection. If the watch fires ATT write requests simultaneously, the camera drops the link.
- **Fix**: Implemented a mandatory 500 ms settling delay after service discovery before initiating writes.

### 2. The 3-Attempt Name Handshake
The camera validates the client device name against internal NVRAM paired device slots:
- **Attempt 1 (`"iPhone"`)**: Checks if the camera accepts the standard Image App piggyback mode.
- **Attempt 2 (`"Instinct 3 - 45mm"`)**: Checks full hardware GAP `0x2A00` name alignment.
- **Attempt 3 (`"Instinct 3 - 45m"`)**: Checks 16-byte fixed-buffer truncation alignment.

### 3. Missing CCCD Descriptors
Unlike standard BLE peripherals, the Lumix G95 omits standard `0x2902` Client Characteristic Configuration Descriptors on certain proprietary characteristics, causing standard Connect IQ profile discovery to fail unless handled sequentially.

---

## Tech Stack & Tooling

- **Target Hardware**: Garmin Instinct 3 Solar (45mm) / Panasonic Lumix DC-G95
- **Language**: Monkey C (Garmin Connect IQ SDK 7.x)
- **Protocol**: Bluetooth Low Energy (GATT custom services: `0x0100`, `0x0102`, `0x011C`)
- **Analysis Tools**: Wireshark BLE packet sniffer, Nordic nRF Connect, OpenMTP sideloading

---

## Interconnected Notes
