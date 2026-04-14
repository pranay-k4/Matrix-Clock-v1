# Led-Matrix-Display
So I am planning on making a led matrix display 16x32 but I wanna try 32x64 too I have seen youtube vids and all and always wanted to have one made by myself. I plan to make my custom PCB I would add audio visualizer and my Spotify song display and I would add a clock



# ESP32 HUB75 Smart LED Matrix Display

## Overview

This project is a real-time embedded LED display system built using an ESP32 microcontroller and a HUB75 RGB LED matrix panel. The system is designed to display dynamic content such as a digital clock, scrolling text, and animated UI modes.

It is built as a full embedded systems project focusing on firmware design, power stability, and modular hardware architecture.

---

## Features

- Real-time clock display
- Multiple display modes (clock, text, animations)
- Button-based user interface
- RTC-based timekeeping support
- Modular hardware design using ESP32 and HUB75 LED matrix
- Designed for stable high-current LED operation

---

## System Architecture

The system is divided into four main subsystems:

- **ESP32 (Controller):** Handles logic, display rendering, and user input
- **HUB75 LED Matrix:** Outputs real-time pixel data
- **Power System:** Provides stable 5V high-current supply
- **RTC Module:** Maintains accurate time tracking
- **Button Inputs:** Allows user interaction and mode switching

(See `/docs/architecture.png` for full system diagram)

---

## Hardware Components

- ESP32 DevKit V1
- HUB75 LED Matrix (32x64)
- 5V 10A Power Supply
- DS3231 RTC Module
- Push Buttons
- Supporting power regulation components (capacitors, buck converter, etc.)

Full list available in `/docs/BOM.md`

---

## Project Goals

- Build a stable embedded LED display system
- Learn real-world hardware + firmware integration
- Design proper power distribution for high-current loads
- Implement modular firmware architecture
- Document full engineering process for portfolio and grant submission

---

## Folder Structure
