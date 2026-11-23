# Audinate Dante Documentation (Dante Virtual Soundcard & Dante Controller)

* **Source PDFs:** `../papers/AUD-MAN-DanteVirtualSoundcard_4.5.x-v1.0.pdf`, `../papers/dante-controller-user-guide.pdf`
* **BibTeX Keys:** `audinate2025dvs`, `audinate2011dc`
* **Bibliographic Info:**
  1. Audinate Pty Ltd, *Dante Virtual Soundcard User Guide (Version 4.5.x)*, Document `AUD-MAN-DanteVirtualSoundcard_4.5.x-v1.0`, Jan. 2025.
  2. Audinate Pty Ltd, *Dante Controller User Guide (Version 3.1.x)*, Document `AUD-MAN-Dante Controller-3.1.2-V1.0`, Feb. 2011.

## Core Contribution
Official technical specifications for Audio-over-IP (AoIP) transport, IEEE 1588 PTP sample-accurate clock synchronization, unicast/multicast flow routing, and host driver latency/buffering on macOS (Core Audio) and Windows (ASIO).

## Relevant Information
* **Channel & Sample Rate Capacity:** DVS supports up to $64\times 64$ channels at $48\text{ kHz}/24\text{-bit}$ (Standard) or $128\times 128$ channels at $48\text{--}96\text{ kHz}$ (DVS Pro) over Gigabit Ethernet; Wi-Fi is unsupported.
* **Latency Architecture:** Hardware Dante devices achieve $0.15\text{ ms}$ to $1.0\text{ ms}$ network Rx latency; DVS software interfaces require $4\text{ ms}$, $6\text{ ms}$, or $10\text{ ms}$ device latency plus host audio buffer latency (ASIO $32\text{--}2048$ samples or Core Audio buffer) to absorb OS scheduling jitter.
* **Flow & Clock Management:** Unicast flows carry up to 4 channels point-to-point, while multicast flows ($8$ channels/flow) prevent transmitter bandwidth saturation when feeding multiple stereo IEM mixes. All nodes synchronize via IEEE 1588 PTP master election.

## Role in Thesis (Real-Time IEM Spatial Mixer)
* Defines the **end-to-end I/O latency budget** when ingesting multitrack stage channels from a digital console (e.g., Behringer WING/X32 via Dante) into a macOS/PC host engine.
* Shows the practical trade-off between **software DVS** ($4\text{ ms}$ minimum DVS latency + Core Audio buffer) versus **hardware Dante interfaces** ($0.15\text{--}1.0\text{ ms}$ Rx latency) for meeting live musician IEM latency tolerances, and dictates using multicast flows for shared stage stems.
