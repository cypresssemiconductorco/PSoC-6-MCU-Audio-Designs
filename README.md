## Table of Contents

* [Introduction](#introduction)
* [Navigating the Repository](#navigating-the-repository)
* [Required Tools](#required-tools)
* [Code Examples List](#code-examples-list)
* [References](#references)

# Introduction
This repository contains examples and demos for PSoC 6 MCU family of devices, a single chip solution for the emerging IoT devices. PSoC 6 MCU bridges the gap between expensive, power hungry application processors and low‑performance microcontrollers (MCUs). The ultra‑low‑power, dual-core architecture of PSoC 6 MCU offers the processing performance needed by IoT devices, eliminating the tradeoffs between power and performance.

Cypress provides a wealth of data at [www.cypress.com](http://www.cypress.com/) to help you select the right PSoC device and effectively integrate it into your design. Visit our [PSoC 6 MCU](http://www.cypress.com/products/32-bit-arm-cortex-m4-psoc-6) webpage to explore more about PSoC 6 MCU family of device.
Feel free to explore through the code example source files and let us innovate together!

# Navigating the Repository

This repository provides reference PSoC 6 projects for developing audio applications using the I2s and PDM to PCM blocks of the PSoC 6 MCU.
If you are new to developing projects with PSoC 6 MCU, we recommend you to refer the [PSoC 6 Getting Started GitHub](https://github.com/cypresssemiconductorco/PSoC-6-MCU-Getting-Started) page which can help you familiarize with device features and guides you to create a simple PSoC 6 design with PSoC Creator IDE. For other block specific design please visit the following GitHub Pages:
#### 1. [Analog Designs](https://github.com/cypresssemiconductorco/PSoC-6-MCU-Analog-Designs)
#### 2. [Digital Designs](https://github.com/cypresssemiconductorco/PSoC-6-MCU-Digital-Designs)
#### 3. [BLE Connectivity Designs](https://github.com/cypresssemiconductorco/PSoC-6-MCU-BLE-Connectivity-Designs)
#### 4. [Device Related Designs](https://github.com/cypresssemiconductorco/PSoC-6-MCU-Device-Related-Design)
#### 5. [System-Level Designs](https://github.com/cypresssemiconductorco/PSoC-6-MCU-System-Level-Designs)
#### 6. [PSoC 6 Pioneer Kit Designs](https://github.com/cypresssemiconductorco/PSoC-6-MCU-Pioneer-Kits)
#### 7. [PSoC 6 MCU based RTOS Designs](https://github.com/cypresssemiconductorco/PSoC-6-MCU-RTOS-Based-Design)

You can use these block level examples to guide you through the development of a system-level design using PSoC 6 MCU. All the code examples in this repository comes with well documented design guidelines to help you understand the design and how to develop it. The code examples and their associated documentation are in the Code Example folder in the repository.

# Required Tools

## Software
### Integrated Development Environment (IDE)
To use the code examples in this repository, please download and install
[PSoC Creator](http://www.cypress.com/products/psoc-creator)

## Hardware
### PSoC 6 MCU Development Kits
* [CY8CKIT-062-BLE PSoC 6 BLE Pioneer Kit](http://www.cypress.com/documentation/development-kitsboards/psoc-6-ble-pioneer-kit).

* [CY8CKIT-062-WiFi-BT PSoC 6 WiFi-BT Pioneer Kit](http://www.cypress.com/documentation/development-kitsboards/psoc-6-wifi-bt-pioneer-kit). 

**Note** Please refer to the code example documentation for selecting the appropriate kit for testing the project

## Code Examples List
#### 1. CE218636 – PSoC 6 MCU Inter-IC Sound (I2S) Example
This code example shows how to play a short audio on a speaker or headphone. The application stores the audio data in the
flash memory. This data is written to the output TX FIFO of the I2S hardware block, which interfaces with an audio codec chip.
The audio codec chip converts a digital audio stream into analog. The chip is configured by the PSoC 6 over an I2C interface.
The code example includes the files codec.c/h, which wrap the configuration of the audio codec. 

#### 2. CE219431 - PSoC 6 MCU PDM-to-PCM Example
This example demonstrates how to use the pulse-density modulation/pulse-code modulation (PDM/PCM) hardware block in
PSoC 6 with a digital microphone.

#### 3. CE220762 – PSoC 6 MCU PDM to I2S Example
This code example shows how to record a short audio sample from a microphone to SRAM, then play it on a speaker or
headphone. The example uses DMA to transfer data from the PDM/PCM hardware block, which interfaces with a microphone,
to SRAM. Once the recording is complete, other DMAs transfer the recorded data to the I2S hardware block, which interfaces
with an audio codec chip. This configuration frees the CPU completely, so it can execute other tasks.

#### 4. CE222221 – PSoC 6 MCU Voice Recorder
This project shows how PSoC 6 MCU can be used to record audio data, store it and play it back. It uses a digital microphone
with the PDM/PCM hardware block. All the audio data captured by the microphone is stored to an external flash memory. After
the recording is completed, you can play the audio data over I2S, which interfaces with an audio codec. You can
record/stop/play/pause/resume with CapSense® buttons. You can control the audio volume with the CapSense slider. The TFT
LCD displays the current state of the voice recorder, the volume, and the time of the record/play.

## References
#### 1. PSoC 6 MCU
PSoC 6 bridges the gap between expensive, power hungry application processors and low‑performance microcontrollers (MCUs). The ultra‑low‑power PSoC 6 MCU architecture offers the processing performance needed by IoT devices, eliminating the tradeoffs between power and performance. The PSoC 6 MCU contains a dual‑core architecture, with both cores on a single chip. It has an Arm® Cortex®‑M4 for high‑performance tasks, and an Arm® Cortex®‑M0+ for low-power tasks, and with security built-in, your IoT system is protected.
To learn more on the device, please visit our [PSoC 6 MCU](http://www.cypress.com/products/32-bit-arm-cortex-m4-psoc-6) webpage.

####  2. PSoC 6 MCU Learning resource list
##### 2.1 PSoC 6 MCU Datasheets
Device datasheets list the features and electrical specifications of PSoC 6 families of devices: [PSoC 6 MCU Datasheets](http://www.cypress.com/search/all?f%5B0%5D=meta_type%3Atechnical_documents&f%5B1%5D=resource_meta_type%3A575&f%5B2%5D=field_related_products%3A114026)
##### 2.2 PSoC 6 MCU Application Notes
Application notes are available on the Cypress website to assist you with designing your PSoC application: [A list of PSoC 6 MCU ANs](http://www.cypress.com/psoc6an)
##### 2.3 PSoC 6 MCU Component Datasheets
PSoC Creator utilizes "components" as interfaces to functional Hardware (HW). Each component in PSoC Creator has an associated datasheet that describes the functionality, APIs, and electrical specifications for the HW. You can access component datasheets in PSoC Creator by right-clicking a component on the schematic page or by going through the component library listing. You can also access component datasheets from the Cypress website: [PSoC 6 Component Datasheets](http://www.cypress.com/documentation/component-datasheets)
##### 2.4 PSoC 6 MCU Technical Reference Manuals (TRM)
The TRM provides detailed descriptions of the internal architecture of PSoC 6 devices:[PSoC 6 MCU TRMs](http://www.cypress.com/psoc6trm)

## FAQ

### Technical Support
Need support for your design and development questions? Check out the [Cypress Developer Community 3.0](https://community.cypress.com/welcome).  

Interact with technical experts in the embedded design community and receive answers verified by Cypress' very best applications engineers. You'll also have access to robust technical documentation, active conversation threads, and rich multimedia content. 

You can also use the following support resources if you need quick assistance:
##### Self-help: [Technical Support](http://www.cypress.com/support)
##### Local Sales office locations: [Sales Office](http://www.cypress.com/about-us/sales-offices)
