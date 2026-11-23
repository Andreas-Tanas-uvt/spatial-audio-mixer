# A DSP-Based Audio Signal Processor

* **Source PDF:** `../papers/9609x008.pdf`
* **BibTeX Key:** `forrer1996dsp`
* **Bibliographic Info:** J. Forrer, *"A DSP-Based Audio Signal Processor,"* *QEX*, Sept. 1996, pp. 1–9.

## Core Contribution
Details the theory and fixed-point DSP implementation of a real-time audio signal processor featuring a Hilbert-transform frequency shifter, multirate FIR filtering, and adaptive LMS/Wiener filtering.

## Relevant Information
* Demonstrates causal FIR Hilbert transform design (order $M$, group delay $(M-1)/2$ samples) to generate analytic signals $z(t) = x(t) + j\hat{x}(t)$ for phase-accurate frequency/phase manipulation.
* Shows how **multirate processing** (decimation/interpolation) drastically reduces FIR tap counts and clock-cycle budgets per sample while preserving steep filter skirts.
* Documents real-time adaptive Least-Mean-Squares (LMS) and Wiener filtering for noise suppression and feedback/heterodyne auto-notching.

## Role in Thesis (Real-Time IEM Spatial Mixer)
* Provides practical DSP building blocks for causal phase-shifting/decorrelation (Hilbert transformers) and CPU-budget optimization via multirate filtering when running on constrained real-time deadlines.
* Offers lightweight adaptive filtering strategies relevant to stage bleed or feedback suppression in live IEM feeds.
