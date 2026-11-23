# FPGA-Enabled Real-Time Audio Sampling, Processing, and Recording for an Electronic Drum Set

* **Source PDF:** `../papers/DAFx26_demo_70.pdf`
* **BibTeX Key:** `taylor2026fpga`
* **Bibliographic Info:** M. A. Taylor & M. Rau, *"FPGA-Enabled Real-Time Audio Sampling, Processing, and Recording for an Electronic Drum Set,"* *Proc. 29th Int. Conf. on Digital Audio Effects (DAFx26)*, Cambridge, MA, USA, pp. 512–515, Sept. 2026.

## Core Contribution
Demonstrates a deterministic low-latency ($1.33\text{ ms}$ DSP pipeline) 16-channel FPGA audio processor with raw Layer-2 Ethernet streaming to a host computer using a closed-loop PI-controlled fractional resampler to eliminate clock drift.

## Relevant Information
* **Deterministic Sub-Millisecond DSP:** Achieves $1.33\text{ ms}$ total processing latency at $48\text{ kHz}$ using minimum-phase FIR filters (instead of linear-phase) and time-division multiplexed DSP blocks.
* **Ethernet Audio & Clock-Drift Compensation:** Streams 32-sample Ethernet payloads ($667\,\mu\text{s}$ buffering, $\sim 400\,\mu\text{s}$ network RTT) into a 512-sample host ring buffer ($5.33\text{ ms}$ latency) regulated by a Proportional-Integral (PI) controller driving a variable-rate Farrow resampler.

## Role in Thesis (Real-Time IEM Spatial Mixer)
* Provides concrete latency budgets for networked live-audio transport and demonstrates why **minimum-phase filters** (rather than linear-phase) are essential to keep end-to-end IEM latency under perceptual thresholds ($<5\text{--}10\text{ ms}$).
* Offers a reference mechanism (PI buffer-fill feedback + fractional resampling) if integrating custom Ethernet/AoIP I/O without hardware PTP clocking.
