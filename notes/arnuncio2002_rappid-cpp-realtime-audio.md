# A C++ Development Platform for Real Time Audio Processing and Synthesis Applications

* **Source PDF:** `../papers/DAFX02_Arnuncio_Hinojosa_deBoer_c++_development.pdf`
* **BibTeX Key:** `arnuncio2002rappid`
* **Bibliographic Info:** E. Robledo Arnuncio, R. Hinojosa, & M. de Boer, *"A C++ Development Platform for Real Time Audio Processing and Synthesis Applications,"* *Proc. 5th Int. Conf. on Digital Audio Effects (DAFx-02)*, Hamburg, Germany, pp. 221–225, Sept. 2002.

## Core Contribution
Presents Rappid, an open-source C++ real-time audio processing framework built on CLAM that decouples high-priority audio DSP threads from asynchronous GUI/control threads for live musical performance.

## Relevant Information
* **Thread Separation & Safety:** Isolates the real-time POSIX audio callback thread (scheduled with elevated OS priority + watchdog protection against deadlocks) from non-real-time UI and parameter-control threads.
* **Modular Processing Graph:** Encapsulates DSP nodes with standardized lifecycle methods (`ConcreteConfigure`, `ConcreteStart`, and frame-based `Do()`) supporting both time-domain and STFT spectral-domain frames.
* **Live Reliability Lessons:** Emphasizes worst-case execution time (WCET) profiling and avoiding OS/driver interruptions during continuous multi-hour live performances.

## Role in Thesis (Real-Time IEM Spatial Mixer)
* Guides the real-time software engineering architecture of the mixer: lock-free/asynchronous parameter updates from the UI/OSC thread to the real-time audio callback thread, preventing priority inversion and buffer dropouts during live shows.
