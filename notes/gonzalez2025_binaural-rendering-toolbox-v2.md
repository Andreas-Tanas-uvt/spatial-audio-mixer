# New Release of the Binaural Rendering Toolbox: Introducing Version 2.0

* **Source PDF:** `../papers/000605.pdf`
* **BibTeX Key:** `gonzalez2025brt`
* **Bibliographic Info:** D. González-Toledo et al., *"New Release of the Binaural Rendering Toolbox: Introducing Version 2.0,"* *Proc. Forum Acusticum / Euronoise 2025*, Málaga, Spain, pp. 6457–6464, 2025.

## Core Contribution
Introduces BRT v2.0, an open-source (GPL) modular C++ header-only library and OSC-controllable standalone renderer (BeRTA) supporting SOFA HRTFs/BRIRs, hybrid Ambisonics/direct rendering, near-field/parallax correction, and bilateral headphone compensation filters.

## Relevant Information
* **Layered C++ Architecture:** Separates Low-Level Core (SOFA I/O, math, convolution), Processing Modules (filters, near-field, delay), High-Level Models (Source, Environment, Listener), and Bilateral Filters using an observer pattern for real-time parameter updates.
* **Hybrid Rendering & Windowing:** Supports direct HRTF convolution for direct paths paired with Ambisonic Virtual Loudspeakers / Reverberant Virtual Loudspeakers (RVL) using raised-cosine windowed BRIRs to reduce CPU load as source count scales.
* **Perceptual Refinements:** Includes near-field distance filtering, acoustic parallax correction (ear offset vs. head center), independent ITD scaling (by head circumference), and Second-Order Section (SOS) bilateral filters for headphone/IEM frequency-response compensation.
* **Control & Safety:** Exposes full scene control over Open Sound Control (OSC) and includes SPL calibration and configurable output limiters.

## Role in Thesis (Real-Time IEM Spatial Mixer)
* Serves as the primary architectural reference (and potential core DSP dependency) for structuring a modular C++ spatial audio engine.
* Directly solves two critical IEM requirements: **IEM frequency-response compensation** via the bilateral SOS filter stage and **multi-musician scalability** via hybrid direct-HRTF + Ambisonic reverb decoding.
* Provides an OSC command schema for linking stage console/performer UI controls to the rendering engine.
